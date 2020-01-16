licenses(["restricted"])  # GPLv3

exports_files(["LICENSE"])

cc_binary(
    name = "swig",
    srcs = [
        "Source/CParse/cparse.h",
        "Source/CParse/cscanner.c",
        "Source/CParse/parser.c",
        "Source/CParse/parser.h",
        "Source/CParse/templ.c",
        "Source/CParse/util.c",
        "Source/DOH/base.c",
        "Source/DOH/doh.h",
        "Source/DOH/dohint.h",
        "Source/DOH/file.c",
        "Source/DOH/fio.c",
        "Source/DOH/hash.c",
        "Source/DOH/list.c",
        "Source/DOH/memory.c",
        "Source/DOH/string.c",
        "Source/DOH/void.c",
        "Source/Include/swigconfig.h",
        "Source/Include/swigwarn.h",
        "Source/Modules/allocate.cxx",
        "Source/Modules/browser.cxx",
        "Source/Modules/contract.cxx",
        "Source/Modules/directors.cxx",
        "Source/Modules/emit.cxx",
        "Source/Modules/lang.cxx",
        "Source/Modules/main.cxx",
        "Source/Modules/module.cxx",
        "Source/Modules/nested.cxx",
        "Source/Modules/overload.cxx",
        "Source/Modules/python.cxx",
        "Source/Modules/swigmain-lite.cxx",
        "Source/Modules/swigmod.h",
        "Source/Modules/typepass.cxx",
        "Source/Modules/uffi.cxx",
        "Source/Modules/utils.cxx",
        "Source/Modules/xml.cxx",
        "Source/Preprocessor/cpp.c",
        "Source/Preprocessor/expr.c",
        "Source/Preprocessor/preprocessor.h",
        "Source/Swig/cwrap.c",
        "Source/Swig/deprecate.c",
        "Source/Swig/error.c",
        "Source/Swig/extend.c",
        "Source/Swig/fragment.c",
        "Source/Swig/getopt.c",
        "Source/Swig/include.c",
        "Source/Swig/misc.c",
        "Source/Swig/naming.c",
        "Source/Swig/parms.c",
        "Source/Swig/scanner.c",
        "Source/Swig/stype.c",
        "Source/Swig/swig.h",
        "Source/Swig/swigfile.h",
        "Source/Swig/swigopt.h",
        "Source/Swig/swigparm.h",
        "Source/Swig/swigscan.h",
        "Source/Swig/swigtree.h",
        "Source/Swig/swigwrap.h",
        "Source/Swig/symbol.c",
        "Source/Swig/tree.c",
        "Source/Swig/typemap.c",
        "Source/Swig/typeobj.c",
        "Source/Swig/typesys.c",
        "Source/Swig/wrapfunc.c",
    ],
    copts = ["$(STACK_FRAME_UNLIMITED)"] + select({
        ":windows": [],
        "//conditions:default": [
            "-Wno-parentheses",
            "-Wno-unused-variable",
            "-fexceptions",
        ],
    }),
    data = [":templates"],
    includes = [
        "Source/CParse",
        "Source/DOH",
        "Source/Include",
        "Source/Modules",
        "Source/Preprocessor",
        "Source/Swig",
    ],
    output_licenses = ["unencumbered"],
    visibility = ["//visibility:public"],
    deps = ["@pcre"],
)

