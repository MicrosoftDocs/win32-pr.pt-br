---
description: É um inteiro vinculado a uma propriedade com os qualificadores de BitMap e bitvalue.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Qualificadores BitMap e bitvalue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752613"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Qualificadores BitMap e bitvalue

Um bitmap é um inteiro vinculado a uma propriedade com os qualificadores **bitmap** e **bitvalue** . Cada bit do valor da propriedade atua como um índice na matriz de valores na lista **bitvalue** . Como vários bits no valor da propriedade podem ser "ativados" ao mesmo tempo, é possível usar um único valor de propriedade para indicar vários valores simultâneos.

Por exemplo, o exemplo de código MOF a seguir estabelece a propriedade **filetype** como tendo os qualificadores **bitmap** e **bitvalues** . Ele estabelece ainda mais que o bit de ordem inferior (bit 0) corresponde ao valor "somente leitura". O próximo bit (bit 1) corresponde a "Hidden" e assim por diante. (Nem todos os bits devem ser significativos. Nesse sistema de oito bits, os dois bits de ordem superior, 6 e 7, não têm significado.)

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

Se a propriedade **filetype** relatar o valor 7 (bits 0000 0111), o arquivo será "somente leitura", "sistema" e "oculto". Se a propriedade **filetype** relatar o valor 18 (0x12, bits 0001 0010), será um subdiretório oculto.

Há dois tipos diferentes de bitmaps usando o código MOF:

-   Bits significativos consecutivos começando com o bit de ordem inferior (bit 0)

    Você pode definir uma matriz de valores de bit sem especificar explicitamente os bits significativos se os bits significativos começarem com o bit de ordem inferior (bit 0) e progredirem para cima sem interrupção por todos os itens na matriz **bitvalue** . O exemplo de código MOF a seguir executa a mesma função do exemplo anterior.

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

    Se o bit de ordem inferior for insignificante ou a sequência de bits significativos não for contínua, você deverá especificar os qualificadores **bitmap** e **bitvalues** . O exemplo de código MOF a seguir mostra uma situação em que o bit de ordem inferior não é significativo e há uma lacuna na sequência de bits significativos.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    Nesse caso, a definição do bit de ordem inferior (bit 0) não tem significância e é ignorada. No entanto, a configuração bit 1 (0x2) indica que essa mensagem de email está sinalizada para acompanhamento, definindo bit 4 (0x8) indica que uma confirmação de entrega deve ser enviada ao remetente quando a mensagem de email chegou à caixa de correio do destinatário e a definição de bit 5 (0x10) especifica que uma confirmação de leitura deve ser enviada ao remetente quando a mensagem de email é aberta pelo Definir todos os três bits significativos (0x1A) especifica todas as três condições para a mensagem de email.

## <a name="remarks"></a>Comentários

Ao decidir se os qualificadores de valores de **bitmap** / **bitvalues** ou **ValueMap** devem ser usados /  , determine se algum dos valores indicados pode ocorrer simultaneamente. Se vários valores simultâneos puderem existir, você deverá usar o **bitmap** / **bitvalues**. Se todos os valores forem mutuamente exclusivos, você deverá usar os qualificadores de valores de **ValueMap** /  .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Qualificadores de valor e ValueMap](value-map.md)
</dt> </dl>

 

 



