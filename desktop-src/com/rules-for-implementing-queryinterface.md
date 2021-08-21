---
title: Regras para implementação de QueryInterface
description: Regras para implementação de QueryInterface
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0d0df2d0382c670ed6f4a323f55dcdd1b187430282abe6699da186e574e390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047864"
---
# <a name="rules-for-implementing-queryinterface"></a>Regras para implementação de QueryInterface

Há três regras principais que regem a implementação do método [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) em um objeto com:

-   Os objetos devem ter identidade.
-   O conjunto de interfaces em uma instância de objeto deve ser estático.
-   Deve ser possível consultar com êxito qualquer interface em um objeto de qualquer outra interface.

## <a name="objects-must-have-identity"></a>Os objetos devem ter identidade

Para qualquer instância de objeto, uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) com a IID \_ IUnknown sempre deve retornar o mesmo valor de ponteiro físico. Isso permite que você chame **QueryInterface** em duas interfaces e compare os resultados para determinar se eles apontam para a mesma instância de um objeto.

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>O conjunto de interfaces em uma instância de objeto deve ser estático

O conjunto de interfaces acessíveis em um objeto por meio de [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) deve ser estático, não dinâmico. Especificamente, se **QueryInterface** retornar S \_ OK para um determinado IID uma vez, ele nunca deve retornar e \_ nointerface em chamadas subsequentes no mesmo objeto; E se **QueryInterface** retornar e \_ nointerface para um determinado IID, as chamadas subsequentes para a mesma IID no mesmo objeto nunca deverão retornar S \_ OK.

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>Deve ser possível consultar com êxito qualquer interface em um objeto de qualquer outra interface

Ou seja, dado o seguinte código:

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

as seguintes regras se aplicam:

-   Se você tiver um ponteiro para uma interface em um objeto, uma chamada como a seguinte para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para a mesma interface deverá ter sucesso:

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   Se uma chamada para [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para um segundo ponteiro de interface for bem sucedido, uma chamada para **QueryInterface** desse ponteiro para a primeira interface também deverá ser bem sucedido. Se o pB foi obtido com êxito, o seguinte também deve ter êxito:

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   Qualquer interface deve ser capaz de consultar qualquer outra interface em um objeto. Se pB obtiver êxito e você consultar com êxito uma terceira interface (IC) usando esse ponteiro, você também deverá ser capaz de consultar com êxito para IC usando o primeiro ponteiro, pA. Nesse caso, a sequência a seguir deve ter sucesso:

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

Implementações de interface devem manter um contador de referências de ponteiros pendentes para todas as interfaces em um determinado objeto. Você deve usar um **inteiro sem sinal** para o contador.

Se um cliente precisar saber que os recursos foram liberados, ele deverá usar um método em alguma interface no objeto com semânticas de nível superior antes de chamar [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando e implementando IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 