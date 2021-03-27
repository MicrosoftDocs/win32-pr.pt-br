---
description: Veja a seguir informações sobre as opções a serem consideradas ao personalizar os blocos de aplicativos da área de trabalho para o Windows 8, incluindo como projetar blocos de aplicativos de área de trabalho para a nova tela inicial e como escolher quais pontos de entrada mostrar na tela inicial.
ms.assetid: EF5182A2-09B2-46F2-B55E-4BD212CC1F7F
title: Blocos de aplicativo de desktop na tela inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fcc5475732926300e2125ae9e97ea2d188bc468
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104297845"
---
# <a name="desktop-app-tiles-on-the-start-screen"></a>Blocos de aplicativo de desktop na tela inicial

Veja a seguir informações sobre as opções a serem consideradas ao personalizar os blocos de aplicativos da área de trabalho para o Windows 8, incluindo como projetar blocos de aplicativos de área de trabalho para a nova tela inicial e como escolher quais pontos de entrada mostrar na tela inicial.

## <a name="design-your-tile-for-the-start-screen"></a>Criar seu bloco para a tela inicial

Você pode personalizar dois aspectos de seus blocos de aplicativo de área de trabalho: o nome do aplicativo e o ícone. A cor do plano de fundo é derivada da cor de fundo escolhida pelo usuário e não é personalizável de forma programática.

![Diretrizes de design de bloco do aplicativo.](images/tiles-desktop-1.png)

DO: Evite o truncamento do nome do aplicativo. Blocos de área de trabalho fixados na tela inicial podem acomodar até duas linhas de texto cada linha ou cerca de dez caracteres (embora isso dependa do idioma da interface do usuário), portanto, tente manter o nome do aplicativo curto o suficiente para evitar truncamento.

FAZER: forneça ícones para os quatro valores de escala de tela inicial com suporte para garantir que os ícones pareçam nítidos em todos os fatores forma.



| Escala | Tamanho do bloco (em pixels) | Tamanho do ícone usado (em pixels) |
|-------|-----------------------|----------------------------|
| 80%   | 120 x 120             | 48 x 48                    |
| 100%  | 150 x 150             | 64 x 64                    |
| 140%  | 210 x 210             | 96 x 96                    |
| 180%  | 270 x 270             | 128 x 128                  |



 

FAZER: adote os princípios de design da Microsoft. A nova aparência dos ícones é simples, portanto, se você quiser imitar os ícones de aplicativos da Windows Store para seu aplicativo de desktop, considere tirar sombras e assim por diante.

Não: não evite o uso da cor. Embora os ícones de aplicativos da Windows Store sejam, às vezes, monodesvios, recomendamos o uso de ícones de cores para aplicativos de desktop. Isso ajuda a diferenciar aplicativos de desktop na barra de tarefas e de outros blocos de aplicativos de área de trabalho na tela inicial, pois a cor do plano de fundo dos blocos da área de trabalho não pode ser personalizada. Considere o uso de cores mais saturadas.

## <a name="decide-the-right-entry-points-to-include-in-the-start-screen"></a>Decidir os pontos de entrada certos a serem incluídos na tela inicial

FAZER: adicionar um atalho por aplicativo na tela inicial quando o aplicativo for instalado. Isso garante que as pessoas possam iniciar seu aplicativo diretamente na tela inicial ou por meio de pesquisa. Se você não incluir um atalho na tela iniciar, seu aplicativo ficará difícil de iniciar. Em particular, não adicione um atalho somente na área de trabalho. Os usuários veem a tela inicial ao fazer logon pela primeira vez e, portanto, colocar um atalho somente na área de trabalho não é tão eficiente quanto incluí-lo na tela inicial.

![Diagrama que mostra uma grade com um bloco de aplicativo, dimensões e ' Segoe U I Semilight ' para indicar a fonte usada.](images/tiles-desktop-2.png)

Não: não forneça vários atalhos para o mesmo aplicativo. Por exemplo, não têm dois atalhos que iniciam um aplicativo em dois modos diferentes, como um para o Windows Internet Explorer e outro para o Internet Explorer sem Complementos.

