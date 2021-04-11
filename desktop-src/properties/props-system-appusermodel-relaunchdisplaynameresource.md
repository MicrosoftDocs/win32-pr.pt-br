---
description: Especifica o nome de exibição usado para o atalho criado na barra de tarefas quando o usuário opta por fixar um aplicativo na barra de tarefas ou iniciar uma nova instância na lista de atalhos de seu botão.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169586"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="01e12-103">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="01e12-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="01e12-104">Especifica o nome de exibição usado para o atalho criado na barra de tarefas quando o usuário opta por fixar um aplicativo na barra de tarefas ou iniciar uma nova instância na lista de atalhos de seu botão.</span><span class="sxs-lookup"><span data-stu-id="01e12-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="01e12-105">O valor dessa propriedade deve ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="01e12-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="01e12-106">Uma cadeia de caracteres de recurso indireto, como "@% systemdir% \\ system32 \\shell32.dll,-19263".</span><span class="sxs-lookup"><span data-stu-id="01e12-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="01e12-107">Observe que o caractere ' @ ' é necessário para distinguir uma cadeia de caracteres indireta de uma cadeia de caracteres de texto sem formatação (descrita no próximo parágrafo com marcadores).</span><span class="sxs-lookup"><span data-stu-id="01e12-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="01e12-108">Essa cadeia de caracteres indireta consiste em um arquivo binário e uma ID de recurso da cadeia de caracteres contida nesse binário.</span><span class="sxs-lookup"><span data-stu-id="01e12-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="01e12-109">É altamente recomendável que você use esse formulário de cadeia de caracteres indireta, o que garante que o nome de exibição seja alterado adequadamente quando o idioma do sistema for alterado por meio da MUI (Multilingual User interface).</span><span class="sxs-lookup"><span data-stu-id="01e12-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="01e12-110">O caractere '-' antes da ID do recurso é necessário.</span><span class="sxs-lookup"><span data-stu-id="01e12-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="01e12-111">Uma cadeia de caracteres de texto sem formatação que não aponta para um recurso.</span><span class="sxs-lookup"><span data-stu-id="01e12-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="01e12-112">Isso só deve ser usado quando o nome de exibição é dinamicamente calculado ou obtido de uma fonte de dados que não oferece suporte a MUI.</span><span class="sxs-lookup"><span data-stu-id="01e12-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="01e12-113">Por exemplo, a cadeia de caracteres pode ser o nome de um dispositivo, como "Microsoft Zune", em casos em que o aplicativo aparece quando o dispositivo é anexado ao computador.</span><span class="sxs-lookup"><span data-stu-id="01e12-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="01e12-114">[System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) e [System. AppUserModel. RelaunchDisplayNameResource]() devem sempre ser definidos juntos.</span><span class="sxs-lookup"><span data-stu-id="01e12-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="01e12-115">Se uma dessas propriedades não for definida, nenhuma será usada.</span><span class="sxs-lookup"><span data-stu-id="01e12-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="01e12-116">Essa propriedade só será usada se uma janela tiver uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), definida por meio de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="01e12-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="01e12-117">Se a janela não tiver um AppUserModelID explícito, essa propriedade será ignorada e a janela será agrupada e fixada como se fosse parte do processo que a possui.</span><span class="sxs-lookup"><span data-stu-id="01e12-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="01e12-118">Para obter mais informações sobre a aplicação de AppUserModelIDs explícitas e seu efeito na fixação da barra de tarefas, consulte [IDs do modelo de usuário do aplicativo (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="01e12-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="01e12-119">Essa propriedade deve ser usada por aplicativos ou Windows que desejem fornecer informações de reinicialização não padrão.</span><span class="sxs-lookup"><span data-stu-id="01e12-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="01e12-120">Para obter mais informações, consulte [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="01e12-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="01e12-121">Essa propriedade será ignorada se [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) for definido.</span><span class="sxs-lookup"><span data-stu-id="01e12-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="01e12-122">Isso permite que um aplicativo controle o agrupamento de suas janelas atribuindo-lhes AppUserModelIDs explícitas, mas impedindo que essas janelas sejam fixadas.</span><span class="sxs-lookup"><span data-stu-id="01e12-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="01e12-123">Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. RelaunchDisplayNameResource]() dessa janela.</span><span class="sxs-lookup"><span data-stu-id="01e12-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="01e12-124">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="01e12-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="01e12-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="01e12-125">Remarks</span></span>

<span data-ttu-id="01e12-126">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="01e12-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01e12-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="01e12-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01e12-128">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="01e12-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="01e12-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="01e12-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="01e12-130">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="01e12-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="01e12-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="01e12-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="01e12-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="01e12-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="01e12-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="01e12-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="01e12-134">typeInfo</span><span class="sxs-lookup"><span data-stu-id="01e12-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="01e12-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="01e12-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="01e12-136">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="01e12-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="01e12-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="01e12-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="01e12-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="01e12-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="01e12-139">numberFormat</span><span class="sxs-lookup"><span data-stu-id="01e12-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="01e12-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="01e12-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="01e12-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="01e12-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="01e12-142">enumera</span><span class="sxs-lookup"><span data-stu-id="01e12-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="01e12-143">enumRange</span><span class="sxs-lookup"><span data-stu-id="01e12-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="01e12-144">imagem</span><span class="sxs-lookup"><span data-stu-id="01e12-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="01e12-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="01e12-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="01e12-146">editControl</span><span class="sxs-lookup"><span data-stu-id="01e12-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="01e12-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="01e12-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="01e12-148">queryControl</span><span class="sxs-lookup"><span data-stu-id="01e12-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="01e12-149">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="01e12-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="01e12-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="01e12-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
