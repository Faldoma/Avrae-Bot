<print>
Dice Examples
!r 2d20kh1 - Roll a d20 with advantage. 
!r 4d6kh3 - 4d6 drop lowest stat rolls. 
!r 2d6ro1ro2 - Rerolls 1s and 2s once.
Lookup Features
- Spells, monsters, and status effects from the 5e SRD.
- Configurable option to show a generalization to players when looking up a monster.
- Item and rule lookup in progress.
Initiative Tracking
- Includes HP tracking, status effect tracking, grouping, and combatant notes.
- HP can be hidden from players, showing a generalization instead.
- Can either roll given a modifier or place a combatant at a pre-rolled initiative.
- Status effects have an automatically decreasing turn counter.
Character Sheet Integration
- Avrae can read character sheets from dicecloud or a PDF, automatically generating macros to roll attacks, ability checks, and saving throws.

How to use Avrae - All commands are case-sensitive! Anything in brackets here (e.g. [name]) should be replaced with an argument when calling a command. For example, you would use !spell Fly, not !spell [Fly] or !spell [SPELLNAME].
- Lookup: To lookup a spell, monster, or condition, use !spell [SPELLNAME], !monster [MONSTERNAME], or !condition [CONDITIONNAME]. By default, monster lookups will only display a full statblock if the invoker of the command has the role "Game Master"; this can be configured by using !lookup_settings -req_dm_monster False. Similarly, you can configure the bot to PM the results of the lookup to reduce spam with !lookup_settings -pm_result True.

- Initiative Tracking: To use, first start combat in a channel by saying !init begin.
Then, each combatant should add themselves to the combat with !init add [initiative modifier] [name].
To hide a combatant's HP, add them with !init add [mod] [name] -h.
Once every combatant is added, each combatant should set their max hp with !init hp [name] max [max hp]. Alternatively, you can specify a max HP in the same command as you add a combatant with !init add [mod] [name] --hp [max hp].
Then, you can proceed through combat with !init next.
To add a note to a combatant, use !init note [name] [note].
To add a status effect to a combatant, use !init effect [name] [duration (rounds)] [effect name]. The duration argument is in rounds, for an auto-decrementing counter, or can be set to -1 for an effect with infinite duration. To remove a status effect, use !init re [name] [effect name]. Effects are automatically removed when they reach 0 rounds remaining.
Once combat ends, end combat with !init end.
For more help, the !help command shows applicable arguments for each command.

- Character Sheet Integration: To load a character sheet, simply say !dicecloud [character sheet url]. To load a PDF, go into Discord and upload the sheet as an attachment, with !pdfsheet as the caption. 
Once this is done, you can roll skill checks with !c [skill], saving throws with !save [stat], and attacks with !a [attack name].
</print>
