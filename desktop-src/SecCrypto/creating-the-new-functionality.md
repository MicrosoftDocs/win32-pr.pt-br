---
description: As funções a seguir estão entre as funções CryptoAPI que podem ser estendidas.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Criando a nova funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ccd528e7e9cf62896c74de07f042dec0e77a7dba5fe5fee32b9b1e2eb229da7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768861"
---
# <a name="creating-the-new-functionality"></a>Criando a nova funcionalidade

As funções a seguir estão entre as funções CryptoAPI que podem ser estendidas.



| Função CryptoAPI                                   | Definição do nome da função OID                         | Cadeia de caracteres de nome da função OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**Cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | CRYPT \_ OID \_ ENCODE \_ OBJECT \_ FUNC<br/>     | "CryptDllEncodeObject"    |
| [**Cryptdecodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ DECODE \_ OBJECT \_ FUNC<br/>     | "CryptDllDecodeObject"    |
| [**Certopenstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CRYPT \_ OID \_ OPEN \_ STORE \_ PROV \_ FUNC<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ VERIFY \_ CTL \_ USAGE \_ FUNC<br/> | "CertDllVerifyCTLUsage"   |
| [**Certverifyrevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CRYPT \_ OID \_ VERIFY \_ REVOCATION \_ FUNC<br/> | "CertDllVerifyRevocation" |



 

Em uso normal com um tipo de codificação e OID existente, o código na função CryptoAPI, em si, é usado. Se uma dessas funções for chamada com um tipo OID e de codificação que o código na função CryptoAPI não foi projetado para manipular, uma nova função, que contém a nova funcionalidade, deverá ser criada em uma DLL. Essa DLL deve ser registrada no Registro ou instalada na memória.

Quando uma das funções listadas é chamada com o OID e o tipo de codificação recém-designados, o código na nova DLL é usado em vez do código fornecido como parte da função CryptoAPI.

O nome da função recém-desenvolvida pode ser o nome listado em "Cadeia de caracteres de nome da função OID" na tabela anterior ou um nome diferente pode ser dado quando o novo código de função é registrado.

A nova função deve usar um protótipo apropriado. Em todos os casos, exceto [**para CertOpenStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)esse protótipo é o mesmo que a função CryptoAPI que chama a nova função. No caso de **CertOpenStore,** o protótipo é o seguinte.


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

 

Além de fornecer o código para a nova função em uma DLL, estender a funcionalidade de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ou [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requer uma definição de tipo para que a nova estrutura de dados C seja colocada em um arquivo de header incluído quando o programa do usuário é compilado.

 

 




