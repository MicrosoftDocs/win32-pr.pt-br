---
title: Estilos de controle da barra de progresso (CommCtrl. h)
description: Os seguintes estilos de controle têm suporte dos controles de barra de progresso
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750938"
---
# <a name="progress-bar-control-styles"></a>Estilos de controle da barra de progresso

Os seguintes estilos de controle têm suporte dos controles de [barra de progresso](progress-bar-control.md) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <dt><strong>PBS_MARQUEE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 6,0</a> ou posterior. O indicador de progresso não aumenta em tamanho, mas, em vez disso, é movido repetidamente ao longo do comprimento da barra, indicando a atividade sem especificar a proporção do progresso concluída. <br/>
<blockquote>
[!Note]<br />
O Comctl32.dll versão 6 não é redistribuível, mas está incluído no Windows ou posterior. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte <a href="cookbook-overview.md">habilitando estilos visuais</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <dt><strong>PBS_SMOOTH</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 4,70</a> ou posterior. A barra de progresso exibe o status de progresso em uma barra de rolagem suave em vez da barra segmentada padrão. <br/>
<blockquote>
[!Note]<br />
Esse estilo só tem suporte no tema clássico do Windows. Todos os outros temas substituem esse estilo.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <dt><strong>PBS_SMOOTHREVERSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 6,0</a> ou posterior e <strong>Windows Vista.</strong> Determina o comportamento da animação que a barra de progresso deve usar ao mover para trás (de um valor mais alto para um valor mais baixo). Se estiver definido, uma &quot; &quot; transição suave ocorrerá, caso contrário, o controle &quot; saltará &quot; para o valor mais baixo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <dt><strong>PBS_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Versão 4,70</a> ou posterior. A barra de progresso exibe o status de progresso verticalmente, de baixo para cima.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Você pode definir estilos de barra de progresso, da mesma forma que outros controles comuns, com [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)ou [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

