---
description: Transição de chave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transição de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e4f83bbe26f49989d612efe718c2d838ce7f1d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825609"
---
# <a name="key-transition"></a>Transição de chave

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A transição de chave executa a criação de chaves com base no valor RGB, no valor alfa, no matiz ou na luminância.

A imagem a seguir mostra a transição de chave:

![transição de chave](images/trans-key.png)

ID de classe (CLSID): {C5B19592-145E-11D3-9F04-006008039E37}

Nome da variável CLSID: CLSID \_ DxtKey

Nome amigável: "DxtKey"

Propriedades



| Propriedade   | Tipo  | Intervalo válido           | Descrição                                                                                                                                                                                                                                                | Aplica-se A                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Matiz        | INT   | 0 – 360                 | O valor de matiz para o qual fazer a chave.                                                                                                                                                                                                                             | Matiz                            |
| Invert     | BOOL  | **False** ou **true** | Valor booliano que indica se a operação padrão da chave deve ser invertida. Se **for false**, os pixels na imagem subjacente serão tornados transparentes da maneira padrão. Se **for true**, a operação inverterá.                                                   | Croma, matiz, luminância, Nonred |
| KeyType    | INT   | Ver comentários           | Especifica o tipo de chave. Para obter mais informações, consulte Comentários.                                                                                                                                                                                              | Todos                            |
| Luminância  | INT   | 0 – 100                 | O valor de luminância para a chave.                                                                                                                                                                                                                       | Luminância                      |
| RGB        | DWORD | 0x0 – 0xFFFFFF        | A cor na qual se deve ser a chave. O valor é um número hexadecimal com o formato 0x *RRGGBB*, em que *RR* é o valor vermelho, *gg* é o valor verde e *BB* é o valor azul. (Vermelho puro, verde e azul são 0xFF0000, 0x00FF00 e 0x0000FF, respectivamente.) | Croma                         |
| Similaridade | INT   | 0 – 100                 | O intervalo de dados de cores que se torna transparente. Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente.                                                                                                                                        | Croma, Nonred                 |



 

## <a name="remarks"></a>Comentários

O tipo de chave executada depende do valor da propriedade **KeyType** , que deve ser uma das seguintes:



| Valor | Enumeração       | Descrição                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Chave croma (chave por valor RGB).                        |
| 1     | DXTKEY \_ NONRED    | Chave Nonred. (Torna as áreas azul e verde transparentes.) |
| 2     | luminância de DXTKEY \_ | Chave de luminância.                                        |
| 3     | DXTKEY \_ alfa     | Chave por valor alfa.                                   |
| 4     | \_matiz DXTKEY       | Chave por matiz.                                           |



 

O tipo de chave usa como padrão DXTKEY \_ alfa.

 

 



