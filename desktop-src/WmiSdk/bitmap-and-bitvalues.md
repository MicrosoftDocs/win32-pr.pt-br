---
description: É um inteiro vinculado a uma propriedade com os qualificadores BitMap e BitValue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificadores BitMap e BitValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b02f2d9f2b6632d5f190d1537b2f33d822d916611983da71121ffbbded943d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051074"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Qualificadores BitMap e BitValue

Um bitmap é um inteiro vinculado a uma propriedade com os **qualificadores BitMap** e **BitValue.** Cada bit do valor da propriedade atua como um índice na matriz de valores na **lista BitValue.** Como vários bits no valor da propriedade podem ser "on" ao mesmo tempo, é possível usar um único valor de propriedade para indicar vários valores simultâneos.

Por exemplo, o exemplo de código MOF a seguir estabelece a **propriedade FileType** como tendo os qualificadores **BitMap** e **BitValues.** Ele estabelece ainda que o bit de ordem baixa (bit 0) corresponde ao valor "Somente Leitura". O próximo bit (bit 1) corresponde a "Hidden" e assim por diante. (Nem todos os bits devem ser significativos. Nesse sistema de oito bits, os dois bits de ordem alta, 6 e 7, não têm nenhum significado.)

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

Se a **propriedade FileType** relata o valor 7 (bits 0000 0111), o arquivo é "Somente Leitura", "Sistema" e "Oculto". Se a **propriedade FileType** relata o valor 18 (0x12 bits 0001 0010), ele é um subdiretório oculto.

Há dois tipos diferentes de bitmaps usando o código MOF:

-   Bits significativos consecutivos começando com o bit de ordem baixa (bit 0)

    Você pode definir uma matriz de valores de bits sem especificar explicitamente os bits significativos se os bits significativos começam com o bit de ordem baixa (bit 0) e progridem para cima sem interrupção em todos os itens na matriz **BitValue.** O exemplo de código MOF a seguir executa a mesma função do exemplo anterior.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Bit significativo precedido por um bit não significativo

    Se o bit de ordem baixa for insignificante ou a sequência de bits significativos não for contínua, você deverá especificar os qualificadores **BitMap** e **BitValues.** O exemplo de código MOF a seguir mostra uma situação em que o bit de ordem baixa não é significativo e há uma lacuna na sequência de bits significativos.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    Nesse caso, definir o bit de ordem baixa (bit 0) não tem nenhum significado e é ignorado. No entanto, a configuração do bit 1 (0x2) indica que essa mensagem de email está sinalizada para acompanhamento, a configuração do bit 4 (0x8) indica que um recibo de entrega deve ser enviado ao remetente quando a mensagem de email chegar à caixa de correio do destinatário e a configuração bit 5 (0x10) especifica que um recibo de leitura deve ser enviado ao remetente quando a mensagem de email for aberta pelo destinatário. Definir todos os três bits significativos (0x1A) especifica todas as três condições para a mensagem de email.

## <a name="remarks"></a>Comentários

Ao decidir se os qualificadores / **BitMap BitValues** ou **ValueMap** Values devem ser usado, determine se qualquer um dos valores que está sendo indicado pode /  ocorrer simultaneamente. Se vários valores simultâneos puderem existir, você deverá usar **BitMap** / **BitValues**. Se todos os valores são mutuamente exclusivos, você deve usar os qualificadores **ValueMap** / **Values.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Qualificadores valueMap e value](value-map.md)
</dt> </dl>

 

 



