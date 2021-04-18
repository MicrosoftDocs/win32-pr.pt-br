---
description: Especifica o ícone usado para o atalho criado na barra de tarefas quando o usuário escolhe fixar um aplicativo na barra de tarefas ou iniciar uma nova instância por meio da lista de atalhos do botão.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756520"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="8bfdc-103">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="8bfdc-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="8bfdc-104">Especifica o ícone usado para o atalho criado na barra de tarefas quando o usuário escolhe fixar um aplicativo na barra de tarefas ou iniciar uma nova instância por meio da lista de atalhos do botão.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="8bfdc-105">Esse é o ícone usado para o grupo da barra de tarefas e é mostrado para um aplicativo fixado, independentemente de o aplicativo estar em execução ou não.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="8bfdc-106">Isso deve ser especificado em um dos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="8bfdc-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="8bfdc-107">Formato de recurso padrão, como "% systemdir% \\ system32 \\shell32.dll,-128".</span><span class="sxs-lookup"><span data-stu-id="8bfdc-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="8bfdc-108">O caractere '-' antes da ID do recurso é necessário.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="8bfdc-109">Não use o caractere ' @ ' na frente da cadeia de caracteres do caminho.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="8bfdc-110">Caminho direto para um arquivo de ícone, como "% ProgramFiles% \\ Microsoft \\ notepad \\ Notepad. ico, 0".</span><span class="sxs-lookup"><span data-stu-id="8bfdc-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="8bfdc-111">Observe que, como os arquivos. ico podem conter vários recursos de ícone, uma ID de recurso é necessária na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="8bfdc-112">Se o arquivo. ico for uma única imagem, use "0" (sem o caractere "-") como a ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="8bfdc-113">[System. AppUserModel. RelaunchIconResource]() é uma propriedade opcional.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="8bfdc-114">Se não estiver definido, o ícone do destino do comando de reinicialização ([System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) será usado.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="8bfdc-115">No entanto, como isso pode levar a resultados indesejados, é altamente recomendável que você forneça um ícone explicitamente por meio dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="8bfdc-116">Essa propriedade só será usada se uma janela tiver uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), definida por meio de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="8bfdc-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="8bfdc-117">Se a janela não tiver um AppUserModelID explícito (System.AppUserModel.ID), essa propriedade será ignorada e a janela será agrupada e fixada como se fosse parte de seu processo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="8bfdc-118">Para obter mais informações sobre a aplicação de AppUserModelIDs explícitas e seu efeito na fixação da barra de tarefas, consulte [IDs do modelo de usuário do aplicativo (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="8bfdc-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="8bfdc-119">Essa propriedade deve ser usada por aplicativos ou Windows que desejem fornecer informações de reinicialização não padrão.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="8bfdc-120">Para obter mais informações, consulte [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="8bfdc-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="8bfdc-121">Se um AppUserModelID explícito for definido na janela, mas essa propriedade não estiver definida, o sistema tentará localizar um atalho com o mesmo AppUserModelID e fixará esse atalho na barra de tarefas para representar a janela.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="8bfdc-122">Se esse atalho não puder ser localizado, o executável de backup do processo que o possui será usado.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="8bfdc-123">Essa propriedade será ignorada se [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) for definido.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="8bfdc-124">Isso permite que um aplicativo controle o agrupamento de suas janelas atribuindo-lhes AppUserModelIDs explícitas, mas impedindo que essas janelas sejam fixadas.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="8bfdc-125">Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. RelaunchIconResource]() dessa janela.</span><span class="sxs-lookup"><span data-stu-id="8bfdc-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="8bfdc-126">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8bfdc-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="8bfdc-127">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bfdc-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="8bfdc-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bfdc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bfdc-129">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="8bfdc-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="8bfdc-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-131">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="8bfdc-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="8bfdc-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="8bfdc-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="8bfdc-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-135">typeInfo</span><span class="sxs-lookup"><span data-stu-id="8bfdc-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="8bfdc-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-137">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="8bfdc-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="8bfdc-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="8bfdc-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-140">numberFormat</span><span class="sxs-lookup"><span data-stu-id="8bfdc-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="8bfdc-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="8bfdc-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-143">enumera</span><span class="sxs-lookup"><span data-stu-id="8bfdc-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-144">enumRange</span><span class="sxs-lookup"><span data-stu-id="8bfdc-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-145">imagem</span><span class="sxs-lookup"><span data-stu-id="8bfdc-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-146">drawControl</span><span class="sxs-lookup"><span data-stu-id="8bfdc-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-147">editControl</span><span class="sxs-lookup"><span data-stu-id="8bfdc-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-148">filterControl</span><span class="sxs-lookup"><span data-stu-id="8bfdc-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-149">queryControl</span><span class="sxs-lookup"><span data-stu-id="8bfdc-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-150">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="8bfdc-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="8bfdc-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="8bfdc-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
