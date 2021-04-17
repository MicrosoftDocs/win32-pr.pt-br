---
title: TsViewCookie (Textstor. h)
description: O tipo de dados TsViewCookie identifica uma exibição de contexto.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759977"
---
# <a name="tsviewcookie"></a>TsViewCookie

O tipo de dados **TsViewCookie** identifica uma exibição de contexto.


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>Comentários

Um aplicativo deve fornecer um valor **TsViewCookie** exclusivo para cada exibição que ele cria.

O Gerenciador de TSF obtém esse valor do aplicativo chamando [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) ou [ITextStoreAnchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview). O Gerenciador de TSF usa esse valor para identificar a exibição ao chamar vários métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) ou [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                       |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                             |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP:: GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**ITextStoreAnchor::GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





