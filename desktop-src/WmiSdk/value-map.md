---
description: Um mapa de valor é uma matriz vinculada a uma propriedade com os qualificadores Value e ValueMap.
ms.assetid: 7667e87f-b997-4fd9-81ea-b27c9d2a9335
ms.tgt_platform: multiple
title: Qualificadores de valor e ValueMap
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df85342df9543e4d62b04482785ec31bb5bd3982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760629"
---
# <a name="valuemap-and-value-qualifiers"></a><span data-ttu-id="52e69-103">Qualificadores de valor e ValueMap</span><span class="sxs-lookup"><span data-stu-id="52e69-103">ValueMap and Value Qualifiers</span></span>

<span data-ttu-id="52e69-104">Um mapa de valor é uma matriz vinculada a uma propriedade com os qualificadores **Value** e **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="52e69-104">A value map is an array linked to a property with the **Value** and **ValueMap** qualifiers.</span></span>

<span data-ttu-id="52e69-105">A propriedade atua como um índice na matriz, mantendo um valor que representa um dos valores na matriz.</span><span class="sxs-lookup"><span data-stu-id="52e69-105">The property acts as an index into the array, holding a value that represents one of the values in the array.</span></span> <span data-ttu-id="52e69-106">Usando o código MOF, você pode ter os seguintes tipos de mapas de valor:</span><span class="sxs-lookup"><span data-stu-id="52e69-106">Using MOF code, you can have the following types of value maps:</span></span>

-   <span data-ttu-id="52e69-107">Mapeamento de matriz para um inteiro.</span><span class="sxs-lookup"><span data-stu-id="52e69-107">Array mapping to an integer.</span></span>

    <span data-ttu-id="52e69-108">Você pode definir uma matriz com o qualificador de **valor** e vincular a matriz diretamente a uma propriedade de número inteiro, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="52e69-108">You can define an array with the **Value** qualifier and link the array directly to an integer property, as shown in the following example:</span></span>

    ``` syntax
    [Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="52e69-109">Neste exemplo, o valor da propriedade **status** é um índice na matriz de cadeia de caracteres definida pelo **valor**.</span><span class="sxs-lookup"><span data-stu-id="52e69-109">In this example, the **Status** property value is an index into the string array defined by **Value**.</span></span> <span data-ttu-id="52e69-110">A propriedade só pode assumir valores que correspondam às posições ordinais na matriz de **valor** menos 1.</span><span class="sxs-lookup"><span data-stu-id="52e69-110">The property can only take on values that correspond to the ordinal positions in the **Value** array minus 1.</span></span> <span data-ttu-id="52e69-111">Por exemplo, a configuração de **status** como "1" é mapeada para o valor "erro".</span><span class="sxs-lookup"><span data-stu-id="52e69-111">For example, setting **Status** to "1" maps to the "Error" value.</span></span> <span data-ttu-id="52e69-112">A propriedade index só pode ter valores que correspondam a posições na matriz **Value** .</span><span class="sxs-lookup"><span data-stu-id="52e69-112">The index property can take only values that correspond to positions in the **Value** array.</span></span> <span data-ttu-id="52e69-113">Por exemplo, se a matriz tiver 10 entradas, a propriedade index poderá obter a história de 0 a 9, não 30 ou 177.</span><span class="sxs-lookup"><span data-stu-id="52e69-113">For example, if the array has 10 entries, the index property can story 0 through 9, not 30 or 177.</span></span>

-   <span data-ttu-id="52e69-114">Mapeamento de matriz para outro mapeamento de matriz para um inteiro.</span><span class="sxs-lookup"><span data-stu-id="52e69-114">Array mapping to another array mapping to an integer.</span></span>

    <span data-ttu-id="52e69-115">Se você quiser criar um índice que não usa um sistema ordinal de contagem, use o qualificador **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="52e69-115">If you wish to create an index that does not use an ordinal system of counting, use the **ValueMap** qualifier.</span></span> <span data-ttu-id="52e69-116">O qualificador **ValueMap** configura outra matriz que contém um sistema de numeração de índice arbitrário, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="52e69-116">The **ValueMap** qualifier sets up another array that holds an arbitrary index numbering system, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"1", "3", "99", "0"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    sint32 Status;
    ```

    <span data-ttu-id="52e69-117">Embora seja necessário posicionar os valores de **ValueMap** entre aspas, o WMI considera os valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="52e69-117">Although you must place the values of **ValueMap** in quotations, WMI considers the values integers.</span></span> <span data-ttu-id="52e69-118">Portanto, neste exemplo, você pode definir a propriedade **status** como um número inteiro no conjunto **ValueMap** : 1, 3, 99 ou 0.</span><span class="sxs-lookup"><span data-stu-id="52e69-118">Therefore, In this example you can set the **Status** property to an integer in the **ValueMap** set: 1, 3, 99, or 0.</span></span> <span data-ttu-id="52e69-119">O WMI mapeia cada inteiro de uma posição ordinal na matriz de cadeia de caracteres **ValueMap** para uma posição correspondente na matriz **Value** .</span><span class="sxs-lookup"><span data-stu-id="52e69-119">WMI maps each integer from an ordinal position in the **ValueMap** string array to a corresponding position in the **Value** array.</span></span> <span data-ttu-id="52e69-120">Por exemplo, definir **status** como 0 é mapeado para "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="52e69-120">For example, setting **Status** to 0 maps to "Unknown".</span></span>

