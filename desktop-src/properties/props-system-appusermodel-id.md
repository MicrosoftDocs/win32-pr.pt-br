---
description: Um AppUserModelID (ID do modelo de usuário) do aplicativo explícito usado para associar processos, arquivos e janelas a um aplicativo específico.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296605"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="3ca49-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="3ca49-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="3ca49-104">Um AppUserModelID (ID do modelo de usuário) do aplicativo explícito usado para associar processos, arquivos e janelas a um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="3ca49-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="3ca49-105">Em alguns casos, é suficiente contar com o AppUserModelID interno atribuído a um processo pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="3ca49-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="3ca49-106">No entanto, um aplicativo que possui vários processos ou um aplicativo que está sendo executado em um processo de host pode precisar se identificar explicitamente por meio dessa propriedade para que ele possa agrupar suas janelas diferentes em um único botão da barra de tarefas e controlar o conteúdo da lista de atalhos desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3ca49-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="3ca49-107">Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System.AppUserModel.ID]() dessa janela.</span><span class="sxs-lookup"><span data-stu-id="3ca49-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="3ca49-108">Para obter mais informações, consulte [IDs de modelo de usuário de aplicativo (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="3ca49-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="3ca49-109">No momento em que a propriedade [System.AppUserModel.ID]() é definida, a barra de tarefas é notificada para atualizar suas informações na janela ou no atalho dado a este AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="3ca49-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="3ca49-110">Outras propriedades de janela e de atalho podem ser usadas em conjunto com um AppUserModelID explícito para controlar ainda mais o agrupamento e a fixação associados a uma janela, o nome de exibição e o ícone usado para ele na barra de tarefas e o comando para iniciar um aplicativo fixado na barra de tarefas ou uma nova instância do aplicativo por meio da lista de atalhos desse aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3ca49-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="3ca49-111">Essas propriedades devem ser definidas antes da definição da propriedade [System.AppUserModel.ID]() .</span><span class="sxs-lookup"><span data-stu-id="3ca49-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="3ca49-112">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="3ca49-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3ca49-113">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="3ca49-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="3ca49-114">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="3ca49-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="3ca49-115">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="3ca49-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="3ca49-116">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="3ca49-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="3ca49-117">Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="3ca49-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="3ca49-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ca49-118">Remarks</span></span>

<span data-ttu-id="3ca49-119">Os valores de PKEY são definidos em Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="3ca49-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ca49-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ca49-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ca49-121">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="3ca49-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="3ca49-122">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="3ca49-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="3ca49-123">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="3ca49-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="3ca49-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3ca49-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3ca49-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3ca49-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3ca49-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3ca49-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3ca49-127">typeInfo</span><span class="sxs-lookup"><span data-stu-id="3ca49-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3ca49-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3ca49-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3ca49-129">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="3ca49-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="3ca49-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3ca49-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3ca49-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3ca49-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3ca49-132">numberFormat</span><span class="sxs-lookup"><span data-stu-id="3ca49-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3ca49-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3ca49-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3ca49-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3ca49-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3ca49-135">enumera</span><span class="sxs-lookup"><span data-stu-id="3ca49-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="3ca49-136">enumRange</span><span class="sxs-lookup"><span data-stu-id="3ca49-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="3ca49-137">imagem</span><span class="sxs-lookup"><span data-stu-id="3ca49-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="3ca49-138">drawControl</span><span class="sxs-lookup"><span data-stu-id="3ca49-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3ca49-139">editControl</span><span class="sxs-lookup"><span data-stu-id="3ca49-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3ca49-140">filterControl</span><span class="sxs-lookup"><span data-stu-id="3ca49-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3ca49-141">queryControl</span><span class="sxs-lookup"><span data-stu-id="3ca49-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="3ca49-142">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="3ca49-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="3ca49-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="3ca49-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
