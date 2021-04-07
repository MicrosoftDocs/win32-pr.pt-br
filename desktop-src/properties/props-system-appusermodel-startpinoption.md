---
description: Defina essa propriedade em um atalho como (1) impedir que um aplicativo seja fixado automaticamente na tela inicial após a instalação; ou (2) indicar que um item é adicionado programaticamente ao iniciador por meio de ação do usuário (que implica automaticamente fixar para iniciar e excluir em Desafixar).
ms.assetid: 247ad0a6-ce65-45f1-a0d5-51ad135000aa
title: System. AppUserModel. StartPinOption
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cdef82a90488ce87bbf182323b00d62a5cdfea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827781"
---
# <a name="systemappusermodelstartpinoption"></a><span data-ttu-id="1d382-103">System. AppUserModel. StartPinOption</span><span class="sxs-lookup"><span data-stu-id="1d382-103">System.AppUserModel.StartPinOption</span></span>

<span data-ttu-id="1d382-104">Defina essa propriedade em um atalho como (1) impedir que um aplicativo seja fixado automaticamente na tela inicial após a instalação; ou (2) indicar que um item é adicionado programaticamente ao iniciador por meio de ação do usuário (que implica automaticamente fixar para iniciar e excluir em Desafixar).</span><span class="sxs-lookup"><span data-stu-id="1d382-104">Set this property on a shortcut to (1) prevent an application from being automatically pinned to Start screen upon installation; or(2) indicate that an item is programmatically added to launcher via user action (which implies automatically pin to Start and delete on unpin).</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="1d382-105">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="1d382-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.AppUserModel.StartPinOption
   shellPKey = PKEY_AppUserModel_StartPinOption
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = false
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Default
            value = 0
            text = Default
            defineToken = APPUSERMODEL_STARTPINOPTION_DEFAULT
         enum
            name = NoPinOnInstall
            value = 1
            text = NoPinOnInstall
            defineToken = APPUSERMODEL_STARTPINOPTION_NOPINONINSTALL
         enum
            name = UserPinned
            value = 2
            text = UserPinned
            defineToken = APPUSERMODEL_STARTPINOPTION_USERPINNED
```

## <a name="remarks"></a><span data-ttu-id="1d382-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d382-106">Remarks</span></span>

<span data-ttu-id="1d382-107">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="1d382-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d382-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d382-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d382-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1d382-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1d382-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1d382-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1d382-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1d382-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1d382-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="1d382-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1d382-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1d382-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1d382-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1d382-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1d382-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1d382-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1d382-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="1d382-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1d382-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1d382-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1d382-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1d382-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1d382-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="1d382-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1d382-120">editControl</span><span class="sxs-lookup"><span data-stu-id="1d382-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1d382-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="1d382-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1d382-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="1d382-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
