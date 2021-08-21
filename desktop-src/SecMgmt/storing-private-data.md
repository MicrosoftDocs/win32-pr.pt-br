---
description: A política LSA fornece duas funções que você pode usar para definir e recuperar dados privados.
ms.assetid: 7b6e63d4-ce8f-4279-85d9-da6b2b589afa
title: Armazenando dados privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bfb1d9a701a93a125d68f81d7f487ffc2e2c7a337fa6bec0276086c08ffabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893433"
---
# <a name="storing-private-data"></a>Armazenando dados privados

A política LSA fornece duas funções que você pode usar para definir e recuperar dados privados. Esses dados são armazenados como uma cadeia de caracteres criptografada no registro. Por exemplo, você pode usar essas funções para armazenar senhas de conta de servidor e outras informações confidenciais.

Chame a função [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) para armazenar e criptografar dados privados. Conforme descrito em [Private Data Object](private-data-object.md), os objetos de dados privados incluem três tipos especializados: local, global e computador. Para criar um objeto especializado, adicione um prefixo ao nome da chave passado para **LsaStorePrivateData**: "L $" para objetos locais, "G $" para objetos globais e "M $" para objetos de máquina. Se você não estiver criando um desses tipos especializados, não será necessário especificar um prefixo de nome de chave.

Para recuperar e decodificar dados privados armazenados anteriormente, chame [**LsaRetrievePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaretrieveprivatedata). Observe que você não pode recuperar objetos de dados privados do computador; os objetos de computador podem ser recuperados somente pelo sistema operacional.

Antes de poder armazenar ou recuperar dados privados, seu aplicativo deve obter um identificador para o objeto de [**política**](policy-object.md) local, conforme demonstrado na [abertura de um identificador de objeto de política](opening-a-policy-object-handle.md).

O exemplo a seguir cria um objeto de dados particular local. Observe que a função InitLsaString converte uma cadeia de caracteres [*Unicode*](/windows/desktop/SecGloss/u-gly) em uma estrutura de [**cadeia de \_ \_ caracteres Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . O código para essa função é mostrado em [usando cadeias de caracteres de Unicode LSA](using-lsa-unicode-strings.md).


```C++
#include <windows.h>
#include <stdio.h>

BOOL CreatePrivateDataObject(LSA_HANDLE PolicyHandle)
{
  NTSTATUS ntsResult;
  LSA_UNICODE_STRING lucKeyName;
  LSA_UNICODE_STRING lucPrivateData;
  // The L$ prefix specifies a local private data object
  WCHAR wszKeyName[] = L"L$MyPrivateKey";
  WCHAR wszPrivateData[] = L"Something secret.";

  // Initializing PLSA_UNICODE_STRING structures
  if (!InitLsaString(&lucKeyName, wszKeyName))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }
  if (!InitLsaString(&lucPrivateData, wszPrivateData))
  {
         wprintf(L"Failed InitLsaString\n");
         return FALSE;
  }

  // Store the private data.
  ntsResult = LsaStorePrivateData(
    PolicyHandle,   // handle to a Policy object
    &lucKeyName,    // key to identify the data
    &lucPrivateData // the private data
  );
  if (ntsResult != STATUS_SUCCESS)
  {
    wprintf(L"Store private object failed %lu\n",
      LsaNtStatusToWinError(ntsResult));
    return FALSE;
  }
  return TRUE;
}
```



> [!Note]  
> Os dados armazenados pela função [**LsaStorePrivateData**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsastoreprivatedata) não são absolutamente protegidos. No entanto, a chave tem uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) que permite que apenas o criador e os administradores leiam os dados.

 

 

 
