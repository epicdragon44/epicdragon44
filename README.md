# OCaml
[Transpile](#typescript) ➡️ TypeScript

```ml
let Daniel_Wei : info = (* I'm a work in progress, actually. *)
```

```ml
let show_me (me: info) : string = match me with
  | Student (school, major, minors) ->
    "Cornell University Computer Science, minoring in UX Design and East Asian Studies"
  | Work work_list 
    -> String.concat ";" ["Instapath YC W19"; "Cornell Design & Tech Initiative"]
  | Fun fun_list 
    -> String.concat ";" ["Kayaking"; "Music Composition"; "Doomscrolling"; "Rewatching Start-Up (the kdrama)"]
  | Social 
    -> "@fromdanielwei15 on twitter, weidaniel15 on linkedin, and danielwei15 on everything else"
  | _ -> "(don't) talk to me about the role functional programming has to play in good frontend web development"
```

# TypeScript
[Compile](#javascript) ➡️ JavaScript

```ts
type Info = 'Student' | 'Work' | 'Fun' | 'Social';

interface Student {
  school: string;
  major: string;
  minors: string[];
}

interface Work {
  workList: string[];
}

interface Fun {
  funList: string[];
}

type Daniel_Wei_Info = Student | Work | Fun | Info;

const show_me = (me: Daniel_Wei_Info): string => {
  switch (me) {
    case 'Student':
      return "Cornell University Computer Science, minoring in UX Design and East Asian Studies";
    case 'Work':
      return "Instapath YC W19;Cornell Design & Tech Initiative";
    case 'Fun':
      return "Kayaking;Music Composition;Doomscrolling;Rewatching Start-Up (the kdrama)";
    case 'Social':
      return "@fromdanielwei15 on twitter, weidaniel15 on linkedin, and danielwei15 on everything else";
    default:
      return "(don't) talk to me about the role functional programming has to play in good frontend web development";
  }
}
```

# JavaScript
[Test](#testing) with Jest & TS

```js
function show_me(me) {
    switch (me) {
        case 'Student':
            return "Cornell University Computer Science, minoring in UX Design and East Asian Studies";
        case 'Work':
            return "Instapath YC W19;Cornell Design & Tech Initiative";
        case 'Fun':
            return "Kayaking;Music Composition;Doomscrolling;Rewatching Start-Up (the kdrama)";
        case 'Social':
            return "@fromdanielwei15 on twitter, weidaniel15 on linkedin, and danielwei15 on everything else";
        default:
            return "(don't) talk to me about the role functional programming has to play in good frontend web development";
    }
}
```

# Testing
[Open Console](#console)

```ts
import { show_me, Daniel_Wei_Info, Student, Work, Fun } from './show_me';

describe('show_me', () => {
  it('returns the correct string for Student', () => {
    const studentInfo: Student = {
      school: 'Cornell University',
      major: 'Computer Science',
      minors: ['UX Design', 'East Asian Studies'],
    };

    expect(show_me(studentInfo)).toBe(
      'Cornell University Computer Science, minoring in UX Design and East Asian Studies',
    );
  });

  it('returns the correct string for Work', () => {
    const workInfo: Work = {
      workList: ['Instapath YC W19', 'Cornell Design & Tech Initiative'],
    };

    expect(show_me(workInfo)).toBe('Instapath YC W19;Cornell Design & Tech Initiative');
  });

  it('returns the correct string for Fun', () => {
    const funInfo: Fun = {
      funList: ['Kayaking', 'Music Composition', 'Doomscrolling', 'Rewatching Start-Up (the kdrama)'],
    };

    expect(show_me(funInfo)).toBe('Kayaking;Music Composition;Doomscrolling;Rewatching Start-Up (the kdrama)');
  });

  it('returns the correct string for Social', () => {
    const socialInfo: Daniel_Wei_Info = 'Social';

    expect(show_me(socialInfo)).toBe(
      '@fromdanielwei15 on twitter, weidaniel15 on linkedin, and danielwei15 on everything else',
    );
  });

  it('returns the correct string for the default case', () => {
    const unknownInfo: Daniel_Wei_Info = 'Unknown';

    expect(show_me(unknownInfo)).toBe(
      "(don't) talk to me about the role functional programming has to play in good frontend web development",
    );
  });
});
```

# Console

```txt
Hi! I'm Daniel Wei!

I study Computer Science at Cornell University, and I'm minoring in UX Design and East Asian Studies.

I've worked at YC companies like Instapath as a designer and frontend engineer, and managed large teams like at Cornell DTI.

In my free time, you'll catch me kayaking, composing music, spending an unhealthy amount of time on Twitter, or re-watching Start-Up in my room.

Follow me places! danielwei.me is my personal site, but you can also catch me on Twitter @danielwei15 and Linkedin as weidaniel15.

If you enjoyed this little chain of links, now try setting up Babel/Rollup/Webpack/Vite to do the same thing on your machine, and you'll start to develop the same love-hate relationship I have with the web development ecosystem soon enough.
```

[![GitHub Trends SVG](https://api.githubtrends.io/user/svg/epicdragon44/langs?time_range=one_year&include_private=True&loc_metric=changed&theme=dark)](https://githubtrends.io)   [![GitHub Trends SVG](https://api.githubtrends.io/user/svg/epicdragon44/repos?time_range=six_months&include_private=True&group=private&theme=dark)](https://githubtrends.io)
