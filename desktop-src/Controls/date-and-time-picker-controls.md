---
title: Sobre os controles de seletor de data e hora
description: Um controle de data e hora (DTP) fornece uma interface simples e intuitiva por meio da qual as informações de data e hora do Exchange são trocadas por um usuário.
ms.assetid: 6749c3ae-2c52-4183-ac4e-68ca7ebf1e13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182381c40b636683255e95ba0680a1245ef0adf3
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424216"
---
# <a name="about-date-and-time-picker-controls"></a>Sobre os controles de seletor de data e hora

Um *controle de data e hora (DTP)* fornece uma interface simples e intuitiva por meio da qual as informações de data e hora do Exchange são trocadas por um usuário. Por exemplo, com um controle DTP, você pode pedir ao usuário para inserir uma data e recuperar facilmente a seleção.

Os seguintes tópicos são abordados:

-   [Interface do usuário do seletor de data e hora](#date-and-time-picker-user-interface)
-   [Estilos e formatos de controle do seletor de data e hora](#date-and-time-picker-control-styles-and-formats)
    -   [Formatos predefinidos](#preset-formats)
    -   [Formatos personalizados](#custom-formats)
    -   [Cadeias de caracteres de formato](#format-strings)
    -   [Campos de retorno de chamada](#callback-fields)
-   [Mensagens de notificação de controle do seletor de data e hora](#date-and-time-picker-control-notification-messages)
-   [Tópicos relacionados](#related-topics)

> [!Note]
> O Windows não oferece suporte a datas anteriores a 1601. Consulte a estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) para obter detalhes.
>
> O controle é baseado no calendário gregoriano, que foi introduzido em 1753. Ele não calculará as datas consistentes com o calendário juliano.

## <a name="date-and-time-picker-user-interface"></a>Interface do usuário do seletor de data e hora

A área cliente de um controle DTP (data e hora) exibe informações de data ou hora, ou ambas, e atua como a interface por meio da qual os usuários modificam as informações. A data pode ser selecionada em um calendário ou usando um controle acima-abaixo; a hora pode ser alterada digitando-se os campos definidos pelas [cadeias de caracteres de formato](#format-strings)do controle. Opcionalmente, o controle exibe uma caixa de seleção. Quando está marcado, o valor no controle pode ser recuperado; caso contrário, o controle será considerado como não inicializado.

A ilustração a seguir mostra uma janela que contém três controles de selador de data. O primeiro controle selador de data foi criado com o estilo [**DTS \_ SHOWNONE,**](date-and-time-picker-control-styles.md) o segundo com o estilo [**\_ UPDOWN**](date-and-time-picker-control-styles.md) do DTS e o terceiro sem estilos especiais. No terceiro controle, o usuário clicou na seta para baixo para exibir o calendário.

![captura de tela de uma janela que demonstra três estilos de controles de selador de data](images/dtpdatepick.png)

A ilustração a seguir mostra uma janela com três controles que contêm a hora.

O primeiro controle foi criado com o estilo [**\_ TIMEFORMAT do DTS**](date-and-time-picker-control-styles.md) e mostra a hora no tempo padrão, que consiste em quatro campos. O usuário pode digitar um valor válido em qualquer um desses campos ou selecionar o campo e alterar o valor usando as teclas de seta ou controle para cima para baixo.

O segundo controle mostra um formato personalizado definido usando [**DateTime \_ SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat). Assim como no primeiro controle, o usuário pode alterar os campos de tempo digitando ou usando teclas de seta. O dia da semana pode ser alterado selecionando uma data do calendário que é aberta quando o usuário clica na seta para baixo.

O terceiro controle mostra como o texto arbitrário pode ser adicionado ao controle. O usuário pode selecionar uma hora (de 1 a 24) digitando, usando as teclas de direção ou usando o controle para cima para baixo.

![captura de tela de uma janela que mostra três controles que contêm a hora](images/dtpdatetimepick.png)

O controle DTP atualiza automaticamente as informações internas com base na entrada do usuário. O controle reconhece o seguinte como entrada válida.



| Categoria de Entrada | Descrição                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Setas     | O controle aceita teclas de seta para navegar pelos campos no controle e alterar valores. O usuário pode pressionar as teclas ou para mover-se pelo controle Se o usuário tentar passar do último campo em uma determinada direção, o foco do teclado "se envolve" para o campo no lado oposto do controle. As chaves e alteram valores no campo atual incrementalmente. |
| Fim e início   | O controle aceita as \_ chaves virtuais VK end e VK \_ Home para alterar o valor dentro do campo atual para seus limites superior e inferior, respectivamente.                                                                                                                                                                                                                          |
| Teclas de função  | A chave ativa o modo de edição. A chave faz com que o controle exiba um controle de calendário de mês suspenso (pressionar também faz isso).                                                                                                                                                                                                                                          |
| Números        | O controle aceita entrada numérica em segmentos de dois caracteres. Se o valor digitado pelo usuário for inválido (como definir o mês como 14), o controle o rejeitará e redefinirá a exibição para o valor anterior.                                                                                                                                                                |
| Mais e menos | O controle aceita o VK \_ Adicionar e VK \_ subtrair chaves virtuais do teclado numérico para incrementar e decrementar o valor no campo atual.                                                                                                                                                                                                                             |



 

Os controles DTP que não usam o estilo de [**\_ upDown DTS**](date-and-time-picker-control-styles.md) exibem um botão de seta. Se o usuário clicar nesse botão, um controle de calendário mensal cai. O usuário pode selecionar uma data específica clicando em uma área do calendário.

## <a name="date-and-time-picker-control-styles-and-formats"></a>Estilos e formatos de controle do seletor de data e hora

Os controles DTP (data e time Picker) têm vários [estilos de controle seletor de data e hora](date-and-time-picker-control-styles.md) que determinam a aparência e o comportamento de um controle. Especifique o estilo ao criar o controle com o parâmetro *dwStyle* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Para recuperar ou alterar o estilo de janela depois de criar o controle, use [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) e [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

### <a name="preset-formats"></a>Formatos predefinidos

Há três formatos predefinidos disponíveis para exibir a data e outra para exibir a hora. Defina esses formatos escolhendo um dos seguintes estilos de janela.



|   Formatar                                                                                                    |   Descrição                                                         |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [**\_LONGDATEFORMAT Dts**](date-and-time-picker-control-styles.md)                 | A exibição será como: "Sexta-feira, 19 de abril de 1996".      |
| [**DTS \_ SHORTDATEFORMAT**](date-and-time-picker-control-styles.md)               | A exibição terá esta aparência: "19/4/96".                     |
| [**DTS \_ SHORTDATECENTURYFORMAT**](date-and-time-picker-control-styles.md) | **Versão 5.80.** A exibição terá a aparência: "19/4/1996". |
| [**TIMEFORMAT de DTS \_**](date-and-time-picker-control-styles.md)                         | A exibição terá a aparência: "17:31:42".                  |



 

### <a name="custom-formats"></a>Formatos personalizados

Um controle DTP depende de uma cadeia de caracteres de formato para determinar como ele exibirá campos de informações. Se os formatos predefinidos não são suficientes, você pode criar um formato personalizado definindo sua própria cadeia de caracteres de formato. Formatos personalizados fornecem maior flexibilidade para um aplicativo. Eles permitem que você especifique a ordem na qual o controle exibirá campos de informações. Você pode incluir texto do corpo, bem como campos de retorno de chamada para solicitar informações do usuário. Depois que a cadeia de caracteres for criada, atribua-a ao controle DTP com uma [**mensagem \_ SETFORMAT DTM.**](dtm-setformat.md)

### <a name="format-strings"></a>Cadeias de caracteres de formato

Uma cadeia de caracteres de formato DTP consiste em uma série de elementos que representam uma determinada informação e definem seu formato de exibição. Os elementos serão exibidos na ordem em que aparecerem na cadeia de caracteres de formato.

Os elementos de formato de data e hora serão substituídos pela data e hora reais. Eles são definidos pelos seguintes grupos de caracteres.



| Elemento | Descrição                                                                       |
|---------|-----------------------------------------------------------------------------------|
| "d"     | O dia de um ou dois dígitos.                                                        |
| "dd"    | O dia de dois dígitos. Valores de dia de dígito único são precedidos por um zero.                |
| "ddd"   | A abreviação da semana de três caracteres.                                         |
| "dddd"  | O nome completo do dia da semana.                                                            |
| "h"     | A hora de um ou dois dígitos no formato de 12 horas.                                     |
| "hh"    | A hora de dois dígitos no formato de 12 horas. Valores de dígito único são precedidos por um zero. |
| "H"     | A hora de um ou dois dígitos no formato de 24 horas.                                     |
| "HH"    | A hora de dois dígitos no formato de 24 horas. Valores de dígito único são precedidos por um zero. |
| "m"     | O minuto de um ou dois dígitos.                                                     |
| "mm"    | O minuto de dois dígitos. Valores de dígito único são precedidos por um zero.                 |
| “M”     | O número de mês de um ou dois dígitos.                                               |
| "MM"    | O número de mês de dois dígitos. Valores de dígito único são precedidos por um zero.           |
| "MMM"   | A abreviação de mês de três caracteres.                                           |
| "MMMM"  | O nome completo do mês.                                                              |
| "t"     | A abreviação AM/PM de uma letra (ou seja, AM é exibida como "A").              |
| "tt"    | A abreviação AM/PM de duas letras (ou seja, é exibida como "AM").             |
| "yy"    | Os dois últimos dígitos do ano (ou seja, 1996 seriam exibidos como "96").       |
| "yyyy"  | O ano completo (ou seja, 1996 seria exibido como "1996").                       |



 

Para tornar as informações mais acessíveis, você pode adicionar texto de corpo à cadeia de caracteres de formato, entre aspas simples. Espaços e marcas de pontuação não precisam ser entre aspas.

> [!Note]  
> Caracteres não format que não são delimitados por aspas simples resultarão em exibição imprevisível pelo controle DTP.

Por exemplo, para exibir a data atual com o formato "'Today is: 04:22:31 Tuesday 23, 1996", a cadeia de caracteres de formato é "'Today is: 'hh':'m':'s dddd MMM dd', 'yyyy". Para incluir uma aspas simples no texto do corpo, use duas aspas simples consecutivas. Por exemplo, "'Don't forget' MMM dd',' yyyy" produz uma saída que se parece com: Não se esqueça de 23 de março de 1996. Não é necessário usar aspas com a vírgula, portanto, "'Don't forget' MMM dd, yyyy" também é válido e produz a mesma saída.

### <a name="callback-fields"></a>Campos de retorno de chamada

Além do texto padrão [cadeias](#format-strings) de caracteres de formato e corpo, você também pode definir determinadas partes da exibição como campos [de retorno de chamada](#callback-fields). Esses campos podem ser usados para consultar o usuário para obter informações. Para declarar um campo de retorno de chamada, inclua um ou mais caracteres "X" (CÓDIGO ASCII 88) em qualquer lugar na cadeia de caracteres de formato. Você pode criar campos de retorno de chamada que têm uma identidade exclusiva repetindo o caractere "X". Portanto, a cadeia de caracteres de formato "XX dddd MMM dd", "aaa XXX" contém dois campos de retorno de chamada exclusivos, "XX" e "XXX". Assim como outros campos de controle DTP, os campos de retorno de chamada são exibidos na ordem da esquerda para a direita com base em seu local na cadeia de caracteres de formato.

Quando o controle DTP analisar a cadeia de caracteres de formato e encontrar um campo de retorno de chamada, ele enviará códigos de notificação [DTN \_ FORMAT](dtn-format.md) [e DTN \_ FORMATQUERY.](dtn-formatquery.md) O elemento de cadeia de caracteres de formato correspondente ao campo de retorno de chamada é incluído com as notificações para permitir que o aplicativo receptor determine qual campo de retorno de chamada está sendo consultado. O proprietário do controle deve responder a essas notificações para garantir que as informações personalizadas sejam exibidas corretamente.

## <a name="date-and-time-picker-control-notification-messages"></a>Mensagens de notificação de controle do seletor de data e hora

Um controle de data e hora (DTP) envia códigos de notificação quando recebe entrada ou processos do usuário e reage a campos de retorno de chamada. O pai do controle recebe esses códigos de notificação na forma de mensagens [**de \_ notificação do WM**](wm-notify.md) .

Os códigos de notificação a seguir são usados com controles DTP.



| Código de notificação                             | Descrição                                                                                                                                                                                                       |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DTN \_ closeup](dtn-closeup.md)               | Indica que o calendário do mês suspenso está prestes a ser removido.                                                                                                                                               |
| [DTN \_ DATETIMECHANGE](dtn-datetimechange.md) | Sinaliza uma alteração dentro do controle DTP.                                                                                                                                                                          |
| [\_lista suspensa DTN](dtn-dropdown.md)             | Indica que o calendário do mês suspenso está prestes a ser exibido.                                                                                                                                             |
| [\_formato DTN](dtn-format.md)                 | Solicita o texto a ser exibido em uma parte da cadeia de caracteres de formato descrita como um campo de retorno de chamada.                                                                                                                         |
| [DTN \_ FORMATQUERY](dtn-formatquery.md)       | Solicita informações sobre o tamanho máximo permitido do texto a ser exibido em um campo de retorno de chamada.                                                                                                            |
| [DTN \_ userstring](dtn-userstring.md)         | Sinaliza o final da operação de edição de um usuário dentro do controle. Essa notificação é enviada somente por controles DTP que usam o estilo [**DTS \_ APPCANPARSE**](date-and-time-picker-control-styles.md) . |
| [DTN \_ WMKEYDOWN](dtn-wmkeydown.md)           | Sinaliza que o usuário pressionou uma tecla em um campo de retorno de chamada do controle DTP.                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle do selador de data e hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 