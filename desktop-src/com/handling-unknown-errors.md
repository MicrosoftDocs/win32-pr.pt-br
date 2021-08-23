---
title: Tratamento de erros desconhecidos
description: Tratamento de erros desconhecidos
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38fb0e8aaaef8fc3ff4ae9bb76f76a845c325c4b5a5dc4d409dbd0ab35734ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048254"
---
# <a name="handling-unknown-errors"></a>Tratamento de erros desconhecidos

É legal retornar um código de status somente da implementação de um método de interface sancionado como legalmente returnável. A falha ao observar essa regra convida a possibilidade de conflito entre os valores de código de erro retornados e os sancionados pelo aplicativo. Preste atenção especial a esse possível problema ao propagar códigos de erro de funções que são chamadas internamente.

Os aplicativos que chamam interfaces devem tratar qualquer código de erro retornado desconhecido (em vez de um código de êxito) como sinônimo de E \_ UNEXPECTED. Essa prática de lidar com códigos de erro desconhecidos é exigida pelos clientes das interfaces e funções definidas pelo COM. Como a prática de programação típica é lidar com alguns códigos de erro específicos em detalhes e tratar o restante genericamente, esse requisito de lidar com códigos de erro inesperados ou desconhecidos é facilmente atendido.

É importante tratar todos os erros possíveis ao chamar um método de interface. A falha ao fazer isso pode fazer com que seu aplicativo falha, corrompa dados ou se torne vulnerável a explorações de segurança. O exemplo de código a seguir mostra a maneira recomendada de lidar com erros desconhecidos:


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



A verificação de erro a seguir geralmente é usada com as rotinas que não retornam nada especial (diferente de S \_ OK ou algum erro inesperado):


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erro em COM](error-handling-in-com.md)
</dt> </dl>

 

 




