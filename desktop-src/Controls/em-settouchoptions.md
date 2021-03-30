---
title: Mensagem de EM_SETTOUCHOPTIONS (RichEdit. h)
description: Define as opções de toque associadas a um controle de edição rico.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- Controles de EM_SETTOUCHOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7613679a574955ef726da9fa10e8d919c8fe53b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455343"
---
# <a name="em_settouchoptions-message"></a>\_Mensagem em SETtouchoptions

Define as opções de toque associadas a um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A opção de toque a ser definida. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                        | Significado                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**indisponibilidades de RTO \_**</dt> </dl>          | Mostre ou oculte os identificadores de garra de toque, dependendo do valor de *lParam*.<br/>                                                                                                                                                       |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**\_DISABLEHANDLES RTO**</dt> </dl> | Habilite ou desabilite os identificadores de garra de toque, dependendo do valor de *lParam*. Quando os identificadores estiverem desabilitados, eles ficarão ocultos se estiverem visíveis e permanecerão ocultos até que uma mensagem em **\_ settouchoptions** altere seu status. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Defina como **true** para mostrar/habilitar as alças de seleção de toque ou **false** para ocultar/desabilitar as alças de seleção de toque.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**em \_ GETtouchoptions**](em-settouchoptions.md)
</dt> </dl>

 

 





