---
title: Sobre os controles de calendário mensal
description: Um controle de calendário mensal implementa uma interface de usuário do tipo calendário.
ms.assetid: 81b8f233-272e-4043-92ff-5ff47b0610d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f61b0ffc291473b330469910d1dad0317668e1
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084932"
---
# <a name="about-month-calendar-controls"></a>Sobre os controles de calendário mensal

Um controle de calendário mensal implementa uma interface de usuário do tipo calendário. Isso fornece ao usuário um método muito intuitivo e reconhecível de inserir ou selecionar uma data. O controle também fornece ao aplicativo os meios para obter e definir as informações de data no controle usando tipos de dados existentes.

-   [Recursos de controle de calendário mensal](#month-calendar-control-features)
    -   [Selecionando um dia](#selecting-a-day)
    -   [Selecionando um mês não adjacente](#selecting-a-nonadjacent-month)
    -   [Selecionando um ano diferente](#selecting-a-different-year)
-   [Localização](#localization)
-   [Vezes no controle de calendário mensal](#times-in-the-month-calendar-control)

## <a name="month-calendar-control-features"></a>Recursos de controle de calendário mensal

A captura de tela a seguir mostra um controle de calendário mensal que foi dimensionado para mostrar dois meses.

![captura de tela de uma caixa de diálogo com um controle de calendário mensal mostrando dois meses, lado a lado](images/mc-simple.png)

> [!Note]  
> A aparência e o comportamento do controle de calendário mensal difere ligeiramente em diferentes versões da biblioteca de tempo de execução. Este tópico se concentra no controle como ele aparece no Windows Vista com a versão 6 do Comctl32.dll.

 

O controle na ilustração tem os seguintes recursos opcionais.

-   A data atual é mostrada em uma linha separada na parte inferior do controle. Este é o estilo padrão.
-   O "círculo atual" (na verdade, um retângulo nesta versão) aparece em torno do dia atual e ao lado da linha "hoje" como uma indicação visual. Este é o estilo padrão.
-   Os números da semana são mostrados à esquerda de cada linha de dias. Esse estilo deve ser especificado.
-   Algumas datas são mostradas em negrito, de acordo com o estado do dia definido pelo aplicativo. Por exemplo, as datas que têm reuniões agendadas podem ser mostradas em negrito. Esse estilo deve ser especificado.

> [!Note]
>
> O Windows não oferece suporte a datas anteriores a 1601. Consulte [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) para obter detalhes.
>
> O controle mês-Calendar é baseado no calendário gregoriano, que foi introduzido em 1753. Ele não calculará as datas consistentes com o calendário juliano que estava em uso antes de 1753.

 

### <a name="selecting-a-day"></a>Selecionando um dia

Por padrão, quando um usuário clica nos botões de seta na parte superior esquerda ou superior direita do controle de calendário mensal, o controle atualiza sua exibição para mostrar o mês anterior ou o próximo. O usuário também pode executar a mesma ação clicando nos meses parciais exibidos antes do primeiro mês e depois do último mês.

Os comandos de teclado a seguir também podem ser usados para mover a seleção. O calendário sempre rola conforme necessário para exibir o dia selecionado. (Os [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes) são mostrados na tabela.)



|                         |                                                                                                                                                                                                                                          |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Seta para a esquerda (VK \_ esquerda)   | Selecione o dia anterior.                                                                                                                                                                                                                 |
| Seta para a direita (VK \_ direita) | Selecione o dia seguinte.                                                                                                                                                                                                                     |
| Seta para cima (VK \_ up)       | Selecione o mesmo dia na semana anterior.                                                                                                                                                                                                |
| Seta para baixo (VK \_ down)   | Selecione o mesmo dia na próxima semana.                                                                                                                                                                                                    |
| PAGE UP (VK \_ anterior)     | Selecione o mesmo dia no mês anterior. (Se esse mês não tiver o dia, o dia mais próximo será selecionado; por exemplo, a seleção passará de 31 de março para 28 de fevereiro ou 29.)                                                      |
| PAGE DOWN (VK \_ Avançar)    | Selecione o mesmo dia no mês seguinte.                                                                                                                                                                                                   |
| Página inicial (VK \_ Home)         | Selecione o primeiro dia do mês atual.                                                                                                                                                                                               |
| FIM (VK \_ end)           | Selecione o último dia do mês atual.                                                                                                                                                                                                |
| CTRL + PÁGINA INICIAL             | Role um mês para trás e selecione um dia na coluna mais à esquerda.                                                                                                                                                                       |
| CTRL + FIM              | Role um mês para frente e selecione um dia na coluna mais à direita.                                                                                                                                                                       |
| CTRL + PAGE UP          | Selecione o mesmo dia em um mês anterior. O número de meses pelos quais a seleção é movida é o número de meses exibidos no controle. Por exemplo, se dois meses forem exibidos, a seleção mudaria de 6 de junho para 6 de maio.    |
| CTRL + PAGE DOWN        | Selecione o mesmo dia em um mês anterior. O número de meses pelos quais a seleção é movida é o número de meses exibidos no controle. Por exemplo, se dois meses forem exibidos, a seleção mudaria de 6 de junho para 6 de agosto. |



 

Se um controle de calendário mensal não estiver usando o estilo [**MCS \_ nohoje**](month-calendar-control-styles.md) , o usuário poderá retornar ao dia atual clicando no texto "hoje" na parte inferior do controle. Se o dia atual não estiver visível, o controle atualizará sua exibição para mostrá-lo.

Um aplicativo pode alterar o número de meses pelos quais o controle atualiza sua exibição usando a mensagem [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) ou a macro correspondente, [**calendário mensal \_ SETMONTHDELTA**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta). No entanto, as teclas PAGE UP e PAGE DOWN alteram o mês selecionado em uma, independentemente do número de meses exibidos ou do valor definido por **MCM \_ SETMONTHDELTA**.

### <a name="selecting-a-nonadjacent-month"></a>Selecionando um mês não adjacente

Quando um usuário clica no nome de um mês exibido, todos os meses do ano são listados (em versões anteriores, esse é um menu pop-up). O usuário pode selecionar um mês na lista. Se a seleção do usuário não estiver visível, o controle de calendário mensal rolará sua exibição para mostrar o mês escolhido. Na captura de tela a seguir, um controle de calendário mensal mostra os meses de dois anos adjacentes.

![captura de tela de uma caixa de diálogo com um controle de calendário mensal mostrando todos os meses de 2007 e 2008](images/mc-months.png)

### <a name="selecting-a-different-year"></a>Selecionando um ano diferente

Se o usuário clicar no ano, um grupo de anos será listado e o usuário poderá selecionar um diferente, conforme mostrado na captura de tela a seguir.

![captura de tela de um controle de calendário mensal mostrando todos os anos de 1999 a 2020](images/mc-years.png)

## <a name="localization"></a>Localização

O controle mês-Calendar obtém seu formato e todas as cadeias de caracteres do padrão de usuário da localidade \_ \_ .

## <a name="times-in-the-month-calendar-control"></a>Vezes no controle de calendário mensal

O controle de calendário mensal não exibe a hora. No entanto, a estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) usada para definir e recuperar a data selecionada ou a data de hoje contém campos de hora. Quando uma data é definida programaticamente, o controle copia os campos de hora como eles são ou os valida primeiro e, se forem inválidos, armazena os horários padrão atuais. A seguir está uma lista das mensagens que definem uma data e uma descrição de como os campos de hora são tratados.



|                                             |                                                                                                                                                                                                                            |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCM \_ SETcurseal**](mcm-setcursel.md)     | O controle copia os campos de hora como estão, sem validação ou modificação.                                                                                                                                        |
| [**\_SETRANGE MCM**](mcm-setrange.md)       | Os campos de hora das estruturas transmitidas são validados. Se eles forem válidos, os campos de tempo serão copiados sem modificação. Se forem inválidos, o controle copiará os campos de hora dos dados atuais.                  |
| [**MCM \_ SETSELRANGE**](mcm-setselrange.md) | Os campos de hora das estruturas transmitidas são validados. Se eles forem válidos, os campos de tempo serão copiados sem modificação. Se forem inválidos, o controle manterá os campos de hora dos intervalos de seleção atuais. |
| [**MCM de \_ hoje**](mcm-settoday.md)       | O controle copia os campos de hora como estão, sem validação ou modificação.                                                                                                                                        |



 

Quando uma data for recuperada do controle, os campos de hora serão copiados dos horários armazenados sem modificação. A manipulação dos campos de tempo pelo controle é fornecida como uma conveniência para o programador. O controle não examina nem modifica os campos de hora como resultado de qualquer operação diferente daquelas listadas acima.

 

 