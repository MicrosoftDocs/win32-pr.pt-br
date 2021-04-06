---
title: Mensagem de SB_SETTEXT (commctrl. h)
description: Define o texto na parte especificada de uma janela de status.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- Controles de SB_SETTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a466187b4ccd00a974b992eacec11938f45001da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086018"
---
# <a name="sb_settext-message"></a>\_Mensagem de SETtext do SB

Define o texto na parte especificada de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) da palavra de ordem inferior Especifica o índice de base zero da parte a ser definida. Se **LOBYTE** for definido como SB \_ simpleid, a janela de status será considerada uma barra de status de modo simples; ou seja, uma barra de status com apenas uma parte.

O [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) da palavra de ordem inferior Especifica o tipo da operação de desenho. Esse parâmetro pode usar um dos valores a seguir.

A palavra de ordem superior de *wParam* é ignorada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>0</strong></dt> </dl></td>
<td>O texto é desenhado com uma borda para aparecer menor do que o plano da janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>O texto é desenhado sem bordas.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>O texto é desenhado pela janela pai. <br/>
<blockquote>
[!Note]<br />
Uma barra de status de modo simples não dá suporte ao desenho de proprietário.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>O texto é desenhado com uma borda para aparecer maior do que o plano da janela.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>O texto será exibido na direção oposta ao texto na janela pai.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>Os caracteres de tabulação são ignorados.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que especifica o texto a ser definido. Se *wParam* for SBT \_ OWNERDRAW, esse parâmetro representará 32 bits de dados. A janela pai deve interpretar os dados e desenhar o texto quando receber a mensagem [**\_ DRAWITEM do WM**](wm-drawitem.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A mensagem invalida a parte da janela que foi alterada, fazendo com que ela exiba o novo texto quando a janela recebe a próxima mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) .

Texto de exibição normal do Windows da esquerda para a direita (EPD). O Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que são lidos da direita para a esquerda (RTL). Se SBT \_ RTLREADING for definido, a cadeia de caracteres *lParam* lerá na direção oposta do texto na janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ SETTEXTW** (Unicode) e **SB \_ settexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SB \_ GETtext**](sb-gettext.md)
</dt> </dl>

 

