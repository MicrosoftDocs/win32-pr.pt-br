---
description: O sistema de propriedades contém uma propriedade chamada System. Kind, que divide os itens em tipos de acordo com a extensão de nome de arquivo e quais usuários finais podem facilmente identificar com o.
ms.assetid: 1466b4c7-49ea-417a-ac94-7b45515ccb96
title: Usando nomes de tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f358306deaeb04d4ea30b10b0665cdc8323b4d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296612"
---
# <a name="using-kind-names"></a><span data-ttu-id="0ea52-103">Usando nomes de tipos</span><span class="sxs-lookup"><span data-stu-id="0ea52-103">Using Kind Names</span></span>

<span data-ttu-id="0ea52-104">O sistema de propriedades contém uma propriedade chamada `System.Kind` , que divide os itens em tipos de acordo com a extensão de nome de arquivo e quais usuários finais podem facilmente identificar com o.</span><span class="sxs-lookup"><span data-stu-id="0ea52-104">The property system contains a property called `System.Kind`, which divides items into types according to the file name extension, and which end users can easily identify with.</span></span>

<span data-ttu-id="0ea52-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0ea52-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="0ea52-106">Sobre a propriedade System. Kind</span><span class="sxs-lookup"><span data-stu-id="0ea52-106">About the System.Kind Property</span></span>](#about-the-systemkind-property)
-   [<span data-ttu-id="0ea52-107">Tipo de hierarquia e registro de valor</span><span class="sxs-lookup"><span data-stu-id="0ea52-107">Kind Value Hierarchy and Registration</span></span>](#kind-value-hierarchy-and-registration)
-   [<span data-ttu-id="0ea52-108">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="0ea52-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="0ea52-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ea52-109">Related topics</span></span>](#related-topics)

## <a name="about-the-systemkind-property"></a><span data-ttu-id="0ea52-110">Sobre a propriedade System. Kind</span><span class="sxs-lookup"><span data-stu-id="0ea52-110">About the System.Kind Property</span></span>

<span data-ttu-id="0ea52-111">O tipo foi introduzido no Windows Vista para expressar uma noção mais amigável do tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="0ea52-111">Kind was introduced in Windows Vista to express a more user-friendly notion of file type.</span></span> <span data-ttu-id="0ea52-112">A `System.Kind` Propriedade divide itens em tipos e fornece um nome de tipo que os usuários finais podem identificar, como documentos, música, imagens e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0ea52-112">The `System.Kind` property divides items into types and provides a Kind name that end users can identify with, such as Documents, Music, Pictures, and so forth.</span></span> <span data-ttu-id="0ea52-113">Portanto, os nomes de espécie vêm para serem conhecidos como amigáveis para o usuário.</span><span class="sxs-lookup"><span data-stu-id="0ea52-113">Hence, Kind names have come to be known as user-friendly.</span></span> <span data-ttu-id="0ea52-114">Como a `System.Kind` propriedade é definida com o mesmo valor para itens do mesmo tipo de arquivo e associa itens que têm características semelhantes com uma propriedade comum, o sistema e o usuário podem agir no grupo como um todo.</span><span class="sxs-lookup"><span data-stu-id="0ea52-114">Because the `System.Kind` property is set to the same value for items of the same file type, and associates items that have similar characteristics with a common property, the system and the user can act on the group as a whole.</span></span> <span data-ttu-id="0ea52-115">Por exemplo, a `System.Kind` propriedade pode ser usada para limitar uma pesquisa a itens de um tipo específico, exibir as propriedades mais relevantes para um item no modo de exibição de conteúdo ou agrupar itens semelhantes.</span><span class="sxs-lookup"><span data-stu-id="0ea52-115">For example, the `System.Kind` property can be used to limit a search to items of a specific kind, display the most relevant properties for an item in the Content view, or group similar items together.</span></span>

<span data-ttu-id="0ea52-116">Como Kind é uma propriedade de cadeia de caracteres com vários valores, você pode ter um `audio;video` valor ou um `link;document` tipo.</span><span class="sxs-lookup"><span data-stu-id="0ea52-116">Because Kind is a multi-value string property, you can have an `audio;video` or `link;document` Kind value.</span></span> <span data-ttu-id="0ea52-117">Um `System.Kind` valor é uma lista ordenada de valores de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0ea52-117">A `System.Kind` values is an ordered list of string values.</span></span> <span data-ttu-id="0ea52-118">Em alguns casos, pode haver apenas um elemento nessa lista.</span><span class="sxs-lookup"><span data-stu-id="0ea52-118">In some cases, there might be only one element in that list.</span></span> <span data-ttu-id="0ea52-119">Em outros casos, um item pode pertencer a mais de um tipo.</span><span class="sxs-lookup"><span data-stu-id="0ea52-119">In other cases, an item can belong to more than one Kind.</span></span> <span data-ttu-id="0ea52-120">Para obter um exemplo de um item que pertence a mais de um tipo, consulte o exemplo de chave do registro neste tópico.</span><span class="sxs-lookup"><span data-stu-id="0ea52-120">For an example of an item that belongs to more than one Kind, see the registry key example in this topic.</span></span> <span data-ttu-id="0ea52-121">Os valores de cadeia de caracteres são de um conjunto predefinido de valores conhecidos.</span><span class="sxs-lookup"><span data-stu-id="0ea52-121">The string values are from a predefined set of known values.</span></span> <span data-ttu-id="0ea52-122">Os valores são comparados usando funções de comparação de cadeia de caracteres e não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0ea52-122">The values are compared by using case-insensitive and locale-insensitive string-compare functions.</span></span> <span data-ttu-id="0ea52-123">Essas cadeias de caracteres não estão localizadas.</span><span class="sxs-lookup"><span data-stu-id="0ea52-123">These strings are not localized.</span></span>

<span data-ttu-id="0ea52-124">Alguns nomes de tipo já estão associados a propriedades e padrões de layout.</span><span class="sxs-lookup"><span data-stu-id="0ea52-124">Some Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="0ea52-125">Por exemplo, itens associados a `Kind.Picture` e itens associados a `Kind.Document` Exibir propriedades diferentes mesmo quando estão na mesma exibição, devido às propriedades e padrões de layout que já estão associados a esses dois tipos de nomes.</span><span class="sxs-lookup"><span data-stu-id="0ea52-125">For example, items associated with `Kind.Picture` and items associated with `Kind.Document` display different properties even when they are in the same view, because of the properties and layout patterns that are already associated with those two Kind names.</span></span> <span data-ttu-id="0ea52-126">Cada tipo de item pode ser associado a um dos quatro padrões de layout exclusivos que definem o número de propriedades exibidas para cada item e seu layout.</span><span class="sxs-lookup"><span data-stu-id="0ea52-126">Each item Kind can be associated with one of four unique layout patterns that defines the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="0ea52-127">Para obter mais informações, consulte [exibição de conteúdo com base na associação de tipo de arquivo ou](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85))tipo.</span><span class="sxs-lookup"><span data-stu-id="0ea52-127">For more information, see [Content View based on the File Type or Kind Association](/previous-versions/windows/desktop/legacy/ee330739(v=vs.85)).</span></span>

## <a name="kind-value-hierarchy-and-registration"></a><span data-ttu-id="0ea52-128">Tipo de hierarquia e registro de valor</span><span class="sxs-lookup"><span data-stu-id="0ea52-128">Kind Value Hierarchy and Registration</span></span>

<span data-ttu-id="0ea52-129">Um `Kind` valor deve representar um dos valores na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ea52-129">A `Kind` value must represent one of the values in the following list.</span></span>

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

<span data-ttu-id="0ea52-130">Manipuladores de propriedade podem declarar sua `System.Kind` Propriedade estaticamente por meio do registro ou podem fornecer o valor dinamicamente por meio de seu código como faria com uma propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="0ea52-130">Property handlers can declare their `System.Kind` property statically through the registry, or they can provide the value dynamically through their code as they would with a standard property.</span></span>

<span data-ttu-id="0ea52-131">Para definir estaticamente a `Kind` propriedade, uma entrada de valor **\_ sz do reg** é adicionada sob a chave do registro **KindMap** , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ea52-131">To statically define the `Kind` property, a **REG\_SZ** value entry is added under the **KindMap** registry key as shown in the following example.</span></span>

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

<span data-ttu-id="0ea52-132">Observe que o `Kind` pode ser um único valor ou vários valores em uma cadeia de caracteres delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="0ea52-132">Note that the `Kind` can be a single value or multiple values in a semi-colon delimited string.</span></span> <span data-ttu-id="0ea52-133">Ao fornecer vários valores, o valor mais específico `Kind` é listado primeiro com o menos específico a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ea52-133">When providing multiple values, the most specific `Kind` value is listed first with the least specific following.</span></span> <span data-ttu-id="0ea52-134">No exemplo, o contato é nomeado primeiro porque é hierarquicamente mais específico do que as comunicações.</span><span class="sxs-lookup"><span data-stu-id="0ea52-134">In the example, Contact is named first because it is hierarchically more specific than Communications.</span></span> <span data-ttu-id="0ea52-135">O **Item** de valor é assumido e não deve ser fornecido explicitamente.</span><span class="sxs-lookup"><span data-stu-id="0ea52-135">The value **Item** is assumed and should not be explicity provided.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ea52-136">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="0ea52-136">Additional Resources</span></span>

-   <span data-ttu-id="0ea52-137">Para obter a documentação de referência sobre propriedades, consulte [System. Kind](./props-system-kind.md) e [System. KindText](./props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="0ea52-137">For reference documentation about properties, see [System.Kind](./props-system-kind.md) and [System.KindText](./props-system-kindtext.md).</span></span>
-   <span data-ttu-id="0ea52-138">Para obter mais informações sobre como criar novos ou usar tipos de arquivo existentes, consulte [tipos de arquivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="0ea52-138">For more information about creating new or using existing file types, see [File Types](../shell/fa-file-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ea52-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0ea52-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ea52-140">Noções básicas sobre manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="0ea52-140">Understanding Property Handlers</span></span>](./building-property-handlers-properties.md)
</dt> <dt>

[<span data-ttu-id="0ea52-141">Usando listas de propriedades</span><span class="sxs-lookup"><span data-stu-id="0ea52-141">Using Property Lists</span></span>](./building-property-handlers-property-lists.md)
</dt> <dt>

[<span data-ttu-id="0ea52-142">Inicializando manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="0ea52-142">Initializing Property Handlers</span></span>](./building-property-handlers-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="0ea52-143">Registrando e distribuindo manipuladores de propriedade</span><span class="sxs-lookup"><span data-stu-id="0ea52-143">Registering and Distributing Property Handlers</span></span>](./prophand-reg-dist.md)
</dt> <dt>

[<span data-ttu-id="0ea52-144">Práticas recomendadas e perguntas frequentes do manipulador de propriedades</span><span class="sxs-lookup"><span data-stu-id="0ea52-144">Property Handler Best Practices and FAQ</span></span>](./prophand-bestprac-faq.md)
</dt> </dl>

 

 