filegroup(
    name = "templates",
    srcs = [
        "Lib/allkw.swg",
        "Lib/attribute.i",
        "Lib/carrays.i",
        "Lib/cdata.i",
        "Lib/cffi/cffi.swg",
        "Lib/cmalloc.i",
        "Lib/constraints.i",
        "Lib/cpointer.i",
        "Lib/cstring.i",
        "Lib/cwstring.i",
        "Lib/exception.i",
        "Lib/intrusive_ptr.i",
        "Lib/inttypes.i",
        "Lib/linkruntime.c",
        "Lib/math.i",
        "Lib/pointer.i",
        "Lib/python/argcargv.i",
        "Lib/python/attribute.i",
        "Lib/python/boost_shared_ptr.i",
        "Lib/python/builtin.swg",
        "Lib/python/carrays.i",
        "Lib/python/ccomplex.i",
        "Lib/python/cdata.i",
        "Lib/python/cmalloc.i",
        "Lib/python/cni.i",
        "Lib/python/complex.i",
        "Lib/python/cpointer.i",
        "Lib/python/cstring.i",
        "Lib/python/cwstring.i",
        "Lib/python/defarg.swg",
        "Lib/python/director.swg",
        "Lib/python/embed.i",
        "Lib/python/embed15.i",
        "Lib/python/exception.i",
        "Lib/python/factory.i",
        "Lib/python/file.i",
        "Lib/python/implicit.i",
        "Lib/python/jstring.i",
        "Lib/python/pyabc.i",
        "Lib/python/pyapi.swg",
        "Lib/python/pybackward.swg",
        "Lib/python/pybuffer.i",
        "Lib/python/pyclasses.swg",
        "Lib/python/pycomplex.swg",
        "Lib/python/pycontainer.swg",
        "Lib/python/pydocs.swg",
        "Lib/python/pyerrors.swg",
        "Lib/python/pyfragments.swg",
        "Lib/python/pyhead.swg",
        "Lib/python/pyinit.swg",
        "Lib/python/pyiterators.swg",
        "Lib/python/pymacros.swg",
        "Lib/python/pyname_compat.i",
        "Lib/python/pyopers.swg",
        "Lib/python/pyprimtypes.swg",
        "Lib/python/pyrun.swg",
        "Lib/python/pyruntime.swg",
        "Lib/python/pystdcommon.swg",
        "Lib/python/pystrings.swg",
        "Lib/python/python.swg",
        "Lib/python/pythonkw.swg",
        "Lib/python/pythreads.swg",
        "Lib/python/pytuplehlp.swg",
        "Lib/python/pytypemaps.swg",
        "Lib/python/pyuserdir.swg",
        "Lib/python/pywstrings.swg",
        "Lib/python/std_alloc.i",
        "Lib/python/std_auto_ptr.i",
        "Lib/python/std_basic_string.i",
        "Lib/python/std_carray.i",
        "Lib/python/std_char_traits.i",
        "Lib/python/std_common.i",
        "Lib/python/std_complex.i",
        "Lib/python/std_container.i",
        "Lib/python/std_deque.i",
        "Lib/python/std_except.i",
        "Lib/python/std_ios.i",
        "Lib/python/std_iostream.i",
        "Lib/python/std_list.i",
        "Lib/python/std_map.i",
        "Lib/python/std_multimap.i",
        "Lib/python/std_multiset.i",
        "Lib/python/std_pair.i",
        "Lib/python/std_set.i",
        "Lib/python/std_shared_ptr.i",
        "Lib/python/std_sstream.i",
        "Lib/python/std_streambuf.i",
        "Lib/python/std_string.i",
        "Lib/python/std_unordered_map.i",
        "Lib/python/std_unordered_multimap.i",
        "Lib/python/std_unordered_multiset.i",
        "Lib/python/std_unordered_set.i",
        "Lib/python/std_vector.i",
        "Lib/python/std_vectora.i",
        "Lib/python/std_wios.i",
        "Lib/python/std_wiostream.i",
        "Lib/python/std_wsstream.i",
        "Lib/python/std_wstreambuf.i",
        "Lib/python/std_wstring.i",
        "Lib/python/stl.i",
        "Lib/python/typemaps.i",
        "Lib/python/wchar.i",
        "Lib/runtime.swg",
        "Lib/shared_ptr.i",
        "Lib/std/_std_deque.i",
        "Lib/std/std_alloc.i",
        "Lib/std/std_basic_string.i",
        "Lib/std/std_carray.swg",
        "Lib/std/std_char_traits.i",
        "Lib/std/std_common.i",
        "Lib/std/std_container.i",
        "Lib/std/std_deque.i",
        "Lib/std/std_except.i",
        "Lib/std/std_ios.i",
        "Lib/std/std_iostream.i",
        "Lib/std/std_list.i",
        "Lib/std/std_map.i",
        "Lib/std/std_multimap.i",
        "Lib/std/std_multiset.i",
        "Lib/std/std_pair.i",
        "Lib/std/std_queue.i",
        "Lib/std/std_set.i",
        "Lib/std/std_sstream.i",
        "Lib/std/std_stack.i",
        "Lib/std/std_streambuf.i",
        "Lib/std/std_string.i",
        "Lib/std/std_unordered_map.i",
        "Lib/std/std_unordered_multimap.i",
        "Lib/std/std_unordered_multiset.i",
        "Lib/std/std_unordered_set.i",
        "Lib/std/std_vector.i",
        "Lib/std/std_vectora.i",
        "Lib/std/std_wios.i",
        "Lib/std/std_wiostream.i",
        "Lib/std/std_wsstream.i",
        "Lib/std/std_wstreambuf.i",
        "Lib/std/std_wstring.i",
        "Lib/std_except.i",
        "Lib/stdint.i",
        "Lib/stl.i",
        "Lib/swig.swg",
        "Lib/swigarch.i",
        "Lib/swigerrors.swg",
        "Lib/swiginit.swg",
        "Lib/swiglabels.swg",
        "Lib/swigrun.i",
        "Lib/swigrun.swg",
        "Lib/swigwarn.swg",
        "Lib/swigwarnings.swg",
        "Lib/typemaps/attribute.swg",
        "Lib/typemaps/carrays.swg",
        "Lib/typemaps/cdata.swg",
        "Lib/typemaps/cmalloc.swg",
        "Lib/typemaps/cpointer.swg",
        "Lib/typemaps/cstring.swg",
        "Lib/typemaps/cstrings.swg",
        "Lib/typemaps/cwstring.swg",
        "Lib/typemaps/enumint.swg",
        "Lib/typemaps/exception.swg",
        "Lib/typemaps/factory.swg",
        "Lib/typemaps/fragments.swg",
        "Lib/typemaps/implicit.swg",
        "Lib/typemaps/inoutlist.swg",
        "Lib/typemaps/misctypes.swg",
        "Lib/typemaps/primtypes.swg",
        "Lib/typemaps/ptrtypes.swg",
        "Lib/typemaps/std_except.swg",
        "Lib/typemaps/std_string.swg",
        "Lib/typemaps/std_strings.swg",
        "Lib/typemaps/std_wstring.swg",
        "Lib/typemaps/string.swg",
        "Lib/typemaps/strings.swg",
        "Lib/typemaps/swigmacros.swg",
        "Lib/typemaps/swigobject.swg",
        "Lib/typemaps/swigtype.swg",
        "Lib/typemaps/swigtypemaps.swg",
        "Lib/typemaps/traits.swg",
        "Lib/typemaps/typemaps.swg",
        "Lib/typemaps/valtypes.swg",
        "Lib/typemaps/void.swg",
        "Lib/typemaps/wstring.swg",
        "Lib/wchar.i",
        "Lib/windows.i",
    ],
    licenses = ["notice"],  # simple notice license for Lib/
    path = "Lib",
    visibility = ["//visibility:public"],
)

