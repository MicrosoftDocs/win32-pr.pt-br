---
description: As constantes a seguir formam o conjunto de comandos válidos do dispositivo de hardware WIA (Windows Image Acquisition).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandos do dispositivo WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827163"
---
# <a name="wia-device-commands"></a>Comandos do dispositivo WIA

As constantes a seguir formam o conjunto de comandos válidos do dispositivo de hardware WIA (Windows Image Acquisition).



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
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Faz com que o minidriver do dispositivo sincronize itens em cache com o dispositivo de hardware. Se o dispositivo der suporte ao método <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , emitir esse comando fará com que o minidriver descarte os resultados da análise e redefina o item para seu estado inicial. Todos os drivers devem dar suporte a esse comando.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Faz com que um dispositivo WIA adquira uma imagem.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Informa ao dispositivo para excluir todos os itens que podem ser excluídos da árvore de objetos <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> que representam o dispositivo. A exclusão do item é impedida pela definição das propriedades do item. Para obter detalhes, consulte <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> e <a href="-wia-property-attributes.md">atributos de propriedade</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Usado para scanners de documento. Faz com que o verificador carregue a próxima página em seu manipulador de documentos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Usado para scanners de documento. Instrui o dispositivo a descarregar todas as páginas restantes em seu manipulador de documentos. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Usado para scanners de documento que têm um alimentador de página. Instrui o dispositivo a iniciar o motor do alimentador. Esse recurso está disponível a partir do Windows 8.<br/>
<blockquote>
[!Note]<br />
O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Usado para scanners de documento que têm um alimentador de página. Instrui o dispositivo a parar o motor do alimentador. Esse recurso está disponível a partir do Windows 8.<br/>
<blockquote>
[!Note]<br />
O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <strong>WIA_IPS_FEEDER_CONTROL</strong> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Usado para scanners de documento que têm um alimentador de página. Instrui o dispositivo a pausar o motor do alimentador. Esse recurso está disponível a partir do Windows 8.<br/>
<blockquote>
[!Note]<br />
O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <strong>WIA_IPS_FEEDER_CONTROL</strong> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
