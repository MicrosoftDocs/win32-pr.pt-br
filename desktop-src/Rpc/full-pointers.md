---
title: Ponteiros completos
description: Ao contrário de ponteiros exclusivos, os ponteiros completos dão suporte a aliases.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdbdc223125889eeb1849e60d162e5690b5c307b18b6667d43c578a46282400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021247"
---
# <a name="full-pointers"></a>Ponteiros completos

Ao contrário de ponteiros [exclusivos](unique-pointers.md) , os ponteiros completos dão suporte a aliases. Isso significa que vários ponteiros podem se referir aos mesmos dados, conforme mostrado na figura a seguir:

![dois ponteiros fazendo referência aos mesmos dados](images/prog-a02.png)

Um ponteiro completo tem as seguintes características:

-   Ele pode ter o valor NULL.
-   Ele pode mudar de nulo para não nulo durante a chamada. Quando o valor muda para não nulo, o stub do cliente aloca uma nova memória alocado no retorno. O programa cliente deve liberar essa memória antes de ser encerrado.
-   Ele pode mudar de não nulo para nulo durante a chamada. Quando o valor é alterado para NULL, o aplicativo é responsável por liberar a memória.
-   O valor pode ser alterado de um valor não nulo para outro.
-   O armazenamento que um ponteiro completo aponta para pode ser acessado por outro ponteiro ou nome na operação.
-   Os dados de retorno são gravados no armazenamento existente se o ponteiro não tiver o valor NULL.

Use o \[ atributo [**PTR**](/windows/desktop/Midl/ptr) \] para especificar um ponteiro completo, conforme mostrado no exemplo a seguir:

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

Neste exemplo, os parâmetros *ptrName1* e *ptrName2* são definidos como ponteiros completos para uma cadeia de caracteres. É possível que ambos os ponteiros apontem para o mesmo endereço de memória que contém uma única cadeia de caracteres.

\[**PTR** \] é necessário ao fornecer suporte a alias. No entanto, como ela requer o processamento máximo de todos os ponteiros disponíveis no RPC, ela não é recomendada para a maioria dos aplicativos.

 

 