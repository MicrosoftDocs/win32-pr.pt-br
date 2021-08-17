---
description: as constantes a seguir especificam o tipo de item de aquisição de imagem de Windows (WIA).
ms.assetid: 7961f692-088a-4f3b-84e9-5fabb0373c3c
title: Sinalizadores de tipo de item WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaItemTypeAnalyze
- WiaItemTypeAudio
- WiaItemTypeBurst
- WiaItemTypeDeleted
- WiaItemTypeDevice
- WiaItemTypeDisconnected
- WiaItemTypeDocument
- WiaItemTypeFile
- WiaItemTypeFolder
- WiaItemTypeFree
- WiaItemTypeGenerated
- WiaItemTypeHasAttachments
- WiaItemTypeHPanorama
- WiaItemTypeImage
- WiaItemTypeProgrammableDataSource
- WiaItemTypeRemoved
- WiaItemTypeRoot
- WiaItemTypeStorage
- WiaItemTypeTransfer
- WiaItemTypeTwainCapabilityPassThrough
- WiaItemTypeVideo
- WiaItemTypeVPanorama
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 5a1a76792a79321ba909607ec7f514a40dac4da92fbbfc4623f87eb99881aaa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965525"
---
# <a name="wia-item-type-flags"></a>Sinalizadores de tipo de item WIA

as constantes a seguir especificam o tipo de item de aquisição de imagem de Windows (WIA).



