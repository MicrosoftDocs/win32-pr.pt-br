---
description: Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixação na barra de tarefas ou para inclusão na lista de uso mais frequente (MFU) do menu iniciar.
title: Como excluir itens da fixação da barra de tarefas e listas recentes/frequentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967903"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="1aaaf-103">Como excluir itens da fixação da barra de tarefas e listas recentes/frequentes</span><span class="sxs-lookup"><span data-stu-id="1aaaf-103">How to Exclude Items from Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="1aaaf-104">Aplicativos, processos e janelas podem optar por se tornar indisponíveis para fixação na barra de tarefas ou para inclusão na lista de uso mais frequente (MFU) do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="1aaaf-104">Applications, processes, and windows can opt to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

## <a name="instructions"></a><span data-ttu-id="1aaaf-105">Instruções</span><span class="sxs-lookup"><span data-stu-id="1aaaf-105">Instructions</span></span>


<span data-ttu-id="1aaaf-106">Há três mecanismos para realizar a exclusão de itens da fixação da barra de tarefas e de listas recentes/frequentes:</span><span class="sxs-lookup"><span data-stu-id="1aaaf-106">There are three mechanisms to accomplish the exclusion of items from taskbar pinning and recent/frequent lists:</span></span>

-   <span data-ttu-id="1aaaf-107">Adicione a entrada NoStartPage ao registro do aplicativo, conforme mostrado neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="1aaaf-107">Add the NoStartPage entry to the application's registration as shown in this example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="1aaaf-108">Os dados associados à entrada NoStartPage são ignorados.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-108">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="1aaaf-109">Somente a presença da entrada é necessária.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-109">Only the presence of the entry is required.</span></span> <span data-ttu-id="1aaaf-110">Portanto, o tipo ideal para NoStartPage é **reg \_ None**.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-110">Therefore, the ideal type for NoStartPage is **REG\_NONE**.</span></span>

    <span data-ttu-id="1aaaf-111">Observe que qualquer uso de uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) substitui a entrada NoStartPage.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-111">Note that any use of an explicit Application User Model ID (AppUserModelID) overrides the NoStartPage entry.</span></span> <span data-ttu-id="1aaaf-112">Se um AppUserModelID explícito for aplicado a um atalho, processo ou janela, ele se tornará fixas e elegível para a lista MFU do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="1aaaf-112">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

-   <span data-ttu-id="1aaaf-113">Defina a propriedade [System. AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) no Windows e nos atalhos.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-113">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="1aaaf-114">Essa propriedade deve ser definida em uma janela antes de a propriedade de [ \_ \_ ID PKEY AppUserModel](../properties/props-system-appusermodel-id.md) ser definida.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-114">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property is set.</span></span>
-   <span data-ttu-id="1aaaf-115">Adicione um AppUserModelID explícito como um valor na seguinte subchave do registro, conforme mostrado neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="1aaaf-115">Add an explicit AppUserModelID as a value under the following registry subkey as shown in this example:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="1aaaf-116">Cada entrada é um **valor \_ nulo reg** com o nome do AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-116">Each entry is a **REG\_NULL** value with the name of the AppUserModelID.</span></span> <span data-ttu-id="1aaaf-117">Qualquer AppUserModelID encontrado nessa lista não é fixas e não está qualificado para inclusão na lista de MFU do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="1aaaf-117">Any AppUserModelID that is found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

## <a name="remarks"></a><span data-ttu-id="1aaaf-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1aaaf-118">Remarks</span></span>

