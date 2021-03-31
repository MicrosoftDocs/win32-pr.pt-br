---
title: O corpo da interface IDL
description: O corpo da interface IDL contém tipos de dados usados em chamadas de procedimento remoto e os protótipos de função para os procedimentos remotos.
ms.assetid: b07524a7-b27e-4ea2-ae34-068c07d9a444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 565cbe6493bd865030b77b5e9ef6275b444ca451
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641442"
---
# <a name="the-idl-interface-body"></a>O corpo da interface IDL

O corpo da interface IDL contém tipos de dados usados em chamadas de procedimento remoto e os protótipos de função para os procedimentos remotos. O corpo da interface também pode conter importações, pragmas, declarações constantes e declarações de tipo. No modo Microsoft-Extensions, o compilador MIDL também permite declarações implícitas na forma de definições de variáveis.

O exemplo a seguir mostra um arquivo IDL contendo a definição de uma interface. O corpo da definição de interface, que ocorre entre chaves, contém a definição de uma constante (**bufsize**), um tipo (**\_ \_ tipo de identificador PCONTEXT**) e alguns procedimentos remotos (**RemoteOpen**, **RemoteRead**, **RemoteClose** e **Shutdown**).

``` syntax
[ 
  uuid (ba209999-0c6c-11d2-97cf-00c04f8eea45), 
  version(1.0), 
  pointer_default(unique) 
] 
interface cxhndl 
{ 
 
  const short BUFSIZE = 1024;  
 
  typedef [context_handle] void *PCONTEXT_HANDLE_TYPE; 
 
  short RemoteOpen( 
      [out] PCONTEXT_HANDLE_TYPE *pphContext, 
      [in, string] unsigned char *pszFile 
  ); 
 
   short RemoteRead( 
      [in]  PCONTEXT_HANDLE_TYPE phContext, 
      [out] unsigned char achBuf[BUFSIZE], 
      [out] short *pcbBuf 
  ); 
 
  short RemoteClose( [in, out] PCONTEXT_HANDLE_TYPE *pphContext ); 
 
  void Shutdown(void); 
 
}
```

Para obter mais informações, consulte a [referência de linguagem MIDL](/windows/desktop/Midl/midl-language-reference).

 

 