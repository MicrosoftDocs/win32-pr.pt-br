---
description: Várias das funções de diretiva LSA usam a \_ estrutura de cadeia de caracteres Unicode LSA \_ para armazenar informações de cadeia de caracteres. Essa estrutura armazena a cadeia de caracteres e suas informações de comprimento.
ms.assetid: 8a02cbb4-0b59-4c1e-9831-592a2005905e
title: Usando cadeias de caracteres de Unicode LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00e5b98bf2e287f32934b4ea093570ba3359ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784133"
---
# <a name="using-lsa-unicode-strings"></a>Usando cadeias de caracteres de Unicode LSA

Várias das funções de diretiva LSA usam a estrutura de [**\_ cadeia de \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) para armazenar informações de cadeia de caracteres. Essa estrutura armazena a cadeia de caracteres e suas informações de comprimento.

O código a seguir implementa uma função que converte dados **LPWSTR** em estruturas de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) :


```C++
#include <windows.h>

bool InitLsaString(
  PLSA_UNICODE_STRING pLsaString,
  LPCWSTR pwszString
)
{
  DWORD dwLen = 0;

  if (NULL == pLsaString)
      return FALSE;

  if (NULL != pwszString) 
  {
      dwLen = wcslen(pwszString);
      if (dwLen > 0x7ffe)   // String is too large
          return FALSE;
  }

  // Store the string.
  pLsaString->Buffer = (WCHAR *)pwszString;
  pLsaString->Length =  (USHORT)dwLen * sizeof(WCHAR);
  pLsaString->MaximumLength= (USHORT)(dwLen+1) * sizeof(WCHAR);

  return TRUE;
}
```



 

 



