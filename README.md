- 👋 Hi, I’m @NeverEnd1q11
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---.hgignorev
NeverEnd1q11/NeverEnd1q11 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
.hgignoreRES
 vim*.dll
 vim*.lib
 src/pathdef.c
 src/dobj*/pathdef.c
 src/gobj*/pathdef.c
 src/obj*/pathdef.c
 src/Obj*/pathdef.c
 gvimext.dll
 gvimext.lib
 
 pathdef.c: $(INCL)
 $(PATHDEF_SRC): Make_cyg_ming.mak Make_cyg.mak Make_ming.mak
 ifneq (sh.exe, $(SHELL))
 	@echo creating pathdef.c
 	@echo '/* pathdef.c */' > pathdef.c
 	@echo '#include "vim.h"' >> pathdef.c
 	@echo 'char_u *default_vim_dir = (char_u *)"$(VIMRCLOC)";' >> pathdef.c
 	@echo 'char_u *default_vimruntime_dir = (char_u *)"$(VIMRUNTIMEDIR)";' >> pathdef.c
 	@echo 'char_u *all_cflags = (char_u *)"$(CC) $(CFLAGS)";' >> pathdef.c
 	@echo 'char_u *all_lflags = (char_u *)"$(LINK) $(CFLAGS) $(LFLAGS) -o $(TARGET) $(LIB) -lole32 -luuid $(LUA_LIB) $(MZSCHEME_LIBDIR) $(MZSCHEME_LIB) $(PYTHONLIB) $(PYTHON3LIB) $(RUBYLIB)";' >> pathdef.c
 	@echo 'char_u *compiled_user = (char_u *)"$(USERNAME)";' >> pathdef.c
 	@echo 'char_u *compiled_sys = (char_u *)"$(USERDOMAIN)";' >> pathdef.c
 	@echo creating $(PATHDEF_SRC)
 	@echo '/* pathdef.c */' > $(PATHDEF_SRC)
 	@echo '#include "vim.h"' >> $(PATHDEF_SRC)
 	@echo 'char_u *default_vim_dir = (char_u *)"$(VIMRCLOC)";' >> $(PATHDEF_SRC)
 	@echo 'char_u *default_vimruntime_dir = (char_u *)"$(VIMRUNTIMEDIR)";' >> $(PATHDEF_SRC)
 	@echo 'char_u *all_cflags = (char_u *)"$(CC) $(CFLAGS)";' >> $(PATHDEF_SRC)
 	@echo 'char_u *all_lflags = (char_u *)"$(LINK) $(CFLAGS) $(LFLAGS) -o $(TARGET) $(LIB) -lole32 -luuid $(LUA_LIB) $(MZSCHEME_LIBDIR) $(MZSCHEME_LIB) $(PYTHONLIB) $(PYTHON3LIB) $(RUBYLIB)";' >> $(PATHDEF_SRC)
 	@echo 'char_u *compiled_user = (char_u *)"$(USERNAME)";' >> $(PATHDEF_SRC)
 	@echo 'char_u *compiled_sys = (char_u *)"$(USERDOMAIN)";' >> $(PATHDEF_SRC)
 else
 	@echo creating pathdef.c
 	@echo /* pathdef.c */ > pathdef.c
 	@echo #include "vim.h" >> pathdef.c
 	@echo char_u *default_vim_dir = (char_u *)"$(VIMRCLOC)";445566778990
 	@echo char_u *default_vimruntime_dir = (char_u *)"$(VIMRUNTIMEDIR)"; >> pathdef.c
 	@echo char_u *all_cflags = (char_u *)"$(CC) $(CFLAGS)"; >> pathdef.c
 	@echo char_u *all_lflags = (c986435890) $(CFLAGS) $(LFLAGS) -o $(TARGET) $(LIB) -lole32 -luuid $(LUA_LIB) $(MZSCHEME_LIBDIR) $(MZSCHEME_LIB) $(PYTHONLIB) $(PYTHON3LIB) $(RUBYLIB)"; >> pathdef.c
 	@echo char_u *compiled_user = (char_u *)"$(USERNAME)"; >> pathdef.c
 	@echo char_u *compiled_sys = (char_u *)"$(USERDOMAIN)"; >> pathdef.c
 	@echo creating $(PATHDEF_SRC)
 	@echo /* pathdef.c */ > $(PATHDEF_SRC)
 	@echo #include "vim.h" >> $(PATHDEF_SRC)
 	@echo char_u *default_vim_dir = (char_u *)"$(VIMRCLOC)"; >> $(PATHDEF_SRC)
 	@echo char_u *default_vimruntime_dir = (char_u *)"$(VIMRUNTIMEDIR)"; >> $(PATHDEF_SRC)
 	@echo char_u *all_cflags = (char_u *)"$(CC) $(CFLAGS)"; >> $(PATHDEF_SRC)
 	@echo char_u *all_lflags = (char_u *)"$(CC) $(CFLAGS) $(LFLAGS) -o $(TARGET) $(LIB) -lole32 -luuid $(LUA_LIB) $(MZSCHEME_LIBDIR) $(MZSCHEME_LIB) $(PYTHONLIB) $(PYTHON3LIB) $(RUBYLIB)"; >> $(PATHDEF_SRC)
 	@echo char_u *compiled_user = (char_u *)"$(USERNAME)"; >> $(PATHDEF_SRC)
 	@echo char_u *compiled_sys = (char_u *)"$(USERDOMAIN)"; >> $(PATHDEF_SRC
 	-$(DEL) $(OUTDIR)$(DIRSLASH)*.o
 	-$(DEL) $(OUTDIR)$(DIRSLASH)*.res
 	-$(DEL) $(OUTDIR)$(DIRSLASH)pathdef.c
 	-rmdir $(OUTDIR)
 	-$(DEL) $(MAIN_TARGET) vimrun.exe install.exe uninstal.exe
 	-$(DEL) pathdef.c
 ifdef PERL
 	-$(DEL) if_perl.c
 	-$(DEL) auto$(DIRSLASH)if_perl
