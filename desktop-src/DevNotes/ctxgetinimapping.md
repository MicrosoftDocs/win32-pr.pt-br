---
description: Determina se o Terminal Server está no modo de instalação (somente no Windows Terminal Server 4,0).
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: Função CtxGetIniMapping
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 17093303cf0ea74e7efc6a3070c48660083bc491
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749737"
---
# <a name="ctxgetinimapping-function"></a>Função CtxGetIniMapping

\[Essa função não tem suporte e não deve ser usada. Ele pode mudar ou desaparecer completamente sem aviso prévio. Em vez disso, use **VerifyVersionInfo**.\]

Determina se o Terminal Server está no modo de instalação (somente no Windows Terminal Server 4,0).

## <a name="syntax"></a>Sintaxe


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função retornará **false** se o Terminal Server estiver no modo de instalação, **true** se estiver no modo de execução.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 
