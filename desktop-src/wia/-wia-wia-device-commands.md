---
description: as constantes a seguir formam o conjunto de comandos de dispositivo de hardware WIA (aquisição de imagem Windows) válidos.
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
ms.openlocfilehash: 08aeb26502686d2550d872bcfa845e3c68230ac4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467103"
---
# <a name="wia-device-commands"></a>Comandos do dispositivo WIA

as constantes a seguir formam o conjunto de comandos de dispositivo de hardware WIA (aquisição de imagem Windows) válidos.




| Constante | Descrição | 
|----------|-------------|
| <span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt></dl> | Faz com que o minidriver do dispositivo sincronize itens em cache com o dispositivo de hardware. Se o dispositivo der suporte ao método <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , emitir esse comando fará com que o minidriver descarte os resultados da análise e redefina o item para seu estado inicial. Todos os drivers devem dar suporte a esse comando.<br /> | 
| <span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt></dl> | Faz com que um dispositivo WIA adquira uma imagem.<br /> | 
| <span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt></dl> | Informa ao dispositivo para excluir todos os itens que podem ser excluídos da árvore de objetos <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> que representam o dispositivo. A exclusão do item é impedida pela definição das propriedades do item. Para obter detalhes, consulte <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> e <a href="-wia-property-attributes.md">atributos de propriedade</a>.<br /> | 
| <span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt></dl> | Usado para scanners de documento. Faz com que o verificador carregue a próxima página em seu manipulador de documentos.<br /> | 
| <span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt></dl> | Usado para scanners de documento. Instrui o dispositivo a descarregar todas as páginas restantes em seu manipulador de documentos. <br /> | 
| <span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl><dt><strong>WIA_CMD_START_FEEDER</strong></dt></dl> | Usado para scanners de documento que têm um alimentador de página. Instrui o dispositivo a iniciar o motor do alimentador. Esse recurso está disponível a partir de Windows 8.<br /><blockquote>[!Note]<br />O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 
| <span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt></dl> | Usado para scanners de documento que têm um alimentador de página. Instrui o dispositivo a parar o motor do alimentador. Esse recurso está disponível a partir de Windows 8.<br /><blockquote>[!Note]<br />O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <strong>WIA_IPS_FEEDER_CONTROL</strong> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 
| <span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt></dl> | Usado para scanners de documento que têm um alimentador de página. Instrui o dispositivo a pausar o motor do alimentador. Esse recurso está disponível a partir de Windows 8.<br /><blockquote>[!Note]<br />O minidriver WIA deve rejeitar esse comando e retornar <strong>WIA_ERROR_INVALID_COMMAND</strong> quando a propriedade <strong>WIA_IPS_FEEDER_CONTROL</strong> não for suportada ou estiver definida como WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
