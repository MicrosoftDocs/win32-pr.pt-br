---
title: TS_ATTRID (Textstor. h)
description: O \_ tipo de dados TS ATTRID é usado para identificar um atributo de texto.
ms.assetid: 5e375609-3d3c-4c12-ae05-dcaa70779162
keywords:
- TS_ATTRID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1c40d56f1f8ff3deb59d0dd7664a197a672ade7b2d53beebd8e35ba5de7c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950332"
---
# <a name="ts_attrid"></a>\_ATTRID TS

O tipo de dados **TS \_ ATTRID** é usado para identificar um atributo de texto.


```C++
typedef GUID TS_ATTRID;
```



## <a name="remarks"></a>Comentários

Uma lista de GUIDs predefinidos para TS \_ ATTRID está em tsattrs. h.

Os GUIDs TSATTRID \_ Text \_ VERTICALWRITING e TSATTRID \_ Text \_ Orientation são úteis para que os aplicativos correspondam ao texto de entrada que deve ser corrigido. GUIDs adicionais definidos pelo usuário podem ser criados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                             |
| Redistribuível<br/>          | TSF 1,0 em Windows 2000 Professional<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITextStoreACP:: FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[**ITextStoreACP:: RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrsatposition)
</dt> <dt>

[**ITextStoreACP:: RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreACP:: RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestsupportedattrs)
</dt> <dt>

[**ITextStoreACPSink:: OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onattrschange)
</dt> <dt>

[**ITextStoreAnchor::FindNextAttrTransition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrsatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestAttrsTransitioningAtPosition**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> <dt>

[**ITextStoreAnchor::RequestSupportedAttrs**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestsupportedattrs)
</dt> <dt>

[**ITextStoreAnchorSink::OnAttrsChange**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onattrschange)
</dt> <dt>

[**\_ATTRVAL TS**](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> </dl>

 

 





