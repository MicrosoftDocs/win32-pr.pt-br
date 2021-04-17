---
description: Mostra como usar as interfaces VSS para criar um provedor de hardware VSS.
ms.assetid: 4d3c3f3c-22d2-4246-afef-aee2a0bd52d6
title: Ferramenta VssSampleProvider e exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fceaa65b851e5469a3e82323da92d8bde0651a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763408"
---
# <a name="vsssampleprovider-tool-and-sample"></a><span data-ttu-id="44acf-103">Ferramenta VssSampleProvider e exemplo</span><span class="sxs-lookup"><span data-stu-id="44acf-103">VssSampleProvider Tool and Sample</span></span>

<span data-ttu-id="44acf-104">Mostra como usar as [interfaces](volume-shadow-copy-api-interfaces.md) VSS para criar um provedor de hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="44acf-104">Shows how to use the VSS [interfaces](volume-shadow-copy-api-interfaces.md) to create a VSS hardware provider.</span></span>

> [!Note]  
> <span data-ttu-id="44acf-105">A ferramenta VssSampleProvider e o exemplo estão incluídos no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="44acf-105">The VssSampleProvider tool and sample are included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="44acf-106">Você pode baixar o SDK do Windows do [SDK (Software Development Kit) do Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span><span class="sxs-lookup"><span data-stu-id="44acf-106">You can download the Windows SDK from [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk).</span></span>

 

<span data-ttu-id="44acf-107">Na instalação do SDK do Windows, a ferramenta VssSampleProvider pode ser encontrada em `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para o Windows de 64 bits) e `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para o windows de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="44acf-107">In the Windows SDK installation, the VssSampleProvider tool can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

> [!Note]  
> <span data-ttu-id="44acf-108">Os provedores de hardware só têm suporte em sistemas operacionais Windows Server.</span><span class="sxs-lookup"><span data-stu-id="44acf-108">Hardware providers are only supported on Windows Server operating systems.</span></span> <span data-ttu-id="44acf-109">Em um sistema operacional cliente Windows, você pode compilar o exemplo VssSampleProvider, mas não pode registrá-lo como um provedor de hardware.</span><span class="sxs-lookup"><span data-stu-id="44acf-109">On a Windows Client operating system, you can compile the VssSampleProvider sample, but you can't register it as a hardware provider.</span></span>

 

<span data-ttu-id="44acf-110">A ferramenta VssSampleProvider consiste nos seguintes arquivos:</span><span class="sxs-lookup"><span data-stu-id="44acf-110">The VssSampleProvider tool consists of the following files:</span></span>

-   <span data-ttu-id="44acf-111">Virtualstorage.sys</span><span class="sxs-lookup"><span data-stu-id="44acf-111">Virtualstorage.sys</span></span>
-   <span data-ttu-id="44acf-112">Vstorcontrol.exe</span><span class="sxs-lookup"><span data-stu-id="44acf-112">Vstorcontrol.exe</span></span>
-   <span data-ttu-id="44acf-113">Vssampleprovider.dll</span><span class="sxs-lookup"><span data-stu-id="44acf-113">Vssampleprovider.dll</span></span>
-   <span data-ttu-id="44acf-114">Vstorinterface.dll</span><span class="sxs-lookup"><span data-stu-id="44acf-114">Vstorinterface.dll</span></span>

<span data-ttu-id="44acf-115">O exemplo de VssSampleProvider inclui os seguintes scripts de instalação e desinstalação:</span><span class="sxs-lookup"><span data-stu-id="44acf-115">The VssSampleProvider sample includes the following installation and uninstallation scripts:</span></span>

-   <span data-ttu-id="44acf-116">Install-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="44acf-116">Install-sampleprovider.cmd</span></span>
-   <span data-ttu-id="44acf-117">Uninstall-SampleProvider. cmd</span><span class="sxs-lookup"><span data-stu-id="44acf-117">Uninstall-sampleprovider.cmd</span></span>
-   <span data-ttu-id="44acf-118">Registrar \_app.vbs</span><span class="sxs-lookup"><span data-stu-id="44acf-118">Register\_app.vbs</span></span>

<span data-ttu-id="44acf-119">**Para instalar e usar o exemplo de VssSampleProvider**</span><span class="sxs-lookup"><span data-stu-id="44acf-119">**To install and use the VssSampleProvider sample**</span></span>

1.  <span data-ttu-id="44acf-120">Navegue até o diretório `Program Files (x86)\Windows Kits\8.0\bin\`.</span><span class="sxs-lookup"><span data-stu-id="44acf-120">Navigate to the `Program Files (x86)\Windows Kits\8.0\bin\` directory.</span></span> <span data-ttu-id="44acf-121">Esse diretório contém virtualstoragevss.sys e vstorcontrol.exe.</span><span class="sxs-lookup"><span data-stu-id="44acf-121">This directory contains virtualstoragevss.sys and vstorcontrol.exe.</span></span>
2.  <span data-ttu-id="44acf-122">Abra uma janela de prompt de comando no diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="44acf-122">Open a command prompt window in the specified directory.</span></span>
3.  <span data-ttu-id="44acf-123">Para instalar o driver de armazenamento virtual, na janela do prompt de comando, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="44acf-123">To install the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe install
    ```

    

4.  <span data-ttu-id="44acf-124">Para instalar o provedor de exemplo do VSS, na janela do prompt de comando, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="44acf-124">To install the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    install-sampleprovider.cmd
    ```

    

5.  <span data-ttu-id="44acf-125">Para criar um LUN virtual, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="44acf-125">To create a virtual LUN, do the following.</span></span>

    1.  <span data-ttu-id="44acf-126">Na janela de prompt de comando, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="44acf-126">In the command prompt window, type the following command:</span></span>

        ```cmd
        vstorcontrol.exe create fixeddisk -
        newimage C:\disk1.image -size 20M -storid "VSS Sample HW Provider"
        ```

        

        <span data-ttu-id="44acf-127">Este comando cria um LUN virtual cujo identificador de armazenamento é um **provedor de HW de exemplo VSS**.</span><span class="sxs-lookup"><span data-stu-id="44acf-127">This command creates a virtual LUN whose storage identifier is **VSS Sample HW Provider**.</span></span> <span data-ttu-id="44acf-128">Para criar LUNs virtuais adicionais, repita essa etapa.</span><span class="sxs-lookup"><span data-stu-id="44acf-128">To create additional virtual LUNs, repeat this step.</span></span>

        <span data-ttu-id="44acf-129">O provedor de exemplo do VSS reconhece um LUN somente se o **provedor de HW de exemplo do VSS** faz parte do identificador de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="44acf-129">The VSS sample provider recognizes a LUN only if **VSS Sample HW Provider** is a part of the storage identifier.</span></span> <span data-ttu-id="44acf-130">Para obter mais informações sobre o identificador de armazenamento, consulte a seguinte postagem no blog.</span><span class="sxs-lookup"><span data-stu-id="44acf-130">For more information about the storage identifier, see the following blog post.</span></span>

        [<span data-ttu-id="44acf-131">LUN-ressincronização com o DiskShadow e o armazenamento virtual</span><span class="sxs-lookup"><span data-stu-id="44acf-131">LUN - Resync with Diskshadow and Virtual Storage</span></span>](https://blogs.msdn.microsoft.com/b/himanshu_kale/archive/2009/06/02/lun-resync-with-diskshadow-virtual-storage.aspx)

    2.  <span data-ttu-id="44acf-132">Na janela do prompt de comando, use diskpart.exe para formatar o disco virtual e atribuir uma letra da unidade a ele.</span><span class="sxs-lookup"><span data-stu-id="44acf-132">In the command prompt window, use diskpart.exe to format the virtual disk and assign a drive letter to it.</span></span>

        <span data-ttu-id="44acf-133">Aqui está um script de exemplo a ser executado no prompt de comando do DiskPart.</span><span class="sxs-lookup"><span data-stu-id="44acf-133">Here is a sample script to run at the diskpart command prompt.</span></span>

        ```cmd
        Select disk 
        Create partition primary size=<size>
        Format FS=NTFS quick
        Assign Letter=<letter>
        Exit
        ```

        

6.  <span data-ttu-id="44acf-134">Para executar o provedor de exemplo, na janela do prompt de comando, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="44acf-134">To run the sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    Run vshadow.exe -p -nw <drive>
    ```

    

    <span data-ttu-id="44acf-135">*<drive>* representa a letra da unidade do LUN virtual.</span><span class="sxs-lookup"><span data-stu-id="44acf-135">*<drive>* represents the drive letter of the virtual LUN.</span></span>

7.  <span data-ttu-id="44acf-136">Para desinstalar o provedor de exemplo do VSS, na janela do prompt de comando, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="44acf-136">To uninstall the VSS sample provider, in the command prompt window, type the following command:</span></span>

    ```cmd
    uninstall-sampleprovider.cmd
    ```

    

8.  <span data-ttu-id="44acf-137">Para desinstalar o driver de armazenamento virtual, na janela do prompt de comando, digite o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="44acf-137">To uninstall the virtual storage driver, in the command prompt window, type the following command:</span></span>

    ```cmd
    vstorcontrol.exe uninstall
    ```

    

 

 



