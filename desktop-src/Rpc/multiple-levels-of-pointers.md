---
title: Vários níveis de ponteiros
description: Usando vários níveis de ponteiros na RPC (chamada de procedimento remoto).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917521"
---
# <a name="multiple-levels-of-pointers"></a>Vários níveis de ponteiros

Quando há vários níveis de ponteiros, os atributos são associados ao ponteiro mais próximo do nome da variável. O cliente ainda é responsável por alocar qualquer memória associada à resposta.

O exemplo a seguir permite que o stub chame o servidor sem saber antecipadamente a quantidade de dados que será retornada:

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

Neste exemplo, o stub passa o servidor para um ponteiro exclusivo, que o servidor inicializa como **nulo**. Em seguida, o servidor aloca um bloco de barras, define o ponteiro, define o argumento de tamanho e retorna. Observe que, para que o servidor tenha um efeito no chamador, você deve passar um \[ ponteiro de referência \] para um \[ ponteiro [**exclusivo**](/windows/desktop/Midl/unique) \] para seus dados. Observe também que a vírgula em \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is)(, \* psize) \] , que indica que o ponteiro de nível superior não é um ponteiro de tamanho, mas que o ponteiro de nível inferior é.

No lado do cliente, o stub define \* ppBar como **nulo** antes de chamar o procedimento remoto. Em seguida, o stub aloca e desempacota a conjunto de objetos de barra. O argumento size indica o tamanho do bloco (e o número de barras não marshaled). O cliente deve liberar a matriz retornada de objetos de barra quando ela não for mais necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**o tamanho \_ é**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 