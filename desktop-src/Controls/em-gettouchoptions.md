---
title: Mensagem de EM_GETTOUCHOPTIONS (RichEdit. h)
description: Recupera as opções de toque associadas a um controle de edição rico.
ms.assetid: 1D367818-5625-4A5A-A7A1-330FED516990
keywords:
- Controles de EM_GETTOUCHOPTIONS de mensagens do Windows
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
ms.openlocfilehash: 812d37de1972c6da205944d9913dc3fa046c205d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009607"
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

## <a name="return-value"></a>Retornar valor

Retorna o valor da opção especificada pelo parâmetro *wParam* . Ele será diferente de zero se *wParam* for **RTO \_** e os garras de toque ficarão visíveis; zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETtouchoptions**](em-settouchoptions.md)
</dt> </dl>

 

 





