---
description: Compara dois tokens de acesso e determina se eles são equivalentes em relação a uma chamada para a função AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Função NtCompareTokens (Ntseapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtCompareTokens
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: a763f6f4238632c3bcc736ebacbd2ff133b1955da673a0397ba9a95ebb87c2fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780558"
---
# <a name="ntcomparetokens-function"></a>Função NtCompareTokens

A **função NtCompareTokens** compara dois tokens de acesso e determina se eles são [*equivalentes*](/windows/desktop/SecGloss/a-gly) em relação a uma chamada para a função [**AccessCheck.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck)

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NTAPI NtCompareTokens(
  _In_  HANDLE   FirstTokenHandle,
  _In_  HANDLE   SecondTokenHandle,
  _Out_ PBOOLEAN Equal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FirstTokenHandle* \[ Em\]
</dt> <dd>

Um alça para o primeiro token de acesso a ser comparado. O token deve estar aberto para **acesso \_ TOKEN QUERY.**

</dd> <dt>

*SecondTokenHandle* \[ Em\]
</dt> <dd>

Um alça para o segundo token de acesso a ser comparado. O token deve estar aberto para **acesso \_ TOKEN QUERY.**

</dd> <dt>

*Igual a* \[ out\]
</dt> <dd>

Um ponteiro para uma variável que recebe um valor que indica se os tokens representados pelos parâmetros *FirstTokenHandle* e *SecondTokenHandle* são equivalentes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, a função retornará STATUS \_ SUCCESS.

Se a função falhar, ela retornará um **código de erro NTSTATUS.**

## <a name="remarks"></a>Comentários

Dois tokens de controle de acesso serão considerados equivalentes se todas as seguintes condições são verdadeiras:

-   Cada [*SID (identificador de*](/windows/desktop/SecGloss/s-gly) segurança) presente em qualquer token também está presente no outro token.
-   Nenhum ou ambos os tokens são restritos.
-   Se ambos os tokens são restritos, cada SID restrito em um token também é restrito no outro token.
-   Cada privilégio presente em qualquer token também está presente no outro token.

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Ntseapi.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