| Constante                                                                                                                                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WiaItemTypeAnalyze"></span><span id="wiaitemtypeanalyze"></span><span id="WIAITEMTYPEANALYZE"></span><dl> <dt>**WiaItemTypeAnalyze**</dt> </dl>                                                                             | Este item dá suporte ao método [**IWiaItem:: AnalyzeItem**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem) . *essa constante não é suportada pelo* Windows Vista *e posterior.*<br/>                                                                                                                               |
| <span id="WiaItemTypeAudio"></span><span id="wiaitemtypeaudio"></span><span id="WIAITEMTYPEAUDIO"></span><dl> <dt>**WiaItemTypeAudio**</dt> </dl>                                                                                     | O item é um arquivo de áudio. Válido somente para itens que também têm o atributo **WiaItemTypeFile** . <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeBurst"></span><span id="wiaitemtypeburst"></span><span id="WIAITEMTYPEBURST"></span><dl> <dt>**WiaItemTypeBurst**</dt> </dl>                                                                                     | Somente para pastas. As imagens nesta pasta foram executadas em uma sequência de tempo contínua. *essa constante não é suportada pelo* Windows Vista *e posterior.*<br/>                                                                                                                                       |
| <span id="WiaItemTypeDeleted"></span><span id="wiaitemtypedeleted"></span><span id="WIAITEMTYPEDELETED"></span><dl> <dt>**WiaItemTypeDeleted**</dt> </dl>                                                                             | O item é marcado como excluído da árvore. <br/>                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeDevice"></span><span id="wiaitemtypedevice"></span><span id="WIAITEMTYPEDEVICE"></span><dl> <dt>**WiaItemTypeDevice**</dt> </dl>                                                                                 | O item representa um dispositivo conectado. <br/>                                                                                                                                                                                                                                               |
| <span id="WiaItemTypeDisconnected"></span><span id="wiaitemtypedisconnected"></span><span id="WIAITEMTYPEDISCONNECTED"></span><dl> <dt>**WiaItemTypeDisconnected**</dt> </dl>                                                         | O item representa um dispositivo desconectado. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeDocument"></span><span id="wiaitemtypedocument"></span><span id="WIAITEMTYPEDOCUMENT"></span><dl> <dt>**WiaItemTypeDocument**</dt> </dl>                                                                         | O item representa um documento. *essa constante é suportada apenas pelo* Windows Vista *e posterior.*<br/>                                                                                                                                                                                        |
| <span id="WiaItemTypeFile"></span><span id="wiaitemtypefile"></span><span id="WIAITEMTYPEFILE"></span><dl> <dt>**WiaItemTypeFile**</dt> </dl>                                                                                         | O item é um arquivo. <br/>                                                                                                                                                                                                                                                                   |
| <span id="WiaItemTypeFolder"></span><span id="wiaitemtypefolder"></span><span id="WIAITEMTYPEFOLDER"></span><dl> <dt>**WiaItemTypeFolder**</dt> </dl>                                                                                 | O item é uma pasta. <br/>                                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeFree"></span><span id="wiaitemtypefree"></span><span id="WIAITEMTYPEFREE"></span><dl> <dt>**WiaItemTypeFree**</dt> </dl>                                                                                         | O item não foi inicializado ou foi excluído. <br/>                                                                                                                                                                                                                                        |
| <span id="WiaItemTypeGenerated"></span><span id="wiaitemtypegenerated"></span><span id="WIAITEMTYPEGENERATED"></span><dl> <dt>**WiaItemTypeGenerated**</dt> </dl>                                                                     | Este item foi criado pelo aplicativo ou pelo driver e não tem um item correspondente na árvore de itens de driver. <br/>                                                                                                                                                               |
| <span id="WiaItemTypeHasAttachments"></span><span id="wiaitemtypehasattachments"></span><span id="WIAITEMTYPEHASATTACHMENTS"></span><dl> <dt>**WiaItemTypeHasAttachments**</dt> </dl>                                                 | O item tem anexos de arquivo. *essa constante não é suportada pelo* Windows Vista *e posterior.*<br/>                                                                                                                                                                                          |
| <span id="WiaItemTypeHPanorama"></span><span id="wiaitemtypehpanorama"></span><span id="WIAITEMTYPEHPANORAMA"></span><dl> <dt>**WiaItemTypeHPanorama**</dt> </dl>                                                                     | O item representa uma imagem panorâmica horizontal. *essa constante não é suportada pelo* Windows Vista *e posterior.*<br/>                                                                                                                                                                       |
| <span id="WiaItemTypeImage"></span><span id="wiaitemtypeimage"></span><span id="WIAITEMTYPEIMAGE"></span><dl> <dt>**WiaItemTypeImage**</dt> </dl>                                                                                     | O item é um arquivo de imagem. Válido somente para itens que também têm o atributo **WiaItemTypeFile** . <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeProgrammableDataSource"></span><span id="wiaitemtypeprogrammabledatasource"></span><span id="WIAITEMTYPEPROGRAMMABLEDATASOURCE"></span><dl> <dt>**WiaItemTypeProgrammableDataSource**</dt> </dl>                 | O item representa uma fonte de dados programável. *essa constante é suportada apenas pelo* Windows Vista *e posterior.*<br/>                                                                                                                                                                        |
| <span id="WiaItemTypeRemoved"></span><span id="wiaitemtyperemoved"></span><span id="WIAITEMTYPEREMOVED"></span><dl> <dt>**WiaItemTypeRemoved**</dt> </dl>                                                                             | O item foi removido do dispositivo. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeRoot"></span><span id="wiaitemtyperoot"></span><span id="WIAITEMTYPEROOT"></span><dl> <dt>**WiaItemTypeRoot**</dt> </dl>                                                                                         | Identifica o item raiz na árvore do dispositivo de objetos de item. *essa constante é suportada apenas pelo* Windows Vista *e posterior.*<br/>                                                                                                                                                         |
| <span id="WiaItemTypeStorage"></span><span id="wiaitemtypestorage"></span><span id="WIAITEMTYPESTORAGE"></span><dl> <dt>**WiaItemTypeStorage**</dt> </dl>                                                                             | O item representa um meio de armazenamento. <br/>                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeTransfer"></span><span id="wiaitemtypetransfer"></span><span id="WIAITEMTYPETRANSFER"></span><dl> <dt>**WiaItemTypeTransfer**</dt> </dl>                                                                         | O item pode ser transferido. <br/>                                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeTwainCapabilityPassThrough"></span><span id="wiaitemtypetwaincapabilitypassthrough"></span><span id="WIAITEMTYPETWAINCAPABILITYPASSTHROUGH"></span><dl> <dt>**WiaItemTypeTwainCapabilityPassThrough**</dt> </dl> | Esse tipo indica que o dispositivo WIA é capaz de receber dados de capacidade de TWAIN da camada de compatibilidade TWAIN. Se esse tipo for definido, qualquer recurso de TWAIN que não seja compreendido pela camada de compatibilidade TWAIN, durante uma sessão TWAIN, será passado para o driver WIA. <br/> |
| <span id="WiaItemTypeVideo"></span><span id="wiaitemtypevideo"></span><span id="WIAITEMTYPEVIDEO"></span><dl> <dt>**WiaItemTypeVideo**</dt> </dl>                                                                                     | O item representa vídeo de streaming. *essa constante não é suportada pelo* Windows Server 2003 *,* Windows Vista *ou posterior.*<br/>                                                                                                                                                      |
| <span id="WiaItemTypeVPanorama"></span><span id="wiaitemtypevpanorama"></span><span id="WIAITEMTYPEVPANORAMA"></span><dl> <dt>**WiaItemTypeVPanorama**</dt> </dl>                                                                     | O item representa uma imagem panorâmica vertical. *essa constante não é suportada pelo* Windows Vista *e posterior.*<br/>                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




