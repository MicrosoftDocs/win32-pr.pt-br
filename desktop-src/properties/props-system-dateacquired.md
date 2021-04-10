---
description: A data de aquisição do arquivo ou da mídia.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a85f36df252202c319e90460807e16fefa3d559a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171575"
---
# <a name="systemdateacquired"></a><span data-ttu-id="a5812-103">System. DateAcquired</span><span class="sxs-lookup"><span data-stu-id="a5812-103">System.DateAcquired</span></span>

<span data-ttu-id="a5812-104">A data de aquisição do arquivo ou da mídia.</span><span class="sxs-lookup"><span data-stu-id="a5812-104">The acquisition date of the file or media.</span></span> <span data-ttu-id="a5812-105">Essa propriedade está relacionada a um usuário ou grupo de usuários específico.</span><span class="sxs-lookup"><span data-stu-id="a5812-105">This property is related to a particular user or group of users.</span></span> <span data-ttu-id="a5812-106">Por exemplo, esses dados são usados como o principal eixo de classificação para a pasta virtual **nova música**, o que permite às pessoas procurar as últimas adições à sua coleção.</span><span class="sxs-lookup"><span data-stu-id="a5812-106">For example, this data is used as the main sorting axis for the virtual folder **New Music**, which enables people to browse the latest additions to their collection.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a5812-107">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a5812-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a><span data-ttu-id="a5812-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5812-108">Windows Vista</span></span>

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a><span data-ttu-id="a5812-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5812-109">Remarks</span></span>

<span data-ttu-id="a5812-110">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="a5812-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="a5812-111">[DateAcquired]() é armazenado como um valor no fluxo principal do arquivo, mas talvez nem sempre esteja presente.</span><span class="sxs-lookup"><span data-stu-id="a5812-111">[DateAcquired]() is stored as a value in the main stream of the file, but it may not always be present.</span></span> <span data-ttu-id="a5812-112">Nessas instâncias, a data de aquisição pode ser aproximada com base em outras datas conhecidas para o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a5812-112">In those instances, the acquisition date can be approximated based on other known dates for the content.</span></span> <span data-ttu-id="a5812-113">O manipulador de metadados deve usar um conjunto de regras para determinar a data a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="a5812-113">The metadata handler should use a set of rules to determine the date to return.</span></span> <span data-ttu-id="a5812-114">O exemplo a seguir demonstra isso para arquivos de música.</span><span class="sxs-lookup"><span data-stu-id="a5812-114">The following example demonstrates this for music files.</span></span>

-   <span data-ttu-id="a5812-115">Para música adquirida, o tempo de criação do arquivo deve ser usado se nenhuma data de aquisição estiver presente.</span><span class="sxs-lookup"><span data-stu-id="a5812-115">For purchased music, the file's creation time should be used if no acquired date is present.</span></span> <span data-ttu-id="a5812-116">No entanto, o provedor de download deve definir a propriedade [DateAcquired]() no arquivo.</span><span class="sxs-lookup"><span data-stu-id="a5812-116">However, the download provider should set the [DateAcquired]() property in the file.</span></span>
-   <span data-ttu-id="a5812-117">Para arquivos de música que o usuário ou o grupo "copiou" (copiando música ou vídeo de um CD ou DVD para um disco rígido), a data de aquisição deve ser a data em que a ação foi realizada.</span><span class="sxs-lookup"><span data-stu-id="a5812-117">For music files that the user or group "ripped" (copying music or video from a CD or DVD to a hard disk), the acquisition date should be the date that action took place.</span></span> <span data-ttu-id="a5812-118">Por exemplo, o atributo [WM/encodingtime](../wmp/wm-encodingtime-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a5812-118">For instance, the [WM/EncodingTime](../wmp/wm-encodingtime-attribute.md) attribute.</span></span>
-   <span data-ttu-id="a5812-119">Para música copiada de outro local, a hora de criação do arquivo deve ser usada como a data de aquisição.</span><span class="sxs-lookup"><span data-stu-id="a5812-119">For music copied from another location, the file's creation time should be used as the acquisition date.</span></span>

<span data-ttu-id="a5812-120">Exemplos de [System. DateAcquired]() são a data e a hora em que as imagens são adquiridas de uma câmera ou quando a música é comprada online.</span><span class="sxs-lookup"><span data-stu-id="a5812-120">Examples of [System.DateAcquired]() are the date and time when pictures are acquired from a camera or when music is purchased online.</span></span> <span data-ttu-id="a5812-121">Isso não é o mesmo que [System. DateImported](./props-system-dateimported.md).</span><span class="sxs-lookup"><span data-stu-id="a5812-121">This is not the same as [System.DateImported](./props-system-dateimported.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5812-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5812-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5812-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a5812-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a5812-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a5812-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a5812-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a5812-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a5812-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a5812-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a5812-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a5812-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a5812-128">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a5812-128">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a5812-129">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a5812-129">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a5812-130">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a5812-130">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a5812-131">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a5812-131">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a5812-132">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a5812-132">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a5812-133">drawControl</span><span class="sxs-lookup"><span data-stu-id="a5812-133">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a5812-134">editControl</span><span class="sxs-lookup"><span data-stu-id="a5812-134">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a5812-135">filterControl</span><span class="sxs-lookup"><span data-stu-id="a5812-135">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a5812-136">queryControl</span><span class="sxs-lookup"><span data-stu-id="a5812-136">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
