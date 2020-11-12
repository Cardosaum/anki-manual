Opções do Baralho
===================

As opções do baralho são acessadas selecionando o baralho na tela principal e
clicando no botão "Opções" no canto inferior da tela.

O Anki permite que você compartilhe opções entre vários baralhos, para fazer com
que o processo de atualizar opções de muitos baralhos ao mesmo tempo se torne
uma tarefa mais fácil. Para fazer isso, opções são agrupadas em "grupo de
opções". Por padrão, todos os baralhos recém criados usam o mesmo grupo de
opções, e baralhos importados de versões antigas do Anki possuem grupo de opções
separados. Se você deseja alterar as configurações de um baralho específico sem
que afete outros, clique no ícone de engrenagem no canto direito e adicione um
novo grupo de opções. O ícone de engrenagem pode ser encontrado na tela
principal, do lado direito do nome do baralho que você deseja alterar. Para
criar um novo grupo de opções, primeiro clique no ícone de engrenagem. Depois,
em "Opções", e então no botão "Gerenciar…". Finalmente, clique no botão
"Adicionar" para criar um novo grupo de opções.
 
Por favor, mude apenas as opções que você de fato entende o que fazem, uma vez
que ajustes inapropriados podem fazer com que o Anki se torne menos eficiente.

Opções não tem efeiro retroativo. Por exemplo, se você mudar uma opção que
controla o intervalo depois que você errar um cartão, cartões que você errou
antes dessa mudança ainda terão o intervalo antigo, e não o novo.

Cartões Novos
-------------

