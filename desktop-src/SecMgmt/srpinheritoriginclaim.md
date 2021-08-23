---
description: Essa função usa o atributo Origin se estiver presente do token Origin e os definirá em uma duplicata do token de herança e retornará o token duplicado.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: função srpInheritOriginClaim
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 64436c699f5cb24b2a12675342078242a340fb2e53de3a6a8f3224d8b88beac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004875"
---
# <a name="srpinheritoriginclaim-function"></a>função srpInheritOriginClaim

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Essa função usa o atributo Origin se estiver presente do token Origin e os definirá em uma duplicata do token de herança e retornará o token duplicado. O chamador pode representar o token retornado. Esta função não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a srpapi.dll.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OriginToken* \[ no\]
</dt> <dd>

Identificador para o token que está duplicado e recebe o atributo de origem herdado. Esse identificador deve ser aberto com o \_ direito de acesso duplicado de token.

</dd> <dt>

*InheritingToken* \[ no\]
</dt> <dd>

Identificador para o token que está duplicado e recebe o atributo de origem herdado. Esse identificador deve ser aberto com o \_ direito de acesso duplicado de token. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

Em caso de sucesso, recebe o token duplicado. O chamador pode representá-lo para executar operações com o atributo Origin herdado. O chamador assume a propriedade desse identificador e deve fechá-lo. 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

