---
description: Compara dois tokens de acesso e determina se eles são equivalentes em relação a uma chamada para a função AccessCheck.
ms.assetid: 3a07ddc6-9748-4f96-a597-2af6b4282e56
title: Função NtCompareTokens (Ntseapi. h)
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
ms.openlocfilehash: d4d0f35bff8fa65e0e09be32a55281b5118f244c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750574"
---
# <a name="ntcomparetokens-function"></a>Função NtCompareTokens

A função **NtCompareTokens** compara dois [*tokens de acesso*](/windows/desktop/SecGloss/a-gly) e determina se eles são equivalentes em relação a uma chamada para a função [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) .

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

*FirstTokenHandle* \[ no\]
</dt> <dd>

Um identificador para o primeiro token de acesso a ser comparado. O token deve estar aberto para acesso de **\_ consulta de token** .

</dd> <dt>

*SecondTokenHandle* \[ no\]
</dt> <dd>

Um identificador para o segundo token de acesso a ser comparado. O token deve estar aberto para acesso de **\_ consulta de token** .

</dd> <dt>

*Igual* \[ a fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe um valor que indica se os tokens representados pelos parâmetros *FirstTokenHandle* e *SecondTokenHandle* são equivalentes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, a função retornará o STATUS \_ êxito.

Se a função falhar, ela retornará um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Dois tokens de controle de acesso são considerados equivalentes se todas as condições a seguir forem verdadeiras:

-   Todo Sid ( [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) ) que está presente em um dos tokens também está presente no outro token.
-   Nem ambos os tokens são restritos.
-   Se ambos os tokens forem restritos, cada SID restrito em um token também será restringido no outro token.
-   Todos os privilégios presentes em um dos tokens também estão presentes no outro token.

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Ntseapi. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

