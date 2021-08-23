---
title: Mensagem de EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera as opções de toque associadas a um controle de edição rico.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- controles de Windows de mensagem de EM_GETTOUCHOPTIONS
topic_type:
- apiref
api_name:
- EM_GETTOUCHOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4771cd11fd8aaf16925c97a3242918ba8f7b56e4e580a6f3cd70672a134399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799986"
---
# <a name="em_gettouchoptions-message"></a>\_Mensagem em GETtouchoptions

Recupera as opções de toque associadas a um controle de edição rico.


```C++
#define EM_GETTOUCHOPTIONS       (WM_USER + 310)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

As opções de toque a serem recuperadas. Pode ser um dos seguintes valores.



| Valor                                                                                                                                                                        | Significado                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="RTO_SHOWHANDLES"></span><span id="rto_showhandles"></span><dl> <dt>**indisponibilidades de RTO \_**</dt> </dl>          | Recupera se os garras de toque estão visíveis.<br/> |
| <span id="RTO_DISABLEHANDLES"></span><span id="rto_disablehandles"></span><dl> <dt>**\_DISABLEHANDLES RTO**</dt> </dl> | A recuperação desse sinalizador não está implementada.<br/>          |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor da opção especificada pelo parâmetro *wParam* . Ele será diferente de zero se *wParam* for **RTO \_** e os garras de toque ficarão visíveis; zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETtouchoptions**](em-settouchoptions.md)
</dt> </dl>

 

 





