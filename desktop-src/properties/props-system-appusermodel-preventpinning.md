---
description: Desabilita a capacidade de um atalho ou janela ser fixado na barra de tarefas ou no menu iniciar. Essa propriedade também torna o item inelegível para inclusão na lista de usados com mais frequência (MFU) do menu iniciar.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828612"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="8bf3a-104">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="8bf3a-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="8bf3a-105">Desabilita a capacidade de um atalho ou janela ser fixado na barra de tarefas ou no menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="8bf3a-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="8bf3a-106">Essa propriedade também torna o item inelegível para inclusão na lista de usados com mais frequência (MFU) do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="8bf3a-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="8bf3a-107">Essa propriedade deve ser definida em uma janela antes da propriedade de [ \_ \_ ID PKEY AppUserModel](./props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf3a-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="8bf3a-108">Depois que a \_ propriedade de ID PKEY AppUserModel \_ for definida, as alterações em [PKEY \_ AppUserModel \_ PreventPinning]() serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="8bf3a-109">Para obter mais informações sobre AppUserModelIDs (IDs de modelo de usuário do aplicativo) e outros métodos de exclusão de um item para ser fixado na barra de tarefas e da inclusão de MFU, consulte [IDs de modelo de usuário de aplicativo (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="8bf3a-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="8bf3a-110">Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. PreventPinning]() dessa janela.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="8bf3a-111">Definir essa propriedade faz com que as seguintes propriedades sejam ignoradas:</span><span class="sxs-lookup"><span data-stu-id="8bf3a-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="8bf3a-112">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="8bf3a-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="8bf3a-113">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="8bf3a-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="8bf3a-114">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="8bf3a-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="8bf3a-115">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bf3a-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="8bf3a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bf3a-116">Remarks</span></span>

<span data-ttu-id="8bf3a-117">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="8bf3a-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bf3a-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf3a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf3a-119">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="8bf3a-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="8bf3a-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-121">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="8bf3a-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="8bf3a-122">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="8bf3a-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="8bf3a-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="8bf3a-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="8bf3a-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-126">typeInfo</span><span class="sxs-lookup"><span data-stu-id="8bf3a-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8bf3a-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-128">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="8bf3a-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="8bf3a-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="8bf3a-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-131">numberFormat</span><span class="sxs-lookup"><span data-stu-id="8bf3a-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8bf3a-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="8bf3a-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-134">enumera</span><span class="sxs-lookup"><span data-stu-id="8bf3a-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-135">enumRange</span><span class="sxs-lookup"><span data-stu-id="8bf3a-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-136">imagem</span><span class="sxs-lookup"><span data-stu-id="8bf3a-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="8bf3a-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-138">editControl</span><span class="sxs-lookup"><span data-stu-id="8bf3a-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="8bf3a-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="8bf3a-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-141">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="8bf3a-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="8bf3a-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="8bf3a-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
