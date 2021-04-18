---
description: Emitido como verdadeiro por um item de contêiner para indicar que seus itens filho não precisam ser enumerados por um indexador se o item de contêiner não foi alterado desde o último rastreamento de verificação de índice incremental.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814592"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="22602-103">System. Search. IsClosedDirectory</span><span class="sxs-lookup"><span data-stu-id="22602-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="22602-104">Emitido como **verdadeiro** por um item de contêiner para indicar que seus itens filho não precisam ser enumerados por um indexador se o item de contêiner não foi alterado desde o último rastreamento de verificação de índice incremental.</span><span class="sxs-lookup"><span data-stu-id="22602-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="22602-105">Isso contribui para a otimização do desempenho do indexador.</span><span class="sxs-lookup"><span data-stu-id="22602-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="22602-106">Nesses casos de contêiner (exemplos são um email com anexos ou um arquivo compactado com uma extensão de nome. zip), os itens filho são inseparáveis de seu item pai.</span><span class="sxs-lookup"><span data-stu-id="22602-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="22602-107">Por exemplo, se a propriedade [System. DateModified](./props-system-datemodified.md) de um item contido for alterada, o valor System. DateModified do contêiner será alterado para Matching.</span><span class="sxs-lookup"><span data-stu-id="22602-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="22602-108">Além disso, se um item pai for excluído, todos os itens filho também serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="22602-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="22602-109">Portanto, se o contêiner não tiver sido alterado, o indexador saberá que nada dentro dele foi alterado e não precisa abrir o contêiner para examinar o conteúdo individualmente.</span><span class="sxs-lookup"><span data-stu-id="22602-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="22602-110">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22602-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="22602-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="22602-111">Remarks</span></span>

<span data-ttu-id="22602-112">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="22602-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="22602-113">Se um item emitir **true** para essa propriedade, cada um de seus itens filho deverá emitir a propriedade [System. Search. IsFullyContained](./props-system-search-isfullycontained.md) como **true** para impedir que esses itens sejam excluídos do índice.</span><span class="sxs-lookup"><span data-stu-id="22602-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="22602-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22602-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22602-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="22602-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="22602-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="22602-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="22602-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="22602-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="22602-118">typeInfo</span><span class="sxs-lookup"><span data-stu-id="22602-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="22602-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="22602-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="22602-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="22602-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="22602-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="22602-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="22602-122">numberFormat</span><span class="sxs-lookup"><span data-stu-id="22602-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="22602-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="22602-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="22602-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="22602-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="22602-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="22602-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="22602-126">editControl</span><span class="sxs-lookup"><span data-stu-id="22602-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="22602-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="22602-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="22602-128">queryControl</span><span class="sxs-lookup"><span data-stu-id="22602-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