<span data-ttu-id="1aaaf-119">Lembre-se de que determinados arquivos executáveis, bem como os atalhos que contêm determinadas cadeias de caracteres em seus nomes, são excluídos automaticamente da fixação e inclusão na lista MFU.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-119">Be aware that certain executable files, as well as shortcuts that contain certain strings in their names, are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="1aaaf-120">Essa exclusão automática pode ser substituída com a aplicação de um AppUserModelID explícito.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-120">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="1aaaf-121">Se qualquer uma das cadeias de caracteres a seguir, independentemente do caso, estiver incluída no nome do atalho, o programa não será fixas e não será exibido na lista de usados com mais frequência (não aplicável ao Windows 10):</span><span class="sxs-lookup"><span data-stu-id="1aaaf-121">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="1aaaf-122">Documentação</span><span class="sxs-lookup"><span data-stu-id="1aaaf-122">Documentation</span></span>
-   <span data-ttu-id="1aaaf-123">Ajuda</span><span class="sxs-lookup"><span data-stu-id="1aaaf-123">Help</span></span>
-   <span data-ttu-id="1aaaf-124">Instalar</span><span class="sxs-lookup"><span data-stu-id="1aaaf-124">Install</span></span>
-   <span data-ttu-id="1aaaf-125">Mais informações</span><span class="sxs-lookup"><span data-stu-id="1aaaf-125">More Info</span></span>
-   <span data-ttu-id="1aaaf-126">Leia-me</span><span class="sxs-lookup"><span data-stu-id="1aaaf-126">Read me</span></span>
-   <span data-ttu-id="1aaaf-127">Leia primeiro</span><span class="sxs-lookup"><span data-stu-id="1aaaf-127">Read First</span></span>
-   <span data-ttu-id="1aaaf-128">Leiame</span><span class="sxs-lookup"><span data-stu-id="1aaaf-128">Readme</span></span>
-   <span data-ttu-id="1aaaf-129">Remover</span><span class="sxs-lookup"><span data-stu-id="1aaaf-129">Remove</span></span>
-   <span data-ttu-id="1aaaf-130">Instalação</span><span class="sxs-lookup"><span data-stu-id="1aaaf-130">Setup</span></span>
-   <span data-ttu-id="1aaaf-131">Suporte</span><span class="sxs-lookup"><span data-stu-id="1aaaf-131">Support</span></span>
-   <span data-ttu-id="1aaaf-132">What's New</span><span class="sxs-lookup"><span data-stu-id="1aaaf-132">What's New</span></span>

<span data-ttu-id="1aaaf-133">A lista de programas a seguir não é fixas e é excluída da lista de usados com mais frequência:</span><span class="sxs-lookup"><span data-stu-id="1aaaf-133">The following list of programs are not pinnable and are excluded from the most frequently used list:</span></span>

-   <span data-ttu-id="1aaaf-134">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-134">Applaunch.exe</span></span>
-   <span data-ttu-id="1aaaf-135">Control.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-135">Control.exe</span></span>
-   <span data-ttu-id="1aaaf-136">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-136">Dfsvc.exe</span></span>
-   <span data-ttu-id="1aaaf-137">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-137">Dllhost.exe</span></span>
-   <span data-ttu-id="1aaaf-138">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-138">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="1aaaf-139">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-139">Hh.exe</span></span>
-   <span data-ttu-id="1aaaf-140">Install.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-140">Install.exe</span></span>
-   <span data-ttu-id="1aaaf-141">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-141">Isuninst.exe</span></span>
-   <span data-ttu-id="1aaaf-142">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-142">Lnkstub.exe</span></span>
-   <span data-ttu-id="1aaaf-143">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-143">Mmc.exe</span></span>
-   <span data-ttu-id="1aaaf-144">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-144">Mshta.exe</span></span>
-   <span data-ttu-id="1aaaf-145">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-145">Msiexec.exe</span></span>
-   <span data-ttu-id="1aaaf-146">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-146">Msoobe.exe</span></span>
-   <span data-ttu-id="1aaaf-147">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-147">Rundll32.exe</span></span>
-   <span data-ttu-id="1aaaf-148">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-148">Setup.exe</span></span>
-   <span data-ttu-id="1aaaf-149">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-149">St5unst.exe</span></span>
-   <span data-ttu-id="1aaaf-150">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-150">Unwise.exe</span></span>
-   <span data-ttu-id="1aaaf-151">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-151">Unwise32.exe</span></span>
-   <span data-ttu-id="1aaaf-152">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-152">Werfault.exe</span></span>
-   <span data-ttu-id="1aaaf-153">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-153">Winhlp32.exe</span></span>
-   <span data-ttu-id="1aaaf-154">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-154">Wlrmdr.exe</span></span>
-   <span data-ttu-id="1aaaf-155">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="1aaaf-155">Wuapp.exe</span></span>

<span data-ttu-id="1aaaf-156">As listas anteriores são armazenadas nos valores de registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-156">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="1aaaf-157">Essas listas não devem ser modificadas por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-157">These lists should not be modified by applications.</span></span> <span data-ttu-id="1aaaf-158">Use um dos métodos de lista de exclusão descritos anteriormente neste tópico para a mesma experiência.</span><span class="sxs-lookup"><span data-stu-id="1aaaf-158">Use one of the exclusion list methods described earlier in this topic for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="1aaaf-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1aaaf-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aaaf-160">A barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="1aaaf-160">The Taskbar</span></span>](taskbar.md)
</dt> <dt>

[<span data-ttu-id="1aaaf-161">Extensões da barra de tarefas</span><span class="sxs-lookup"><span data-stu-id="1aaaf-161">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 
