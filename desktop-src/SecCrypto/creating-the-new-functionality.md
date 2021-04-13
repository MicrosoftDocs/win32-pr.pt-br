---
description: As funções a seguir estão entre as funções de CryptoAPI que podem ser estendidas.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Criando a nova funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501550"
---
# <a name="creating-the-new-functionality"></a>Criando a nova funcionalidade

As funções a seguir estão entre as funções de CryptoAPI que podem ser estendidas.



| Função CryptoAPI                                   | Definição de nome da função de OID                         | Cadeia de nome da função de OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | objeto de codificação de OID cript. \_ \_ \_ \_ Func<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | \_objeto de \_ decodificação de OID cript \_ . \_<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | \_identificação de \_ Prov aberto do \_ repositório de \_ OID cript \_<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | \_identificação da \_ CTL de verificação de OID cript \_ \_ . \_<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | \_ \_ \_ FUNCde verificar revogação de OID \_ cript<br/> | "CertDllVerifyRevocation" |



 

No uso normal com um OID e um tipo de codificação existentes, o código na função CryptoAPI, em si, é usado. Se uma dessas funções for chamada com um tipo de OID e codificação que o código na função CryptoAPI não foi projetado para manipular, uma nova função, contendo a nova funcionalidade, deverá ser criada em uma DLL. Essa DLL deve ser registrada no registro ou instalada na memória.

Quando uma das funções listadas é chamada com o OID e o tipo de codificação designados recentemente, o código na nova DLL é usado em vez do código fornecido como parte da função CryptoAPI.

O nome da função desenvolvida recentemente pode ser o nome listado em "cadeia de nome da função OID" na tabela anterior ou um nome diferente pode ser fornecido quando o novo código de função é registrado.

A nova função deve usar um protótipo apropriado. Em todos os casos, exceto para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), esse protótipo é o mesmo que a função CryptoAPI que chama a nova função. No caso do **CertOpenStore** , o protótipo é o seguinte.


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> Se os protótipos não corresponderem, a pilha do sistema será corrompida.

 

Além de fornecer o código para a nova função em uma DLL, estender a funcionalidade de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ou [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requer uma definição de tipo para que a nova estrutura de dados C seja colocada em um arquivo de cabeçalho incluído quando o programa do usuário é compilado.

 

 




