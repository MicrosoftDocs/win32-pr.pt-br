---
description: Transição de chave
ms.assetid: 5d1ed2e4-82c2-4364-b8f0-22bba974bc22
title: Transição de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fc5b905b1650b6db6bb98b542193160825b8bd6dd74626ef9bddc91b118118
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397268"
---
# <a name="key-transition"></a>Transição de chave

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A transição de chave executa a chave com base no valor RGB, no valor alfa, no matiz ou na luminância.

A imagem a seguir mostra a transição de chave:

![transição de chave](images/trans-key.png)

CLSID (ID de classe): {C5B19592-145E-11D3-9F04-006008039E37}

Nome da variável CLSID: CLSID \_ DxtKey

Nome amigável: "DxtKey"

Propriedades



| Propriedade   | Type  | Intervalo válido           | Descrição                                                                                                                                                                                                                                                | Aplica-se A                     |
|------------|-------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Matiz        | INT   | 0–360                 | O valor de matiz no qual a tecla deve ser chave.                                                                                                                                                                                                                             | Matiz                            |
| Invert     | BOOL  | **FALSE** ou **TRUE** | Valor booliana que indica se a operação padrão da chave deve ser invertida. Se **FALSE**, os pixels na imagem subjacente serão transparentes da maneira padrão. Se **TRUE**, a operação será invertida.                                                   | Chroma, Hue, Luminance, Nonred |
| KeyType    | INT   | Consulte Comentários           | Especifica o tipo de chave. Para obter mais informações, consulte Comentários.                                                                                                                                                                                              | Tudo                            |
| Luminância  | INT   | 0–100                 | O valor de luminância no qual a chave deve ser chave.                                                                                                                                                                                                                       | Luminância                      |
| RGB        | DWORD | 0x0 – 0xFFFFFF        | A cor na qual a tecla deve ser chave. O valor é um número hexadecimal com o formato 0x *RRGGBB,* em que *RR* é o valor vermelho, *GG* é o valor verde e *BB* é o valor azul. (Vermelho puro, verde e azul são 0xFF0000, 0x00FF00 e 0x0000FF, respectivamente.) | Chroma                         |
| Similaridade | INT   | 0–100                 | O intervalo de dados de cores que se torna transparente. Em valores mais altos, um intervalo maior de cores semelhantes é transparente.                                                                                                                                        | Chroma, Nonred                 |



 

## <a name="remarks"></a>Comentários

O tipo de chave que é executado depende do valor da propriedade **KeyType,** que deve ser um dos seguintes:



| Valor | Enumeração       | Descrição                                           |
|-------|-------------------|-------------------------------------------------------|
| 0     | DXTKEY \_ RGB       | Chave Chroma (chave por valor RGB).                        |
| 1     | DXTKEY \_ NONRED    | Chave nãoredada. (Torna as áreas azul e verde transparentes.) |
| 2     | DXTKEY \_ LUMINANCE | Chave de Luminância.                                        |
| 3     | DXTKEY \_ ALFA     | Chave por valor alfa.                                   |
| 4     | DXTKEY \_ HUE       | Chave por matiz.                                           |



 

O tipo de chave assume como padrão DXTKEY \_ ALPHA.

 

 



