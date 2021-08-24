---
description: determina se o Terminal Server está no modo de instalação (somente no Terminal do Windows Server 4,0).
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
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654206"
---
# <a name="ctxgetinimapping-function"></a>Função CtxGetIniMapping

\[Essa função não tem suporte e não deve ser usada. Ele pode mudar ou desaparecer completamente sem aviso prévio. Em vez disso, use **VerifyVersionInfo**.\]

determina se o Terminal Server está no modo de instalação (somente no Terminal do Windows Server 4,0).

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

 

 