FAZER: minimizar o número de blocos que são adicionados como parte da instalação. Considere expor outros pontos de entrada para os aplicativos incorretos. Por exemplo, em vez de incluir um aplicativo de configurações separado com um aplicativo de console, acesse as configurações por meio de um recurso no aplicativo de console.

Não: não coloque atalhos para os seguintes itens na tela inicial:

-   Desinstaladores. Os usuários podem acessar os desinstaladores por meio do item programas no painel de controle.
-   Arquivos de ajuda. Inclua tópicos de ajuda diretamente em seu aplicativo.
-   Opções e configurações do aplicativo. Inclua a interface do usuário para definir as configurações de um aplicativo no aplicativo ou criar um item do painel de controle.
-   Sites da Web. Forneça links apropriados para informações como sites de ajuda e suporte técnico diretamente em seu aplicativo.
-   Assistentes. Os assistentes e outras tarefas de configuração única devem ser iniciados de dentro do aplicativo.

Não: não crie atalhos para recursos ou funcionalidades que possam ser iniciados no próprio aplicativo. Por exemplo, as configurações de idioma podem ser configuradas de qualquer Microsoft Office aplicativo, portanto, é desnecessária também ter um ponto de entrada de configurações de idioma separado na tela inicial.

Não: não crie atalhos para itens que não são arquivos executáveis. Os atalhos que não mapeiam para executáveis, como atalhos que iniciam sites da Web ou arquivos de ajuda, são filtrados da tela inicial.

FAZER: se você instalar um pacote de aplicativos em vez de um único aplicativo, adicione um atalho para cada aplicativo no pacote. Conforme mencionado acima, Evite criar atalhos para a funcionalidade secundária, como informações de ajuda, utilitários e configurações. Essa funcionalidade deve ser incluída no (s) aplicativo (es) relevante (is) do pacote.

FAZER: criar uma pasta de produto de nível único para pacotes que contenham três ou mais blocos. Na exibição de aplicativos da tela inicial, acessível no botão de pesquisa, os aplicativos são agrupados por sua pasta de nível superior. Escolha um nome de pasta descritivo, mas conciso; três palavras ou menos são recomendadas. Lembre-se de que, enquanto a exibição de aplicativos agrupa blocos e mostra o nome da pasta, esse nome não é visível quando um bloco é fixado na tela inicial, portanto, torne seus nomes de bloco suficientemente descritivos.

Não: não crie uma pasta de produto se seu pacote contiver apenas um único atalho. Coloque o atalho na pasta de início de nível superior.

FAZER: ao instalar um pacote de mais de três aplicativos, considere se algum desses aplicativos é para uso secundário e mais irregular e não deve ser fixado na tela inicial. Nesse caso, talvez esses blocos possam ser totalmente removidos, de acordo com as diretrizes acima, e iniciados de dentro de um aplicativo primário. Se você não puder remover os blocos, considere desafixa-los da tela inicial. Dessa forma, os atalhos ainda aparecem na exibição **todos os aplicativos** , mas não sobrecarregam a tela inicial do usuário.

Para criar um atalho adicionar um aplicativo sem fixá-lo na tela iniciar, defina a seguinte propriedade no atalho: System. AppUserModel. StartPinOption = 1. O nome simbólico para 1 é APPUSERMODEL \_ STARTPINOPTION \_ NOPINONINSTALL.

Isso impede que o atalho seja mostrado na tela inicial, mas ainda pode ser visto na exibição **todos os aplicativos** e nos resultados da pesquisa. Somente o usuário pode desafixar os atalhos existentes, portanto, você deve definir essa propriedade durante a instalação ou imediatamente depois de colocar o aplicativo no disco.

Não: não crie um bloco para um host ou tempo de execução para aplicativos, como Silverlight ou Java. Forneça um ponto de entrada para desinstalar a estrutura em Adicionar/remover programas e fornecer qualquer ponto de entrada de configurações no painel de controle.

 

 



