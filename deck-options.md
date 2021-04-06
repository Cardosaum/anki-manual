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

**Novos cartões/dia** diz ao Anki quantos cartões novos você gostaria que fossem
introduzidos a cada dia que você abrir o programa. Dias perdidos não farão com
que os cartões acumulem. O limite é aplicado para o baralho atual e também para
os baralhos filhos. Isso significa que, se o baralho "Francês" tem um limite de
20 cartões novos e o baralho "Francês::Aula 1" e "Francês::Aula 2" ambos têm um
limite de 15 cartões, você terá no fim das contas 15 cartões da aula 1 mas
apenas 5 cartões da aula 2.

Estudar cartões novos aumentará temporariamente o número de revisões que você
precisará fazer em um dia, uma vez que o material recém aprendido requer uma
quantidade considerável de revisões antes que o intervalo entre as repetições
aumente de forma significativa. Se você consistentemente aprende 20 cartões
novos em um dia, pode esperar que suas revisões diárias sejam de mais ou menos
200 cartões/dia. Você pode diminuir o número de revisões diárias introduzindo
uma menor quantidade de cartões novos a cada dia, ou até mesmo desabilitando
temporariamente a introdução de cartões novos até que a sua carga diária de
revisões reduza. Mais de um usuário do Anki já estudou de forma bem empolgada
centenas de novos cartões por dia durante seus primeiros dias usando o programa,
mas no decorrer de algumas semanas se encontraram em uma situação insustentável
devido a tantas revisões que deviam fazer por dia.

**Intervalo de graduação** é o intervalo entre responder 'Bom' em um cartão sem
outros passos devidos e vê-lo novamente.

**Intervalo fácil** é o intervalo entre responder 'Fácil' em um cartão de
aprendizagem e vê-lo pela primeira vez como um cartão de revisão.

**Facilidade inicial** controla a facilidade com a qual um cartão inicia. Esse
valor é definido quando um cartão gradua da fase de aprendizagem pela primeira
vez. Por padrão o valor é 250%, o que significa que uma vez que você termine de
aprender um cartão, responder "Bom" em revisões subsequentes irá aumentar o
intervalo por aproximadamente 2.5x (e.g. se o último intervalo foi de 10 dias, o
próximo será de 25). Baseado em como você classifica um cartão em revisões
futuras, a facilidade pode aumentar ou diminuir com relação à facilidade
inicial.

Desabilitar a opção **ocultar cartões relacionados até o próximo dia** impedirá
que o Anki [oculte cartões irmãos](studying.md#irmãos-e-ocultação), e, ao invés
disso, o Anki apenas tentará evitar mostar cartões irmãos um em seguida do outro
na mesma seção. Para isso funcionar, a configuração de quantidade de novos
cartões/dia deve ser grande o suficiente para que cartões da mesma nota sejam
inclusos.

Revisões
-------

**Revisões máximas/dia** permite que você especifique um limite máximo de
revisões mostradas por dia. Quando esse limite é atingido, o Anki não mostrará
nenhum cartão a mais para esse dia, mesmo que ainda existam alguns esperando. Se
você estuda de forma consistente, essa configuração pode ajudar a suavizar picos
ocasionais na quantidade de cartões devidos, e também pode te salvar de um
ataque cardíaco quando você retornar a usar o Anki depois de uma semana de
férias. Quando revisões forem ocultadas devido a esta opção, uma mensagem
aparecerá na janela de parabenização, sugerindo que você aumente o limite diário
caso você tenha tempo disponível.

**Bônus por ser fácil** permite que você especifique a diferença de intervalos
entre responder um cartão como 'Bom' ou 'Fácil'. Por exemplo, com a configuração
padrão de 130%, 'Fácil' resultará em um intervalo que é 1.3 vezes o intervalo de
se responder o cartão como 'Bom'.

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
