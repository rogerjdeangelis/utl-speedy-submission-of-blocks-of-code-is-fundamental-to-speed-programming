# utl-speedy-submission-of-blocks-of-code-is-fundamental-to-speed-programming

    Speedy submission of blocks of code is fundamental to speed programming.

    I call it point and shoot programming.

    All of SAS can be put on a function key, mouse action or command macro.

    https://tinyurl.com/3u4z4sfj
    https://stackoverflow.com/questions/66457629/is-there-a-shortcut-to-run-current-code-block-without-selecting

       Setup

         A.  Your left hand should hoover over the
             shift
             cntl
             alt keys
             I have about 24 actions programmed on my mouse.

         b.  Your right had should be on the mouse


       Two Speed Submission Methods.

          a. Drag the mouse over a block of code
             hit the right mouse button to submit the code.
             Note you did not have to move your hand off the mouse.

             right mouse button has these actions

             RMB log;clear;out;clear;pgm;submit;home;log;

          b. Place the cursor at the start of a block of code
             The hit function RMB

             Right mouse button has this actions

             RMB C { {;MARK;HOME;60;HOME;MARK;HOME;STORE;note;notesubmit '%nte';

             A block of code is often defined as

             {
              proc print data=sashelp.class;
              run;
              proc print data=sashelp.classfit;
              run;
             }

             You can edit the script below if your definition of
             a block of code differs.

    Related Pepositories

    https://goo.gl/xXYQ3d
    https://github.com/rogerjdeangelis?tab=repositories&q=classic+editor&type=&language=

    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories

    https://tinyurl.com/jujmv358
    https://github.com/rogerjdeangelis/utl-macros-used-in-many-of-rogerjdeangelis-repositories/blob/master/utl_perpac.sas

    {
       proc print data=sashelp.class(obs=5);
       run;
    }


    *_                   _
    (_)_ __  _ __  _   _| |_
    | | '_ \| '_ \| | | | __|
    | | | | | |_) | |_| | |_
    |_|_| |_| .__/ \__,_|\__|
            |_|
    ;
    COMMAND ===>

    00001
    00002
    00003 {
    00004    proc print data=sashelp.class(obs=5);
    00005    run;
    00006 }
    00007
    00008

    *
     _ __  _ __ ___   ___ ___  ___ ___
    | '_ \| '__/ _ \ / __/ _ \/ __/ __|
    | |_) | | | (_) | (_|  __/\__ \__ \
    | .__/|_|  \___/ \___\___||___/___/
    |_|
    ;

    Drag cursot over just

    00004    proc print data=sashelp.class(obs=5);
    00005    run;

    and hit RMB

    Place cursor on the first curly bracket and
    hit RMB

    Put this on RMB

    RMB C { {;MARK;HOME;60;HOME;MARK;HOME;STORE;note;notesubmit '%nte';

    You need to have a autocall library and
    you need to have macro 'nte' in your autocall library.

    * thic copies the macro to c:/oto/nte.sas which is my autocall library;
    filename ft15f001 "c:/oto/nte.sas";
    parmcards4;
    %macro nte/cmd;
    filename _dm clipbrd ;
    data _null_;
       infile _dm ;
       input;
       if index(_infile_,'}')>0 then stop;
       putlog _infile_;
       call execute(_infile_);
    run;quit;
    %mend nte;
    ;;;;
    run;quit;

    %inc "c:/oto/nte.sas";

    *            _               _
      ___  _   _| |_ _ __  _   _| |_
     / _ \| | | | __| '_ \| | | | __|
    | (_) | |_| | |_| |_) | |_| | |_
     \___/ \__,_|\__| .__/ \__,_|\__|
                    |_|
    ;

    Obs     NAME     SEX    AGE    HEIGHT    WEIGHT

      1    Joyce      F      11     51.3      50.5
      2    Louise     F      12     56.3      77.0
      3    Alice      F      13     56.5      84.0
      4    James      M      12     57.3      83.0
      5    Thomas     M      11     57.5      85.0

    *                                 _ _
      __ _ _ __  _ __   ___ _ __   __| (_)_  __
     / _` | '_ \| '_ \ / _ \ '_ \ / _` | \ \/ /
    | (_| | |_) | |_) |  __/ | | | (_| | |>  <
     \__,_| .__/| .__/ \___|_| |_|\__,_|_/_/\_\
          |_|   |_|
    ;

    USEFUL EDITIING COMMANDS
     *************************

      The prefix area  Many of these commands can be put on function keys using a ':', ie :ts.
      SAS is slowly removing some of these functions from theclassic editor?

      D        Delete current line
      I        Insert a line here
      C        Copy current line
      D99----  Delete next 99 lines (also could cut with mouse)
      I999---  Insert 999 blank lines useful when autoadd is set
      IB55---  Insert 55 lines before
      C3-----  Copy next three lines to some target
      A000102  Target for line copy or include file (copy after)
      B000102  Target for line copy or include file (copy before)
      M------  Move this line somewhere
      M3-----  Move next 3 lines somewhere
      O3-----  Move source lines over these lines
      R3-----  Replicate the next 3 lines

      DD00103  Block delete   CC00103  Block Copy    MM00103  Block Move
      0000104                 0000104                0000104
      DD-----                 CC-----                MM-----

      OO00103  Target Over    RR3----  Block Replicate
      0000104                 0000104
      OO-----                 RR-----

      (4-----  Shift left first 4 columns into bit bucket (distructive shift)
      )4-----  Shift right first 4 columns (distructive shift)
      >5-----  Nondistructive shift right
      <5-----  Nondistructive shift left
      >>5----  Non distructive shift right of a block of commands
      0000101
      0000102
      >>-----
      <<,)),(( Similar to single character versions
      UC----- Upper case line  - more useful on function key as :UC
      UC26--- Upper case next 26 lines
      LC----- Lower case line
      LC26    Lower case next 26 lines
      LLC---- Block of lines -lower caSE
      UUC
      TF----- Text flow lines until blank line
      TS----- Text split at cursor better on function key as :tf
      MASK - BUILD TEMPLATE FOR ENTERING DATA


       no need to look up a P-Value or probit
       put this on any command line
       %put %sysfunc(probnorm(1.96)); /* try this on command line  0.975 */
       %put %sysfunc(probit(.95)); /* 1.64 */


       ?          - previous command history IMPORTANT - asked SAS many years ago to add history

       subtop     - submit top line of editor
       bounds 1 64 -
       icon
       rchange    - change on function key hit
       rfind      - find on function key hit
       save  prg       /# save program in your profile  ie pgm.source #/
       copy  prg       /# recalls program from your profile #/
       change     - c today yesterday ic all   ( ignore case all)
       cols
       reset
       keys
       top
       bot
       n           - go to line n
       left  n
       right  n
       spell all - check spelling of all words in editor
       autoadd   - add aline at a time to editor ( usewith mask and bounds )
       vscroll 25 - set scroll amounts for forward and backward
       hscroll 10
       backward max n
       forward max  n
       bounds
       mask
       copy
       paste
       find - f 'data' first last next prev prefix suffix word
       find 'Mac' prefix
       change - c todat yesterday ic all
       rchange - change on function key hit
       rfind   - find on function key hit
       mark - highlight string, lines for submit or edit
       mark block - highlight rectangle within editor
                    does not have to be full lines
       JR
       JL
       JJR
       JJL
       JJC

    Mastering a few more commands greatly increases the complexity of what you can do within the text editor.
    Several commands enable you to justify text. Specify the JL (justify left) command to
    left justify, the JR (justify right) command to right justify, and the JC (justify center)
    command to center text. To justify blocks of text, use the JJL, JJR, and JJC commands. For example, if you want to center the following t

    scripting

       store    * disabled in all future editors (load and store are critical instructions)
       zoom z
       up 2
       down 4
       CAPS on/off
       home
       cursor
       curpos
       nums on/off
       %let
       vt
       pmenu off /# functon key #/
       pmenu on
       end
       print
       submit
       unmark unmark all
       tabs
       redo
       undo cntrl z
       nums on/off
       keys
       fse
       fsv sashelp.class
       fsb

       libn
       filen
       dir
       vt
       print
       copy profile.it.source profile.it1.source


