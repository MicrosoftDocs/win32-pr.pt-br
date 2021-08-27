---
title: Estilos estendidos da barra de ferramentas (CommCtrl. h)
description: Esta seção lista os estilos estendidos com suporte pelos controles da barra de ferramentas.
ms.assetid: da31dbbf-8d0a-4711-a1af-382c62e653cd
topic_type:
- apiref
api_name:
- TBSTYLE_EX_DRAWDDARROWS
- TBSTYLE_EX_HIDECLIPPEDBUTTONS
- TBSTYLE_EX_DOUBLEBUFFER
- TBSTYLE_EX_MIXEDBUTTONS
- TBSTYLE_EX_MULTICOLUMN
- TBSTYLE_EX_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e242426269d4049b913a41910d325c360886f3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476772"
---
# <a name="toolbar-extended-styles"></a>Estilos estendidos da barra de ferramentas

Esta seção lista os estilos estendidos com suporte pelos controles da barra de ferramentas.




| Constante | Descrição | 
|----------|-------------|
| <span id="TBSTYLE_EX_DRAWDDARROWS"></span><span id="tbstyle_ex_drawddarrows"></span><dl><dt><strong>TBSTYLE_EX_DRAWDDARROWS</strong></dt></dl> | <a href="common-control-versions.md">Versão 4,71</a>. Esse estilo permite que os botões tenham uma seta suspensa separada. Os botões que têm o estilo de <a href="toolbar-control-and-button-styles.md"><strong>BTNS_DROPDOWN</strong></a> serão desenhados com uma seta suspensa em uma seção separada, à direita do botão. Se a seta for clicada, somente a parte de seta do botão será pressionado e o controle Toolbar enviará um <a href="tbn-dropdown.md">TBN_DROPDOWN</a> código de notificação para solicitar que o aplicativo exiba o menu suspenso. Se a parte principal do botão for clicada, o controle Toolbar enviará uma mensagem WM_COMMAND com a ID do botão. Normalmente, o aplicativo responde iniciando o primeiro comando no menu.<br /> Há muitas situações em que você talvez queira ter apenas alguns dos botões suspensos em uma barra de ferramentas com setas separadas. Para fazer isso, defina o TBSTYLE_EX_DRAWDDARROWS estilo estendido. Dê a esses botões que não terão setas separadas <a href="toolbar-control-and-button-styles.md"><strong>BTNS_WHOLEDROPDOWN</strong></a> estilo. Os botões com esse estilo terão uma seta exibida ao lado da imagem. No entanto, a seta não será separada e, quando qualquer parte do botão for clicada, o controle da barra de ferramentas enviará um <a href="tbn-dropdown.md">TBN_DROPDOWN</a> código de notificação. Para evitar problemas de repintura, esse estilo deve ser definido antes que o controle da barra de ferramentas fique visível.<br /> | 
| <span id="TBSTYLE_EX_HIDECLIPPEDBUTTONS"></span><span id="tbstyle_ex_hideclippedbuttons"></span><dl><dt><strong>TBSTYLE_EX_HIDECLIPPEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Versão 5,81</a>. Esse estilo oculta os botões parcialmente recortados. O uso mais comum desse estilo é para barras de ferramentas que fazem parte de um controle rebar. Se uma faixa adjacente abranger parte de um botão, o botão não será exibido. No entanto, se a faixa Rebar tiver o estilo de <a href="/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa"><strong>RBBS_USECHEVRON</strong></a> , o botão será exibido no menu suspenso da divisa. <br /> | 
| <span id="TBSTYLE_EX_DOUBLEBUFFER"></span><span id="tbstyle_ex_doublebuffer"></span><dl><dt><strong>TBSTYLE_EX_DOUBLEBUFFER</strong></dt></dl> | <a href="common-control-versions.md">Versão 6</a>. Esse estilo requer que a barra de ferramentas seja duplamente armazenada em buffer. O buffer duplo é um mecanismo que detecta quando a barra de ferramentas foi alterada. <br /><blockquote>[!Note]<br />o Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows ou posterior. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.</blockquote><br /> | 
| <span id="TBSTYLE_EX_MIXEDBUTTONS"></span><span id="tbstyle_ex_mixedbuttons"></span><dl><dt><strong>TBSTYLE_EX_MIXEDBUTTONS</strong></dt></dl> | <a href="common-control-versions.md">Versão 5,81</a>. Esse estilo permite que você defina o texto para todos os botões, mas só o exiba para esses botões com o estilo de botão <a href="toolbar-control-and-button-styles.md"><strong>BTNS_SHOWTEXT</strong></a> . O estilo de <a href="toolbar-control-and-button-styles.md"><strong>TBSTYLE_LIST</strong></a> também deve ser definido. Normalmente, quando um botão não exibe texto, seu aplicativo deve manipular <a href="tbn-getinfotip.md">TBN_GETINFOTIP</a> ou <a href="ttn-getdispinfo.md">TTN_GETDISPINFO</a> para exibir uma dica de ferramenta. Com o TBSTYLE_EX_MIXEDBUTTONS estilo estendido, o texto definido, mas não exibido em um botão, será automaticamente usado como texto de dica de ferramenta do botão. Seu aplicativo só precisa manipular TBN_GETINFOTIP ou TTN_GETDISPINFO se precisar de mais flexibilidade para especificar o texto da dica de ferramenta. <br /> | 
| <span id="TBSTYLE_EX_MULTICOLUMN"></span><span id="tbstyle_ex_multicolumn"></span><dl><dt><strong>TBSTYLE_EX_MULTICOLUMN</strong></dt></dl> | <a href="common-control-versions.md">Versão 5,82</a>. <strong>Destinado ao uso interno; Não recomendado para uso em aplicativos.</strong> Esse estilo dá à barra de ferramentas uma orientação vertical e organiza os botões da barra de ferramentas em colunas. Os botões fluem verticalmente até que um botão exceda a altura delimitadora da barra de ferramentas (consulte <a href="tb-setboundingsize.md"><strong>TB_SETBOUNDINGSIZE</strong></a>) e uma nova coluna seja criada. A barra de ferramentas flui os botões dessa maneira até que todos os botões sejam posicionados. Para usar esse estilo, o estilo de TBSTYLE_EX_VERTICAL também deve ser definido. <br /><blockquote>[!Note]<br />Esse estilo pode não ter suporte em versões futuras do Comctl32.dll. Além disso, esse estilo não é definido em commctrl. h. Adicione a seguinte definição aos arquivos de origem do seu aplicativo para usar este estilo: <code>#define TBSTYLE_EX_MULTICOLUMN 0x00000002</code></blockquote><br /> | 
| <span id="TBSTYLE_EX_VERTICAL"></span><span id="tbstyle_ex_vertical"></span><dl><dt><strong>TBSTYLE_EX_VERTICAL</strong></dt></dl> | <a href="common-control-versions.md">Versão 5,82</a>. <strong>Destinado ao uso interno; Não recomendado para uso em aplicativos.</strong> Esse estilo dá à barra de ferramentas uma orientação vertical. Os botões da barra de ferramentas fluem de cima para baixo em vez de horizontalmente. <br /><blockquote>[!Note]<br />Esse estilo pode não ter suporte em versões futuras do Comctl32.dll. Além disso, esse estilo não é definido em commctrl. h. Adicione a seguinte definição aos arquivos de origem do seu aplicativo para usar este estilo: <code>#define TBSTYLE_EX_VERTICAL 0x00000004</code></blockquote><br /> | 




## <a name="remarks"></a>Comentários

Para definir um estilo estendido, envie o controle Toolbar a uma mensagem de [**TB \_ Extended**](tb-setextendedstyle.md) . Para determinar quais estilos estendidos estão atualmente definidos, envie uma mensagem de [**TB \_ Extended**](tb-getextendedstyle.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





