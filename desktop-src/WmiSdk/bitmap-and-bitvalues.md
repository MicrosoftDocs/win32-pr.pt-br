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
# <a name="bitmap-and-bitvalue-qualifiers"></a><span data-ttu-id="d3973-103">Qualificadores BitMap e bitvalue</span><span class="sxs-lookup"><span data-stu-id="d3973-103">BitMap and BitValue Qualifiers</span></span>

<span data-ttu-id="d3973-104">Um bitmap é um inteiro vinculado a uma propriedade com os qualificadores **bitmap** e **bitvalue** .</span><span class="sxs-lookup"><span data-stu-id="d3973-104">A bitmap is an integer linked to a property with the **BitMap** and **BitValue** qualifiers.</span></span> <span data-ttu-id="d3973-105">Cada bit do valor da propriedade atua como um índice na matriz de valores na lista **bitvalue** .</span><span class="sxs-lookup"><span data-stu-id="d3973-105">Each bit of the property value acts as an index into the array of values in the **BitValue** list.</span></span> <span data-ttu-id="d3973-106">Como vários bits no valor da propriedade podem ser "ativados" ao mesmo tempo, é possível usar um único valor de propriedade para indicar vários valores simultâneos.</span><span class="sxs-lookup"><span data-stu-id="d3973-106">Because multiple bits in the property value can be "on" at the same time, it is possible to use a single property value to indicate multiple concurrent values.</span></span>

<span data-ttu-id="d3973-107">Por exemplo, o exemplo de código MOF a seguir estabelece a propriedade **filetype** como tendo os qualificadores **bitmap** e **bitvalues** .</span><span class="sxs-lookup"><span data-stu-id="d3973-107">For example, the following MOF code example establishes the **FileType** property as having the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="d3973-108">Ele estabelece ainda mais que o bit de ordem inferior (bit 0) corresponde ao valor "somente leitura".</span><span class="sxs-lookup"><span data-stu-id="d3973-108">It further establishes that the low-order bit (bit 0) corresponds to the value "Read Only".</span></span> <span data-ttu-id="d3973-109">O próximo bit (bit 1) corresponde a "Hidden" e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d3973-109">The next bit (bit 1) corresponds to "Hidden", and so on.</span></span> <span data-ttu-id="d3973-110">(Nem todos os bits devem ser significativos.</span><span class="sxs-lookup"><span data-stu-id="d3973-110">(Not all bits must be significant.</span></span> <span data-ttu-id="d3973-111">Nesse sistema de oito bits, os dois bits de ordem superior, 6 e 7, não têm significado.)</span><span class="sxs-lookup"><span data-stu-id="d3973-111">In this eight-bit system, the two high-order bits, 6 and 7, have no significance.)</span></span>

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

<span data-ttu-id="d3973-112">Se a propriedade **filetype** relatar o valor 7 (bits 0000 0111), o arquivo será "somente leitura", "sistema" e "oculto".</span><span class="sxs-lookup"><span data-stu-id="d3973-112">If the **FileType** property reports the value 7 (bits 0000 0111), the file is "Read Only", "System", and "Hidden".</span></span> <span data-ttu-id="d3973-113">Se a propriedade **filetype** relatar o valor 18 (0x12, bits 0001 0010), será um subdiretório oculto.</span><span class="sxs-lookup"><span data-stu-id="d3973-113">If the **FileType** property reports the value 18 (0x12, bits 0001 0010), it is a hidden subdirectory.</span></span>

<span data-ttu-id="d3973-114">Há dois tipos diferentes de bitmaps usando o código MOF:</span><span class="sxs-lookup"><span data-stu-id="d3973-114">There are two different types of bitmaps using MOF code:</span></span>

