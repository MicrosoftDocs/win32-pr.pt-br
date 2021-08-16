---
description: O exemplo a seguir fornece informações sobre as opções a considerar ao personalizar blocos de aplicativo da área de trabalho para Windows 8 incluindo como criar blocos de aplicativos da área de trabalho para o novo tela inicial e como escolher quais pontos de entrada mostrar no tela inicial.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Blocos do aplicativo da área de trabalho na tela inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ed35bd5c8405301e872ef54774914d625e1fc06c6a9fc3c26965e130301eac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861210"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Blocos do aplicativo da área de trabalho na tela inicial

O exemplo a seguir fornece informações sobre as opções a considerar ao personalizar blocos de aplicativo da área de trabalho para Windows 8 incluindo como criar blocos de aplicativos da área de trabalho para o novo tela inicial e como escolher quais pontos de entrada mostrar no tela inicial.

## <a name="design-your-tile-for-the-start-screen"></a>Projete o seu tela inicial

Você pode personalizar dois aspectos dos blocos do aplicativo da área de trabalho: o nome do aplicativo e o ícone. A cor da tela de fundo é derivada da cor da tela de fundo escolhida pelo usuário e não é personalizável programaticamente.

![diretrizes de design deile do aplicativo.](images/tiles-desktop-1.png)

DO: evite o truncamento do nome do aplicativo. Os blocos da área de trabalho fixados no tela inicial podem acomodar até duas linhas de texto em cada linha ou cerca de dez caracteres (embora isso dependa do idioma da interface do usuário), portanto, tente manter o nome do aplicativo curto o suficiente para evitar o truncamento.

DO: forneça ícones para os quatro valores tela inicial escala com suporte para garantir que seus ícones pareçam claros em todos os fatores forma.



| Escala | Tamanho do quadrado (em pixels) | Tamanho do ícone usado (em pixels) |
|-------|-----------------------|----------------------------|
| 80%   | 120 x 120             | 48 x 48                    |
| 100%  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

DO: adote os princípios de design da Microsoft. A nova aparência dos ícones é simples, portanto, se você quiser imitar ícones de aplicativo da Windows Store para seu aplicativo da área de trabalho, considere tirar sombras e assim por diante.

NÃO: não evite o uso de cores. Embora Windows ícones de aplicativo da Store às vezes sejam monocromáticos, é recomendável usar ícones de cores para aplicativos da área de trabalho. Isso ajuda a diferenciar aplicativos da área de trabalho na barra de tarefas e de outros blocos de aplicativo da área de trabalho no tela inicial porque a cor da tela de fundo dos blocos da área de trabalho não pode ser personalizada. Considere o uso de cores mais saturadas.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Decida os pontos de entrada certos a incluir no tela inicial

DO: adicione um atalho por aplicativo no tela inicial quando o aplicativo estiver instalado. Isso garante que as pessoas possam iniciar seu aplicativo diretamente do tela inicial ou por meio da pesquisa. Se você não incluir um atalho no tela inicial, seu aplicativo se tornará difícil de iniciar. Em particular, não adicione um atalho somente na área de trabalho. Os usuários veem o tela inicial logon pela primeira vez e, portanto, colocar um atalho somente na área de trabalho não é tão eficaz quanto incluí-lo no tela inicial.

![Diagrama que mostra a grade com um painel de aplicativo, dimensões e 'Segoe U I Semilight' para indicar a fonte usada.](images/tiles-desktop-2.png)

NÃO: não forneça vários atalhos para o mesmo aplicativo. Por exemplo, não há dois atalhos que iniciam um aplicativo em dois modos diferentes, como um para Windows Internet Explorer e outro para Internet Explorer sem complementos.

DO: minimize o número de blocos adicionados como parte da instalação. Considere expor outros pontos de entrada aos aplicativos inadequados. Por exemplo, em vez de incluir um aplicativo Configurações separado com um aplicativo de console, acesse as configurações por meio de um recurso no aplicativo de console.

NÃO: não coloque atalhos para os seguintes itens na tela inicial:

-   Desinstaladores. Os usuários podem acessar desinstaladores por meio do item Programas no Painel de Controle.
-   Arquivos de ajuda. Inclua tópicos de ajuda diretamente em seu aplicativo.
-   Configurações e opções do aplicativo. Inclua a interface do usuário para definir as configurações de um aplicativo dentro do aplicativo ou crie um Painel de Controle item.
-   Sites. Forneça links apropriados para informações como sites de ajuda e suporte técnico diretamente em seu aplicativo.
-   Assistentes. Os assistentes e outras tarefas de configuração única devem ser lançados de dentro do aplicativo.

NÃO: não crie atalhos para recursos ou funcionalidades que podem ser lançados de dentro do próprio aplicativo. Por exemplo, a linguagem Configurações pode ser configurada de qualquer aplicativo Microsoft Office, portanto, também é desnecessário ter um ponto de entrada Configurações language separado no tela inicial.

NÃO: não crie atalhos para itens que não são arquivos executáveis. Atalhos que não são mapeados para executáveis, como atalhos que iniciam sites ou arquivos de ajuda, são filtrados fora do tela inicial.

DO: se você instalar um pacote de aplicativos em vez de um único aplicativo, adicione um atalho para cada aplicativo no pacote. Conforme mencionado acima, evite criar atalhos para a funcionalidade secundária, como informações de ajuda, utilitários e configurações. Essa funcionalidade deve ser incluída nos aplicativos relevantes do pacote.

DO: crie uma pasta de produto de nível único para os suites que contêm três ou mais blocos. Na exibição Aplicativos do tela inicial, acessível no guia Pesquisar, os aplicativos são agrupados por sua pasta de nível superior. Escolha um nome de pasta descritivo, mas conciso; três palavras ou menos são recomendadas. Esteja ciente de que, embora os Aplicativos exibiam blocos e mostrem o nome da pasta, esse nome não fica visível quando um bloco é fixado no tela inicial, portanto, descritivo o suficiente para seus nomes de bloco.

NÃO: não crie uma pasta de produto se o pacote contiver apenas um único atalho. Coloque o atalho na pasta Iniciar de nível superior.

DO: ao instalar um pacote de mais de três aplicativos, considere se qualquer um desses aplicativos é para uso secundário e mais irregular e não deve ser fixado ao tela inicial. Nesse caso, talvez esses blocos possam ser totalmente removidos, de acordo com as diretrizes acima, e lançados de dentro de um aplicativo primário. Se você não puder remover os blocos, considere unpinning-los do tela inicial. Dessa forma, os atalhos  ainda aparecem na exibição Todos os Aplicativos, mas não desorganizam a tela inicial.

Para criar um atalho de aplicativo sem fixá-lo ao tela inicial, defina a seguinte propriedade no atalho: System.AppUserModel.StartPinOption = 1. O nome simbólico para 1 é APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

Isso impede que o atalho seja mostrado no tela inicial, mas ele  ainda pode ser visto na exibição Todos os Aplicativos e nos resultados da pesquisa. Somente o usuário pode desempinar atalhos existentes, portanto, você deve definir essa propriedade durante a instalação ou imediatamente depois de colocar o aplicativo no disco.

NÃO: não crie um lado para um host ou runtime para aplicativos, como Silverlight ou Java. Forneça um ponto de entrada para desinstalar a estrutura em Adicionar/Remover Programas e fornecer qualquer ponto de entrada de configurações Painel de Controle.

 

 



