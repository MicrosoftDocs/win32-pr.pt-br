---
description: Especifica um comando que pode ser executado por meio de ShellExecute para iniciar um aplicativo quando ele é fixado na barra de tarefas ou quando uma nova instância do aplicativo é iniciada por meio da lista de atalhos do aplicativo.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771511"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="40b5a-103">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="40b5a-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="40b5a-104">Especifica um comando que pode ser executado por meio de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar um aplicativo quando ele é fixado na barra de tarefas ou quando uma nova instância do aplicativo é iniciada por meio da lista de atalhos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40b5a-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="40b5a-105">Os exemplos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="40b5a-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="40b5a-106">Essa propriedade só será usada se uma janela tiver uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), definida por meio de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="40b5a-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="40b5a-107">Se a janela não tiver um AppUserModelID explícito, essa propriedade será ignorada e a janela será agrupada e fixada como se fosse parte do processo que a possui.</span><span class="sxs-lookup"><span data-stu-id="40b5a-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="40b5a-108">Para obter mais informações sobre a aplicação de AppUserModelIDs explícitas e seu efeito na fixação da barra de tarefas, consulte [IDs do modelo de usuário do aplicativo (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="40b5a-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="40b5a-109">Essa propriedade deve ser usada por aplicativos ou Windows que desejem fornecer informações de reinicialização não padrão.</span><span class="sxs-lookup"><span data-stu-id="40b5a-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="40b5a-110">[System. AppUserModel. RelaunchCommand]() e [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) devem sempre ser definidos juntos.</span><span class="sxs-lookup"><span data-stu-id="40b5a-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="40b5a-111">Se uma dessas propriedades não for definida, nenhuma será usada.</span><span class="sxs-lookup"><span data-stu-id="40b5a-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="40b5a-112">Essa propriedade, junto com [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) e [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) , pode ser usada para definir visualmente uma janela como um aplicativo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="40b5a-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="40b5a-113">Isso é útil para cenários de aplicativos host, em que uma única instância de host executa vários aplicativos filho.</span><span class="sxs-lookup"><span data-stu-id="40b5a-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="40b5a-114">Por exemplo, uma máquina virtual que hospeda vários aplicativos virtualizados pode querer que esses aplicativos virtualizados apareçam como aplicativos individuais para o usuário.</span><span class="sxs-lookup"><span data-stu-id="40b5a-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="40b5a-115">A máquina virtual pode rotular cada janela com um AppUserModelID explícito e as propriedades de reinicialização apropriadas para torná-los exibidos como aplicativos.</span><span class="sxs-lookup"><span data-stu-id="40b5a-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="40b5a-116">O usuário poderia fixá-los na barra de tarefas e "reinicializar" a instância fixada.</span><span class="sxs-lookup"><span data-stu-id="40b5a-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="40b5a-117">Essa propriedade será ignorada se [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) for definido.</span><span class="sxs-lookup"><span data-stu-id="40b5a-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="40b5a-118">Isso permite que um aplicativo controle o agrupamento de suas janelas atribuindo-lhes AppUserModelIDs explícitas, mas impedindo que essas janelas sejam fixadas.</span><span class="sxs-lookup"><span data-stu-id="40b5a-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="40b5a-119">Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. RelaunchCommand]() dessa janela.</span><span class="sxs-lookup"><span data-stu-id="40b5a-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="40b5a-120">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="40b5a-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="40b5a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="40b5a-121">Remarks</span></span>

<span data-ttu-id="40b5a-122">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="40b5a-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40b5a-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40b5a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40b5a-124">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="40b5a-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="40b5a-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="40b5a-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="40b5a-126">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="40b5a-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="40b5a-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="40b5a-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="40b5a-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="40b5a-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="40b5a-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="40b5a-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="40b5a-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="40b5a-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="40b5a-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="40b5a-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="40b5a-132">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="40b5a-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="40b5a-133">stringFormat</span><span class="sxs-lookup"><span data-stu-id="40b5a-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="40b5a-134">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="40b5a-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="40b5a-135">numberFormat</span><span class="sxs-lookup"><span data-stu-id="40b5a-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="40b5a-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="40b5a-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="40b5a-137">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="40b5a-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="40b5a-138">enumera</span><span class="sxs-lookup"><span data-stu-id="40b5a-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="40b5a-139">enumRange</span><span class="sxs-lookup"><span data-stu-id="40b5a-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="40b5a-140">imagem</span><span class="sxs-lookup"><span data-stu-id="40b5a-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="40b5a-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="40b5a-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="40b5a-142">editControl</span><span class="sxs-lookup"><span data-stu-id="40b5a-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="40b5a-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="40b5a-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="40b5a-144">queryControl</span><span class="sxs-lookup"><span data-stu-id="40b5a-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="40b5a-145">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="40b5a-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="40b5a-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="40b5a-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