-   <span data-ttu-id="d3973-115">Bits significativos consecutivos começando com o bit de ordem inferior (bit 0)</span><span class="sxs-lookup"><span data-stu-id="d3973-115">Consecutive significant bits beginning with the low-order bit (bit 0)</span></span>

    <span data-ttu-id="d3973-116">Você pode definir uma matriz de valores de bit sem especificar explicitamente os bits significativos se os bits significativos começarem com o bit de ordem inferior (bit 0) e progredirem para cima sem interrupção por todos os itens na matriz **bitvalue** .</span><span class="sxs-lookup"><span data-stu-id="d3973-116">You can define an array of bit values without explicitly specifying the significant bits if the significant bits begin with the low-order bit (bit 0) and progress upward without interruption through all items in the **BitValue** array.</span></span> <span data-ttu-id="d3973-117">O exemplo de código MOF a seguir executa a mesma função do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="d3973-117">The following MOF code example performs the same function as the previous example.</span></span>

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   <span data-ttu-id="d3973-118">Bit significativo precedido por um bit não significativo</span><span class="sxs-lookup"><span data-stu-id="d3973-118">Significant bit preceded by a non-significant bit</span></span>

    <span data-ttu-id="d3973-119">Se o bit de ordem inferior for insignificante ou a sequência de bits significativos não for contínua, você deverá especificar os qualificadores **bitmap** e **bitvalues** .</span><span class="sxs-lookup"><span data-stu-id="d3973-119">If the low-order bit is insignificant, or the sequence of significant bits is not continuous, you must specify both the **BitMap** and **BitValues** qualifiers.</span></span> <span data-ttu-id="d3973-120">O exemplo de código MOF a seguir mostra uma situação em que o bit de ordem inferior não é significativo e há uma lacuna na sequência de bits significativos.</span><span class="sxs-lookup"><span data-stu-id="d3973-120">The following MOF code example shows a situation in which the low-order bit is not significant and there is a gap in the sequence of significant bits.</span></span>

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    <span data-ttu-id="d3973-121">Nesse caso, a definição do bit de ordem inferior (bit 0) não tem significância e é ignorada.</span><span class="sxs-lookup"><span data-stu-id="d3973-121">In this case, setting the low-order bit (bit 0) has no significance and is ignored.</span></span> <span data-ttu-id="d3973-122">No entanto, a configuração bit 1 (0x2) indica que essa mensagem de email está sinalizada para acompanhamento, definindo bit 4 (0x8) indica que uma confirmação de entrega deve ser enviada ao remetente quando a mensagem de email chegou à caixa de correio do destinatário e a definição de bit 5 (0x10) especifica que uma confirmação de leitura deve ser enviada ao remetente quando a mensagem de email é aberta pelo</span><span class="sxs-lookup"><span data-stu-id="d3973-122">However, setting bit 1 (0x2) indicates that this email message is flagged for follow up, setting bit 4 (0x8) indicates that a delivery receipt should be sent to the sender when the email message has arrived at the recipient's mailbox, and setting bit 5 (0x10) specifies that a read receipt should be sent to the sender when the email message is opened by the recipient.</span></span> <span data-ttu-id="d3973-123">Definir todos os três bits significativos (0x1A) especifica todas as três condições para a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d3973-123">Setting all three significant bits (0x1A) specifies all three conditions for the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3973-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3973-124">Remarks</span></span>

<span data-ttu-id="d3973-125">Ao decidir se os qualificadores de valores de **bitmap** / **bitvalues** ou **ValueMap** devem ser usados /  , determine se algum dos valores indicados pode ocorrer simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="d3973-125">In deciding whether to use the **BitMap**/**BitValues** or **ValueMap**/**Values** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="d3973-126">Se vários valores simultâneos puderem existir, você deverá usar o **bitmap** / **bitvalues**.</span><span class="sxs-lookup"><span data-stu-id="d3973-126">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="d3973-127">Se todos os valores forem mutuamente exclusivos, você deverá usar os qualificadores de valores de **ValueMap** /  .</span><span class="sxs-lookup"><span data-stu-id="d3973-127">If all the values are mutually exclusive, you should use the **ValueMap**/**Values** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3973-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3973-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3973-129">Qualificadores de valor e ValueMap</span><span class="sxs-lookup"><span data-stu-id="d3973-129">ValueMap and Value Qualifiers</span></span>](value-map.md)
</dt> </dl>

 

 



