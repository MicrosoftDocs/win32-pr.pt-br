---
title: Atributos direcional (parâmetro)
description: Os atributos direcionais descrevem se os dados são transmitidos do cliente para o servidor, servidor para cliente ou ambos.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Chamada de procedimento remoto RPC, descrito, atributos direcionais
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084718"
---
# <a name="directional-parameter-attributes"></a>Atributos direcional (parâmetro)

Os atributos direcionais descrevem se os dados são transmitidos do cliente para o servidor, servidor para cliente ou ambos. Todos os parâmetros no protótipo de função devem ser associados a atributos direcionais. As três combinações possíveis de atributos direcionais são: 1) \[ [**em**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] e 3) \[ **in**, **out** \] . Elas descrevem a maneira como os parâmetros são passados entre os procedimentos de chamada e chamados. Quando você compila no padrão (modo estendido da Microsoft) e omite um atributo direcional para um parâmetro, o compilador MIDL assume um valor padrão de \[ **no** \] .

Um \[ parâmetro de [**saída**](/windows/desktop/Midl/out-idl) \] deve ser um ponteiro. Na verdade, o \[  \] atributo out não é significativo quando aplicado a parâmetros que não atuam como ponteiros porque os parâmetros da função C são passados por valor. Em C, a função chamada recebe uma cópia privada do valor do parâmetro; Ele não pode alterar o valor da função de chamada para esse parâmetro. No entanto, se o parâmetro atuar como um ponteiro, ele poderá ser usado para acessar e modificar a memória. O \[ atributo **out** \] indica que a função de servidor deve retornar o valor para a função de chamada do cliente e que a memória associada ao ponteiro deve ser retornada de acordo com os atributos atribuídos ao ponteiro.

A interface a seguir demonstra as três possíveis combinações de atributos direcionais que podem ser aplicados a um parâmetro. A função **InOutProc** é definida no arquivo IDL como:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

O primeiro parâmetro, *S1*, é \[ somente [**no**](/windows/desktop/Midl/in) \] . Seu valor é transmitido para o computador remoto, mas não é retornado para o procedimento de chamada. Embora o aplicativo de servidor possa alterar seu valor para *S1*, o valor de *S1* no cliente é o mesmo antes e depois da chamada.

O segundo parâmetro, *PS2*, é definido no protótipo da função como um ponteiro com os \[ atributos [**in**](/windows/desktop/Midl/in) \] e \[ [**out**](/windows/desktop/Midl/out-idl) \] . O \[ atributo **in** \] indica que o valor do parâmetro é passado do cliente para o servidor. O \[ atributo **out** \] indica que o valor apontado por *PS2* é retornado ao cliente.

O terceiro parâmetro está \[ [**fora**](/windows/desktop/Midl/out-idl) \] apenas. O espaço é alocado para o parâmetro no servidor, mas o valor é indefinido na entrada. Conforme mencionado acima, todos os parâmetros de \[ **saída** \] devem ser ponteiros.

O procedimento remoto altera o valor de todos os três parâmetros, mas apenas os novos valores dos \[ [](/windows/desktop/Midl/out-idl) \] parâmetros out e \[ [**in**](/windows/desktop/Midl/in) \] estão disponíveis para o cliente.


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



No retorno da chamada para **InOutProc**, o segundo e o terceiro parâmetros são modificados. O primeiro parâmetro, que está \[ [**em**](/windows/desktop/Midl/in) \] apenas, é inalterado.

![em parâmetros](images/prog-a22.png)

![parâmetros out](images/prog-a23.png)

![parâmetros de entrada](images/prog-a21.png)

 

 