genrule(
    name = "swigconfig",
    outs = ["Source/Include/swigconfig.h"],
    cmd = "cat <<EOF >$@\n" +
          "#define HAVE_BOOL\n" +
          "#define HAVE_PCRE\n" +
          "#define HAVE_POPEN\n" +
          "#define PACKAGE_BUGREPORT \"http://www.swig.org\"\n" +
          "#define PACKAGE_VERSION \"3.0.8\"\n" +
          "#define STDC_HEADERS\n" +
          "#define SWIG_CXX \"bazel4lyfe\"\n" +
          "#define SWIG_LIB \"external/swig/Lib\"\n" +
          "#define SWIG_LIB_WIN_UNIX \"\"\n" +
          "#define SWIG_PLATFORM \"bazel4lyfe\"\n" +
          "EOF",
)

genrule(
    name = "get_rid_of_stuff_we_dont_need_yet",
    srcs = ["Source/Modules/swigmain.cxx"],
    outs = ["Source/Modules/swigmain-lite.cxx"],
    cmd = "sed -e '/swig_allegrocl/d'" +
          "    -e '/swig_cffi/d'" +
          "    -e '/swig_chicken/d'" +
          "    -e '/swig_clisp/d'" +
          "    -e '/swig_csharp/d'" +
          "    -e '/swig_d/d'" +
          "    -e '/swig_go/d'" +
          "    -e '/swig_guile/d'" +
          "    -e '/swig_java/d'" +
          "    -e '/swig_lua/d'" +
          "    -e '/swig_modula3/d'" +
          "    -e '/swig_mzscheme/d'" +
          "    -e '/swig_ocaml/d'" +
          "    -e '/swig_octave/d'" +
          "    -e '/swig_perl/d'" +
          "    -e '/swig_php/d'" +
          "    -e '/swig_pike/d'" +
          "    -e '/swig_r/d'" +
          "    -e '/swig_ruby/d'" +
          "    -e '/swig_scilab/d'" +
          "    -e '/swig_sexp/d'" +
          "    -e '/swig_tcl/d'" +
          "    -e '/swig_uffi/d'" +
          "    $< >$@",
)

config_setting(
    name = "windows",
    values = {"cpu": "x64_windows"},
)
