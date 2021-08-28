---
title: Mensagem de EM_SETTOUCHOPTIONS (RichEdit. h)
description: Define as opções de toque associadas a um controle de edição rico.
ms.assetid: C15036D6-B74F-414D-B731-F1587B616644
keywords:
- controles de Windows de mensagem de EM_SETTOUCHOPTIONS
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
ms.openlocfilehash: 4ea2f372d1e59a76ea13667e994534df1088fe1c78c51c30ac54db1b4dfeed2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048006"
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

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETtouchoptions**](em-settouchoptions.md)
</dt> </dl>

 

 





