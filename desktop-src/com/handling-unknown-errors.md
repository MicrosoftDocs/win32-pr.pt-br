---
title: Manipulando erros desconhecidos
description: Manipulando erros desconhecidos
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006081"
---
# <a name="handling-unknown-errors"></a>Manipulando erros desconhecidos

É legal retornar um código de status somente da implementação de um método de interface aprovado como legalmente retornado. A falha ao observar essa regra convida a possibilidade de conflito entre valores de código de erro retornados e aqueles aprovados pelo aplicativo. Preste atenção especial a esse possível problema ao propagar códigos de erro de funções que são chamadas internamente.

Os aplicativos que chamam interfaces devem tratar qualquer código de erro desconhecido retornado (em oposição a um código de êxito) como sinônimo de E \_ inesperado. Essa prática de manipulação de códigos de erro desconhecidos é exigida pelos clientes das interfaces e funções definidas COM. Como a prática de programação típica é manipular alguns códigos de erro específicos em detalhes e tratar o restante de forma genérica, esse requisito de manipulação de códigos de erro inesperados ou desconhecidos é facilmente atendido.

É importante lidar com todos os erros possíveis ao chamar um método de interface. Se não for possível fazer isso, o aplicativo falhará, corromperá os dados ou ficará vulnerável a explorações de segurança. O exemplo de código a seguir mostra a maneira recomendada de lidar com erros desconhecidos:


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



A verificação de erro a seguir é frequentemente usada com essas rotinas que não retornam nada especial (além de S \_ OK ou algum erro inesperado):


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

 

 




