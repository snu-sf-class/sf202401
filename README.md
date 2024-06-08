# Software Formal Verification, SNU M1522.007300, 2024 Spring

- Instructor: Prof. [Chung-Kil Hur](http://sf.snu.ac.kr/gil.hur)
    + Email address: gil.hur@sf.snu.ac.kr
    + Office: 302-426
- TA: [Jaewoo Kim](http://sf.snu.ac.kr/jaewoo.kim)
    + Email address: sf@sf.snu.ac.kr
        * When sending TA an email,
            * The subject (제목) must start with [SF]
            * Your name and student ID must be included in the body (본문)
    + Office: 302-317
- Class material: http://www.cis.upenn.edu/~bcpierce/sf/current/index.html
- Please use email to ask questions (Do not use GitHub Issues)

## Announcements

- Jun. 8: Assignment 5 result is uploaded (see eTL). Claims : until **Jun 13**.
- Jun. 4: 6월 6일에는 수업이 없습니다.
- Jun. 1: Assignment 6 is uploaded.
- May. 30: Assignment 4 result is uploaded (see eTL). Claims : until **Jun 6**.
- May. 24: Assignment 5 is uploaded.
- May. 23: Final exam : Jun. 16 (14:00 - 18:00). The instruction will soon be uploaded.
- May. 20: Assignment 3 result is uploaded (see eTL). Claims : until Jun 2.
- May. 16: Assignment 4 is uploaded.
- May. 15: Midterm result is uploaded. Claims : until May 28.
- May. 9: 금일 수업은 휴강입니다.
- Apr. 30: Assignment 3 is uploaded.
- Apr. 22: Assignment 2 result is uploaded. Claims : until May 6.
- Apr. 18: Midterm exam date is changed: May. 11 (Sat) (14:00-18:00). See [instruction](https://github.com/snu-sf-class/sf202401/blob/main/MidtermInstruction.md).
- Apr. 16: ~~Midterm exam : Apr. 28 (19:00 - 23:00)~~.
- Apr. 8: Assignment 1 result is uploaded. Claims : until Apr 21.
- Apr. 6: Assignment 2 is uploaded. Before solving the problems, check if `git push` works properly for the assignment.
- Mar. 28: Issue for errata is made. Please check [errata](https://github.com/snu-sf-class/sf202401/issues/2) regularly. (Issue Latest Update : **May 30**)
- Mar. 21: Assignment 1 is uploaded.
- Mar. 19: Assignment 0 is uploaded. If you have trouble signing-in GitLab page or cloning repo, contact TA through email.

## Assignments

**Check errata (in Issues) regularly!**

**Check again that your code compiles without error (using `make`) before submission.**

- Replace `FILL_IN_HERE` with your code in P**.v.
- If you can't complete a proof, just put `Abort.` after `Proof.` (Do not use `admit.`, `Admitted`, etc.)
- Please check `README` file of each assignment.
- **Each assignment has forbidden keywords in forbidden.txt. Do not use those keywords.**
- **Assignment with dependencies is scored using default skeleton file as dependencies in server. So, using custom definitions in different files is not allowed.**
- ~~Try to finish your proof in one proof environment. Write additional 'Lemma' is not recommended. Use 'assert' tactic instead.~~ It is okay to use auxiliary lemmas in the proof.
- Visit [Homework Repo](http://gl.kinetc.net:20105) and log-in with ID `<student_id>_sf2401` (e.g. 2016-12345_sf2401). Your initial password is `XAXBXCX1010XX`. Change your PW immidiately!
- Try to push something to the Homework Repo as soon as the assignment is open. Do not postpone checking `git push` until the last minute.
- If you forget your password, email to ta(sf@sf.snu.ac.kr).
- No delayed submission.
- Claims: see the claim date for each assignment/exam.

| Due        	         | Description                   	 	 	 	 	 	 	 	 	 	 	 	 	 	    |
|------------------------|------------------------------------------------------------------------------------------
| 2024/3/31 23:59:59 KST | Assignment 0 (GitLab Test)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|
| 2024/4/5 23:59:59 KST  | Assignment 1 (Basic, Induction)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|
| 2024/4/19 23:59:59 KST  | Assignment 2 (Lists - Logic)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|
| 2024/5/14 23:59:59 KST  | Assignment 3 (IndProp - Imp)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|
| 2024/5/29 23:59:59 KST  | Assignment 4 (Equiv - Hoare)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|
| 2024/6/7 23:59:59 KST  | Assignment 5 (Hoare2 - HoareasLogic)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|
| 2024/6/14 23:59:59 KST  | Assignment 6 (Smallstep - MoreStlc)          	 	 	 	 	 	 	 	 	 	 	 	 	 	|

## Grading(tentative)
- Attendance: 5%
- Assignments: 25%
- Mid-term: 30%
- Final: 40%

## Coq

- Install Coq [8.18.0](https://coq.inria.fr).
    + Using an installer (Windows, MacOS)
        * Download [Binaries](https://coq.inria.fr/download) and install it.
        * Using Coq in Windows could have unexpected, unsupported problem. TA cannot help you in this case.

    + Using OPAM (Linux / MacOS) (recommended)
        * OPAM is OCaml package manager, and you can use it to install Coq in Linux.
        * See [https://coq.inria.fr/opam-using.html](https://coq.inria.fr/opam-using.html).

    + Using brew (MacOS)
        * Run `brew install coq`.
        * Note this wouldn't install CoqIDE.

- Install IDE for Coq.
    + CoqIDE: installed by default.
    + VS Code: [VSCoq](https://github.com/coq-community/vscoq/tree/vscoq1). Follow the setup instructions.
        * In this semester, we will use VS Code as default IDE.
        * VsCoq v2.x is new and shows unstableness. If you have trouble using VsCoq v2, downgrade to VsCoq Legacy (v0.3.9).
        * Basic command (based on vscoq github page)
            * ```alt + down``` : interpret next step
            * ```alt + up``` : return to previous step
            * ```alt + right``` : interpret to right before cursor
            * ```alt + end``` : interpret until end of file
            * ```alt + home``` : reset
            * more commands : ```F1``` & type ```Coq:```
                * example : ```Coq: Prompt Check```
    + Emacs: [Company-Coq](https://github.com/cpitclaudel/company-coq). Follow the setup instructions.
        * If it shows `Searching for program No such file or directory coqtop` error, please add `(custom-set-variables '(coq-prog-name "PATH/TO/coqtop"))` to `.emacs` file.
        * In case of MacOS, coqtop is at `/Applications/CoqIDE_8.9.1.app/Contents/Resources/bin/`.

- Tips for those using Windows
    + Using [WSL](https://learn.microsoft.com/ko-kr/windows/wsl/install) allows you work on linux.
    + In WSL, [WSL extension of VS Code](https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode) is recommended.

- It is likely that you will use your own laptop in mid-term and final exam. If you do not have a laptop or cannot install Coq on it, please let the TA know.

## Tactics

- You can look up manuals about [Basic tactics](https://coq.inria.fr/doc/V8.18.0/refman/proofs/writing-proofs/index.html), [Automatic solver](https://coq.inria.fr/refman/proofs/automatic-tactics/index.html), and [Ltac](https://coq.inria.fr/refman/proof-engine/ltac.html) for more information about proof techniques.

#### Honor Code: *DO NOT CHEAT*
- Do not copy others' source code, including other students' and resources around the web. Especially, do not consult with public repositories on software foundations.
- Assignment score will be adjusted with the exam score. See above.
