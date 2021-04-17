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
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761854"
---
# <a name="srpinheritoriginclaim-function"></a>função srpInheritOriginClaim

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

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

## <a name="return-value"></a>Retornar valor

Se essa função for bem sucedido, ela retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

