---
title: Atributos direcionais (parâmetro)
description: Atributos direcionais descrevem se os dados são transmitidos do cliente para o servidor, do servidor para o cliente ou ambos.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- RPC de Chamada de Procedimento Remoto , descrito, atributos direcionais
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e9ff23e7e12acbd5cf301afe6786599268d2e149878a326a62f79cd91f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930629"
---
# <a name="directional-parameter-attributes"></a>Atributos direcionais (parâmetro)

Atributos direcionais descrevem se os dados são transmitidos do cliente para o servidor, do servidor para o cliente ou ambos. Todos os parâmetros no protótipo de função devem ser associados a atributos direcionais. As três combinações possíveis de atributos direcionais são: 1) \[ [**em**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] e 3) \[ **em**, **out** \] . Eles descrevem a maneira como os parâmetros são passados entre os procedimentos de chamada e chamado. Quando você compila no padrão (modo estendido da Microsoft) e omite um atributo direcional para um parâmetro, o compilador MIDL assume um valor padrão \[ **de em** \] .

Um \[ [**parâmetro**](/windows/desktop/Midl/out-idl) \] out deve ser um ponteiro. Na verdade, o atributo out não é significativo quando aplicado a parâmetros que não atuam como ponteiros porque os parâmetros da função C são \[  \] passados por valor. Em C, a função chamada recebe uma cópia privada do valor do parâmetro; ele não pode alterar o valor da função de chamada para esse parâmetro. No entanto, se o parâmetro atuar como um ponteiro, ele poderá ser usado para acessar e modificar a memória. O atributo out indica que a função de servidor deve retornar o valor para a função de chamada do cliente e que a memória associada ao ponteiro deve ser retornada de acordo com os atributos atribuídos ao \[  \] ponteiro.

A interface a seguir demonstra as três combinações possíveis de atributos direcionais que podem ser aplicados a um parâmetro. A função **InOutProc** é definida no arquivo IDL como:

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

O primeiro parâmetro, *s1*, \[ [**está em**](/windows/desktop/Midl/in) \] apenas. Seu valor é transmitido para o computador remoto, mas não é retornado ao procedimento de chamada. Embora o aplicativo de servidor possa alterar seu valor para *s1*, o valor *de s1* no cliente é o mesmo antes e depois da chamada.

O segundo parâmetro, *ps2,* é definido no protótipo de função como um ponteiro com atributos \[ [**de dentro**](/windows/desktop/Midl/in) \] e de \[ [](/windows/desktop/Midl/out-idl) \] saída. O \[ **atributo** \] in indica que o valor do parâmetro é passado do cliente para o servidor. O \[ **atributo** \] out indica que o valor apontado por *ps2* é retornado ao cliente.

O terceiro parâmetro está \[ [**fora**](/windows/desktop/Midl/out-idl) \] apenas. O espaço é alocado para o parâmetro no servidor, mas o valor é indefinido na entrada. Conforme mencionado acima, todos \[ **os parâmetros** \] de saída devem ser ponteiros.

O procedimento remoto altera o valor de todos os três parâmetros, mas apenas os novos valores dos parâmetros out e in estão \[ [](/windows/desktop/Midl/out-idl) \] disponíveis para o \[ [](/windows/desktop/Midl/in) \] cliente.


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



No retorno da chamada para **InOutProc,** o segundo e o terceiro parâmetros são modificados. O primeiro parâmetro, que está \[ [**apenas**](/windows/desktop/Midl/in) \] em , não está inalterado.

![em parâmetros](images/prog-a22.png)

![parâmetros out](images/prog-a23.png)

![parâmetros de saída](images/prog-a21.png)

 

 