-   <span data-ttu-id="52e69-121">Mapeamento de matriz para outro mapeamento de matriz para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="52e69-121">Array mapping to another array mapping to a string.</span></span>

    <span data-ttu-id="52e69-122">Se você não quiser usar um inteiro para indexar sua matriz, você pode usar uma cadeia de caracteres para armazenar um dos valores possíveis em sua matriz.</span><span class="sxs-lookup"><span data-stu-id="52e69-122">If you do not want to use an integer to index your array, you can instead use a string to hold one of the possible values in your array.</span></span> <span data-ttu-id="52e69-123">Para fazer isso, você deve definir um **valor** e uma matriz **ValueMap** que contenham cadeias de caracteres, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="52e69-123">To do so, you must define both a **Value** and **ValueMap** array that both contain strings, as shown in the following example:</span></span>

    ``` syntax
    [ValueMap {"OK", "Error", "Degraded", "Unknown"}, 
     Values {"OK", "Error", "Degraded", "Unknown"}, Read]
    string Status;
    ```

    <span data-ttu-id="52e69-124">Com uma propriedade de cadeia de caracteres, os valores reais permitidos da propriedade são as entradas na matriz **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="52e69-124">With a string property, the actual allowable values of the property are the entries in the **ValueMap** array.</span></span> <span data-ttu-id="52e69-125">Por exemplo, você pode definir **status** como "OK" ou "desconhecido".</span><span class="sxs-lookup"><span data-stu-id="52e69-125">For example, you can set **Status** to "OK" or "Unknown".</span></span>

<span data-ttu-id="52e69-126">Cabe ao aplicativo aproveitar os mapeamentos de uma maneira útil.</span><span class="sxs-lookup"><span data-stu-id="52e69-126">It is up to the application to take advantage of mappings in a useful way.</span></span> <span data-ttu-id="52e69-127">Cabe ao provedor impor um intervalo legal de valores.</span><span class="sxs-lookup"><span data-stu-id="52e69-127">It is up to the provider to enforce a legal range of values.</span></span>

## <a name="remarks"></a><span data-ttu-id="52e69-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="52e69-128">Remarks</span></span>

<span data-ttu-id="52e69-129">Ao decidir se deve usar o  / **valor** de ValueMap ou os / qualificadores **bitvalues** de bitmap, determine se algum dos valores indicados pode ocorrer simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="52e69-129">In deciding whether to use the **ValueMap**/**Value** or **BitMap**/**BitValues** qualifiers, determine whether any of the values being indicated could occur concurrently.</span></span> <span data-ttu-id="52e69-130">Se vários valores simultâneos puderem existir, você deverá usar o **bitmap** / **bitvalues**.</span><span class="sxs-lookup"><span data-stu-id="52e69-130">If multiple concurrent values can exist, you must use **BitMap**/**BitValues**.</span></span> <span data-ttu-id="52e69-131">Se todos os valores forem mutuamente exclusivos, você deverá usar os  / qualificadores de **valor** ValueMap.</span><span class="sxs-lookup"><span data-stu-id="52e69-131">If all the values are mutually exclusive, you should use the **ValueMap**/**Value** qualifiers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52e69-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52e69-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52e69-133">BitMap e bitvalues</span><span class="sxs-lookup"><span data-stu-id="52e69-133">BitMap and BitValues</span></span>](bitmap-and-bitvalues.md)
</dt> </dl>

 

 



