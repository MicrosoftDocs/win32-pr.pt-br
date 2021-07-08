---
description: O sistema de propriedades contém uma propriedade chamada System.Kind, que divide itens em tipos de acordo com a extensão de nome de arquivo e com quais usuários finais podem se identificar facilmente.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Usando nomes de tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca36d7c1de587efd8d96f0c18aaca9457721714
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481871"
---
# <a name="using-kind-names"></a><span data-ttu-id="e55df-103">Usando nomes de tipo</span><span class="sxs-lookup"><span data-stu-id="e55df-103">Using Kind Names</span></span>

<span data-ttu-id="e55df-104">O sistema de propriedades contém uma propriedade chamada , que divide os itens em tipos de acordo com a extensão de nome de arquivo e com a qual os usuários finais `System.Kind` podem se identificar facilmente.</span><span class="sxs-lookup"><span data-stu-id="e55df-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="e55df-105">Este tópico é organizado da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="e55df-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e55df-106">Sobre a propriedade System.Kind</span><span class="sxs-lookup"><span data-stu-id="e55df-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="e55df-107">Hierarquia e registro de valor de tipo</span><span class="sxs-lookup"><span data-stu-id="e55df-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="e55df-108">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="e55df-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="e55df-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e55df-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="e55df-110">Sobre a propriedade System.Kind</span><span class="sxs-lookup"><span data-stu-id="e55df-110">About the System.Kind Property</span></span>

<span data-ttu-id="e55df-111">O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e55df-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="e55df-112">A propriedade divide itens em tipos e fornece um Nome de tipo com o qual os usuários finais podem se identificar, como `System.Kind` Documentos, Música, Imagens e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e55df-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="e55df-113">Portanto, os Nomes de tipo vêm a ser conhecidos como amigáveis.</span><span class="sxs-lookup"><span data-stu-id="e55df-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="e55df-114">Como a propriedade é definida com o mesmo valor para itens do mesmo tipo de arquivo e associa itens que têm características semelhantes a uma propriedade comum, o sistema e o usuário podem agir no grupo como `System.Kind` um todo.</span><span class="sxs-lookup"><span data-stu-id="e55df-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="e55df-115">Por exemplo, a propriedade pode ser usada para limitar uma pesquisa a itens de um tipo específico, exibir as propriedades mais relevantes para um item na exibição Conteúdo ou agrupar itens `System.Kind` semelhantes.</span><span class="sxs-lookup"><span data-stu-id="e55df-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="e55df-116">Como Kind é uma propriedade de cadeia de caracteres de vários valores, você pode ter `audio;video` um valor `link;document` ou Kind.</span><span class="sxs-lookup"><span data-stu-id="e55df-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="e55df-117">Um `System.Kind` valor é uma lista ordenada de valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e55df-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="e55df-118">Em alguns casos, pode haver apenas um elemento nessa lista.</span><span class="sxs-lookup"><span data-stu-id="e55df-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="e55df-119">Em outros casos, um item pode pertencer a mais de um Tipo.</span><span class="sxs-lookup"><span data-stu-id="e55df-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="e55df-120">Para obter um exemplo de um item que pertence a mais de um Kind, consulte o exemplo de chave do Registro neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e55df-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="e55df-121">Os valores de cadeia de caracteres são de um conjunto predefinido de valores conhecidos.</span><span class="sxs-lookup"><span data-stu-id="e55df-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="e55df-122">Os valores são comparados usando funções de comparação de cadeia de caracteres não sensíveis a maiúsculas e minúsculas e sem valor de localidade.</span><span class="sxs-lookup"><span data-stu-id="e55df-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="e55df-123">Essas cadeias de caracteres não são localizadas.</span><span class="sxs-lookup"><span data-stu-id="e55df-123">These strings are not localized.</span></span>

<span data-ttu-id="e55df-124">Alguns nomes kind já estão associados a propriedades e padrões de layout.</span><span class="sxs-lookup"><span data-stu-id="e55df-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="e55df-125">Por exemplo, itens associados a e itens associados a exibem propriedades diferentes mesmo quando estão na mesma exibição, devido às propriedades e padrões de layout que já estão associados a esses dois `Kind.Picture` `Kind.Document` Nomes de tipo.</span><span class="sxs-lookup"><span data-stu-id="e55df-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="e55df-126">Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que define o número de propriedades exibidas para cada item e seu layout.</span><span class="sxs-lookup"><span data-stu-id="e55df-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="e55df-127">Para obter mais informações, consulte [Exibição de conteúdo com base no tipo de arquivo ou associação de tipo](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e55df-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="e55df-128">Hierarquia e registro de valor de tipo</span><span class="sxs-lookup"><span data-stu-id="e55df-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="e55df-129">Um `Kind` valor deve representar um dos valores na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="e55df-129">A `Kind` value must represent one of the values in the following list.</span></span>

```
Item
   Folder
   Program
   Game
   WebHistory
   Feed
   Document
   Link
   Movie
   Music
   RecordedTV
   Video
   Picture
   Communications
      Calendar
      Contact
      E-Mail
      Task
      Journal
      Note
      InstantMessage
```

<span data-ttu-id="e55df-130">Os manipuladores de propriedades podem declarar sua propriedade estaticamente por meio do Registro ou podem fornecer o valor dinamicamente por meio de seu código, como faria `System.Kind` com uma propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="e55df-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="e55df-131">Para definir estaticamente a propriedade , uma entrada de valor REG SZ é adicionada sob a chave do Registro `Kind` **KindMap,** conforme mostrado no exemplo a **\_** seguir.</span><span class="sxs-lookup"><span data-stu-id="e55df-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     .recipe = Document
                     .ccc = Contact; Communications
```

<span data-ttu-id="e55df-132">Observe que o `Kind` pode ser um único valor ou vários valores em uma cadeia de caracteres delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="e55df-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="e55df-133">Ao fornecer vários valores, o valor mais `Kind` específico é listado primeiro com o valor menos específico a seguir.</span><span class="sxs-lookup"><span data-stu-id="e55df-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="e55df-134">No exemplo, Contact é nomeado primeiro porque é hierarquicamente mais específico do que Communications.</span><span class="sxs-lookup"><span data-stu-id="e55df-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="e55df-135">O valor **Item** é assumido e não deve ser fornecido explicitamente.</span><span class="sxs-lookup"><span data-stu-id="e55df-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e55df-136">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="e55df-136">Additional Resources</span></span>

-   <span data-ttu-id="e55df-137">Para a documentação de referência sobre propriedades, [consulte System.Kind](./props-system-kind.md) e [System.KindText](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="e55df-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="e55df-138">Para obter mais informações sobre como criar novos ou usar tipos de arquivo existentes, consulte [Tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="e55df-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e55df-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e55df-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e55df-140">Noções básicas sobre manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="e55df-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="e55df-141">Usando listas de propriedades</span><span class="sxs-lookup"><span data-stu-id="e55df-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="e55df-142">Inicializando manipuladores de propriedades</span><span class="sxs-lookup"><span data-stu-id="e55df-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="e55df-143">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="e55df-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="e55df-144">Práticas recomendadas e perguntas frequentes do manipulador de propriedades</span><span class="sxs-lookup"><span data-stu-id="e55df-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