**Passos** controla o número de repetições de aprendizagem, e o intervalo entre
elas. Por favor, veja a seção [aprendizagem](studying.md#aprendizagem) para um
resumo de como os passos de revisão funcionam.

Passos maiores que um dia (1440 minutos) também são suportados - se você quiser,
você pode definir um intervalo como 10 minutos, 1 dia, 3 dias, e finalmente 7
dias antes de que o cartão seja considerado um cartão de revisão.

Se não houver mais nada para estudar, por padrão, o Anki mostrará
antecipadamente cartões com um intervalo de até 20 minutos. Esse intervalo de 20
minutos pode ser configurado em [preferências](preferences.md). Uma coisa a se
estar atento é que, nesse caso, a contagem de cartões devidos será diferente
entre a tela principal, que mostra todos os baralhos, e a tela de estudo de um
baralho específico. Isso é feito para que você tenha uma visão de quais baralhos
precisam de maior atenção.

O Anki trata de uma forma diferente intervalos curtos e longos (aqueles que
viram o dia). Em intervalos curtos, os cartões são mostrados tão logo o
intervalo tenha passado, colocando-os à frente de outros cartões de revisão.
Isso é feito para que você possa responder o cartão o mais próximo possível do
intervalo agendado. Em contraste, cartões que viram o dia são agendados com base
em um agendamento diário, assim como cartões de revisão são tratados. Quando
você retornar para estudar no dia seguinte, a lista de cartões de aprendizagem
diários não será mostrada primeiro, uma vez que isso pode fazer a primeira
metade da seção de revisões consideravelmente difícil e frustrante. Eles são
incluídos na contagem de revisões ao invés de na contagem de aprendizagem devido
a forma que são lidados internamente pelo Anki.

**Ordem** controla como o Anki deve adicionar novos cartões aos baralhos: de
forma aleatória ou ordenada. Quando você muda essa opção, o Anki irá reordenar
os baralhos usando a nova opção de grupo. Uma observação quanto ao modo
aleatório: se você revisar muitos dos seus cartões novos e então adicionar mais
cartões novos, o material recém adicionado é estatisticamente mais provável de
aparecer que os materiais adicionados anteriormente. Para corrigir isso, você
pode mudar a ordem para o modo ordenado e retornar novamente para o modo
aleatório. Dessa forma, você forçará que o Anki reordene (ou, nesse caso,
reembaralhe) a lista de cartões novos.

Quando você seleciona a ordem aleatória, o Anki randomizará suas notas, mantendo
os cartões de uma mesma nota agrupados. Os cartões de uma mesma nota são
mostrados na ordem que seus tipos de cartão aparecem, de forma que cartões
irmãos são introduzidos de forma consistente - caso contrário, você poderia
acabar em um estado no qual algumas notas tiveram todos os seus cartões
introduzidos e outras tiveram apenas um ou dois. Por favor, veja a opção
"ocultar cartões relacionados" abaixo para mais informações.

**New cards/day** tells Anki how many new cards you’d like introduced on
each day you open the program. Missed days will not cause the cards to
pile up. The limit applies to the current deck and subdecks. This means
if "French" has a limit of 20 cards and "French::Lesson 1" and
"French::Lesson 2" both have limits of 15 cards, you’ll get 15 cards
from lesson 1 but only 5 cards from lesson 2.

Studying new cards will temporarily increase the number of reviews you
need to do a day, as freshly learnt material needs to be repeated a
number of times before the delay between repetitions can increase
appreciably. If you are consistently learning 20 new cards a day, you
can expect your daily reviews to be roughly about 200 cards/day. You can
decrease the reviews required by introducing fewer new cards each day,
or by turning off new card display until your review burden decreases.
More than one Anki user has excitedly studied hundreds of new cards over
their first few days of using the program, and then become overwhelmed
by the reviews required.

**Graduating interval** is the delay between answering 'Good' on a card
with no steps left, and seeing the card again.

**Easy interval** is the delay between answering 'easy' on a learning
card and seeing it in review mode for the first time.

**Starting ease** controls the easiness that cards start out with. It is
set when a card graduates from learning for the first time. It defaults
to 250%, meaning that once you’ve finished learning a card, answering
"Good" on subsequent reviews will increase the delay by approximately
2.5x (eg if the last delay was 10 days, the next delay would be 25
days). Based upon how you rate the card in subsequent reviews, the
easiness may increase or decrease from what it starts out as.

Turning off **bury related…​** will prevent Anki from [burying
siblings](studying.md#siblings-and-burying), and instead Anki will just try to avoid showing
siblings directly after one another in the same session. For this to
work, your new cards/day setting needs to be large enough for the cards
of multiple notes to be included.

Reviews
-------

**Maximum reviews/day** allows you to set an upper limit on the number
of reviews to show each day. When this limit is reached, Anki will not
show any more review cards for the day, even if there are some waiting.
If you study consistently, this setting can help to smooth out
occasional peaks in due card counts, and can save you from a heart
attack when returning to Anki after a week off. When reviews have been
hidden due to this option, a message will appear in the congratulations
screen, suggesting you consider increasing the limit if you have time.

**Easy bonus** allows you to set the difference in intervals between
answering 'Good' and 'Easy' on a card. For instance, with the default
value of 130%, Easy will give an interval that is 1.3 times the Good
interval.

**Interval modifier** allows you to apply a multiplication factor to the
intervals Anki generates. At its default of 100% it does nothing; if you
set it to 80% for example, intervals will be generated at 80% of their
normal size (so a 10 day interval would become 8 days). You can thus use
the multiplier to make Anki present cards more or less frequently than
it would otherwise, trading study time for retention or vice versa.

For moderately difficult material, the average user should find they
remember approximately 90% of mature cards that come up for review. You
can find out your own performance by opening the graphs/statistics for a
deck and looking at the Answer Buttons graph - mature retention is the
correct% on the right side of the graph. If you haven’t been studying
long you may not have any mature cards yet. As performance with new
cards and younger cards can vary considerably, it’s a good idea to wait
until you have a reasonable amount of mature reviews before you start
drawing conclusions about your retention rate.

On the SuperMemo website, they suggest that you can find an appropriate
multiplier for a desired retention rate. Their formula boils down to:

    log(desired retention%) / log(current retention%)

Imagine we have a current retention rate of 85% and we want to increase
it to 90%. We’d calculate the modifier as:

    log(90%) / log(85%) = 0.65

You can use Google to [calculate
it](https://www.google.com/search?q=log(90%25)+%2F+log(85%25)) for you.

If you plug the resulting 65% into the interval modifier, you should
find over time that your retention moves closer to your desired
retention.

One important thing to note however is that the tradeoff between time
spent studying and retention is not linear: we can see here that to
increase our retention by 5 percentage points, we’d have to study 35%
more frequently. If the material you are learning is very important then
it may be worth the extra effort – that’s something you’ll need to
decide for yourself. If you’re simply worried that you’re forgetting too
much, you may find investing more time into the initial learning stage
and/or making mnemonics gives you more gain for less effort.

One final thing to note is that Anki forces a new interval to be at
least 1 day longer than it was previously so that you don’t get stuck
reviewing with the same interval forever. If your goal is to repeat a
card once a day for multiple days, you can do that by setting more
learning mode steps instead of by adjusting this modifier.

**Maximum interval** allows you to place an upper limit on the time Anki
will wait to reshow a card. The default is 100 years; you can decrease
this to a smaller number if you’re willing to trade extra study time for
higher retention.

**Hard interval** specifies what the next interval will be when you
press the Hard button. The percentage is relative to the previous
interval, eg with a default 120%, a card with a 10 day interval will be
given 12 days. This option is only available when the experimental
scheduler is enabled in the preferences.

Turning off **bury related…​** will prevent Anki from [burying
siblings](studying.md#siblings-and-burying), and instead Anki will just try to avoid showing
siblings directly after one another in the same session.

Review cards are always shown in random order. If you wish to see them
in a different order, you can use a [filtered deck](filtered-decks.md). More
specifically, Anki randomizes reviews by grabbing batches of 50 cards in
the order that they exist in the database, randomizing each batch, then
putting them together. This means that there is a slight bias towards
older cards being shown first, but it prevents individual cards from
showing up in a predictable order.

Lapses
------

When you forget a review card, it is said to have 'lapsed'. The default
behaviour for lapsed reviews is to reset the interval to 1 (ie, make it
due tomorrow), and put it in the learning queue for a refresher in 10
minutes. This behaviour can be customized with the options listed below.

If you leave the steps blank, Anki will not place the card back in the
learning queue, and it will be rescheduled as a review with its new
interval determined by the settings below.

The new interval is determined when you answer "Again" to a review card,
not when the card finishes its relearning steps. For this reason, the
"Good" and "Easy" buttons during relearing do not alter the interval
again - they only control which step you are on. If there is only a
single step (the default), the "Easy" button will be hidden, since it
would accomplish the same thing as the "Good" button. If you have 2 or
more steps, "Easy" is not hidden, to allow you to graduate cards from
the queue before all of their steps are finished.

'New interval' controls how much Anki should reduce the previous
interval. It reduces the previous interval to the percentage you
specify. If a card had a 200 day interval, the default of 0% would
reduce the interval to 0 (but see the next option). If you set this
option to 50%, the card would have its interval reduced to 100 days
instead.

'Minimum interval' allows you to apply a minimum limit to the above
option. The default setting says that lapses should be reviewed one day
later. The interval must be 1 day or more.

The leech options control the way Anki handles leeches. Please see the
leech section for more information.

General
-------

Anki monitors how long it takes you to answer each question so that it
can show you how long was spent studying each day. The time taken does
not influence scheduling. If you take longer than 60 seconds, Anki
assumes you have walked away from your computer or have been distracted,
and limits the recorded time to 60 seconds, so that you don’t end up
with inaccurate statistics. The 'ignore answer times…​' option allows
you to adjust the cutoff threshold. The minimum cutoff is 30 seconds.

If 'show answer timer' is checked, Anki will display the current time
taken for each card in the study area.

By default, Anki automatically plays audio on the front and back of
cards. If you uncheck 'automatically play audio', Anki will not play
audio until you press the replay audio key, `r` or `F5`.

The 'when answer shown, replay both question and answer audio' option
controls what happens when you choose to replay audio while the answer
is shown. Please note that it does not control what happens when you
show the answer; for that please see [this section](templates/fields.md#special-fields).

Description
-----------

This section allows you to edit the deck description, which is shown in
the study overview. The description is automatically set when
downloading shared decks. You can delete all the text in the description
if you no longer want to see it in the study overview area.

You can also use HTML in the description—anything that works on a note
should be valid.
