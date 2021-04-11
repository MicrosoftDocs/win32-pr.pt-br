---
description: Ao desenvolver seu próprio aplicativo VSS, você deve observar as diretrizes e restrições a seguir.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilidade do aplicativo VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296365"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="d6a4e-103">Compatibilidade do aplicativo VSS</span><span class="sxs-lookup"><span data-stu-id="d6a4e-103">VSS Application Compatibility</span></span>

<span data-ttu-id="d6a4e-104">Ao desenvolver seu próprio aplicativo VSS, você deve observar as diretrizes e restrições a seguir.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="d6a4e-105">Talvez você ache útil consultar o código de exemplo para solicitantes, provedores e gravadores do VSS fornecidos no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="d6a4e-106">O SDK do Windows pode ser usado para desenvolver aplicativos VSS somente para versões posteriores do sistema operacional Windows Vista e do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="d6a4e-107">Ele não pode ser usado para desenvolver solicitantes, provedores ou gravadores VSS para o Windows Server 2003 R2, o Windows Server 2003 ou o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="d6a4e-108">**Windows server 2003 R2, Windows server 2003 e Windows XP:** O VSS está disponível no SDK do Serviço de Cópias de Sombra de Volume 7,2, do qual você pode baixar [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) .</span><span class="sxs-lookup"><span data-stu-id="d6a4e-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="d6a4e-109">Observe que os arquivos vssapi. lib de 64 bits nos diretórios no diretório do Win2003 \\ obj podem ser usados para as versões de 64 bits do Windows server 2003 R2, Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="d6a4e-110">Esse SDK também fornece código de exemplo para solicitantes, provedores e gravadores do VSS.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="d6a4e-111">Compilando aplicativos VSS</span><span class="sxs-lookup"><span data-stu-id="d6a4e-111">Compiling VSS Applications</span></span>

<span data-ttu-id="d6a4e-112">Ao desenvolver um solicitante, como um aplicativo de backup:</span><span class="sxs-lookup"><span data-stu-id="d6a4e-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="d6a4e-113">Inclua os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="d6a4e-113">Include the following headers:</span></span> <dl> <span data-ttu-id="d6a4e-114">VSS. h</span><span class="sxs-lookup"><span data-stu-id="d6a4e-114">Vss.h</span></span>  
    <span data-ttu-id="d6a4e-115">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="d6a4e-115">VsWriter.h</span></span>  
    <span data-ttu-id="d6a4e-116">VsBackup. h</span><span class="sxs-lookup"><span data-stu-id="d6a4e-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="d6a4e-117">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="d6a4e-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="d6a4e-118">Ao desenvolver um gravador:</span><span class="sxs-lookup"><span data-stu-id="d6a4e-118">When developing a writer:</span></span>

-   <span data-ttu-id="d6a4e-119">Inclua os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="d6a4e-119">Include the following headers:</span></span> <dl> <span data-ttu-id="d6a4e-120">VSS. h</span><span class="sxs-lookup"><span data-stu-id="d6a4e-120">Vss.h</span></span>  
    <span data-ttu-id="d6a4e-121">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="d6a4e-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="d6a4e-122">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="d6a4e-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="d6a4e-123">Configurações e restrições com suporte</span><span class="sxs-lookup"><span data-stu-id="d6a4e-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="d6a4e-124">A lista a seguir descreve as configurações e restrições com suporte:</span><span class="sxs-lookup"><span data-stu-id="d6a4e-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="d6a4e-125">O VSS é fornecido e tem suporte em versões do sistema operacional Windows a partir do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="d6a4e-126">A tabela a seguir resume as informações de compatibilidade em todas as versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="d6a4e-127">Observe que, se um aplicativo VSS for "compilado para" uma versão especificada do Windows, isso significará que o aplicativo foi compilado usando os arquivos de cabeçalho e as bibliotecas específicas dessa versão.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="d6a4e-128">Os provedores de hardware serão executados somente em versões do sistema operacional Windows Server.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="d6a4e-129">Eles não serão executados em versões do sistema operacional cliente Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="d6a4e-130">Nas tabelas a seguir, o Windows Server 2008 com Service Pack 2 (SP2) deve ser considerado o mesmo que o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="d6a4e-131">Para obter mais informações sobre o Windows Server 2008 com SP2, consulte <https://go.microsoft.com/fwlink/p/?linkid=178730> .</span><span class="sxs-lookup"><span data-stu-id="d6a4e-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="d6a4e-132">O Windows Server 2003 R2 deve ser considerado o mesmo que o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="d6a4e-133">Se um aplicativo VSS for compilado para o Windows Server 2003 ou posterior, ele também será executado em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d6a4e-134">Solicitantes, gravadores e provedores do VSS compilados para</span><span class="sxs-lookup"><span data-stu-id="d6a4e-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="d6a4e-135">Será executado em</span><span class="sxs-lookup"><span data-stu-id="d6a4e-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="d6a4e-136">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) e Windows Vista (64 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="d6a4e-137">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits) e Windows Vista (64 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d6a4e-138">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) e Windows Vista (32 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="d6a4e-139">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits) e Windows Vista (32 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d6a4e-140">Windows Server 2003 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="d6a4e-141">Windows Server 2008 R2 (64 bits), Windows 7 (64 bits), Windows Server 2008 (64 bits), Windows Vista (64 bits) e Windows Server 2003 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d6a4e-142">Windows Server 2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="d6a4e-143">Windows Server 2008 R2 (32 bits), Windows 7 (32 bits), Windows Server 2008 (32 bits), Windows Vista (32 bits) e Windows Server 2003 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="d6a4e-144">Os solicitantes também serão executados no Windows Server 2003 (64 bits).</span><span class="sxs-lookup"><span data-stu-id="d6a4e-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="d6a4e-145">Edição de 64 bits do Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6a4e-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="d6a4e-146">Windows Server 2003 (64 bits) e Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="d6a4e-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="d6a4e-147">Windows XP (32 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="d6a4e-148">Windows XP (32 bits)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="d6a4e-149">Para compilar um solicitante, gravador ou provedor do VSS para</span><span class="sxs-lookup"><span data-stu-id="d6a4e-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="d6a4e-150">Uso</span><span class="sxs-lookup"><span data-stu-id="d6a4e-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d6a4e-151">Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="d6a4e-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="d6a4e-152">SDK do Windows para Windows 7 (disponível no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=8279)).</span><span class="sxs-lookup"><span data-stu-id="d6a4e-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="d6a4e-153">Windows Server 2008 ou Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6a4e-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="d6a4e-154">SDK do Windows para o Windows Server 2008 (disponível no [SDK do Windows Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span><span class="sxs-lookup"><span data-stu-id="d6a4e-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="d6a4e-155">Windows Server 2003 R2, Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="d6a4e-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="d6a4e-156">SDK do Serviço de Cópias de Sombra de Volume 7,2</span><span class="sxs-lookup"><span data-stu-id="d6a4e-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="d6a4e-157">Todos os aplicativos VSS de 32 bits (solicitantes, provedores e gravadores) devem ser executados como aplicativos nativos de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="d6a4e-158">Não há suporte para executá-los em WOW64.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="d6a4e-159">**Windows Server 2003 e Windows XP:** A execução de solicitantes do VSS de 32 bits no WOW64 tem suporte, mas não para backups de estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="d6a4e-160">Não há suporte para a execução de provedores VSS de 32 bits e gravadores no WOW64.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="d6a4e-161">O suporte para a execução de solicitantes de 32 bits no WOW64 foi removido no Windows Vista e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="d6a4e-162">Uma cópia de sombra criada no Windows Server 2003 R2 ou no Windows Server 2003 não pode ser usada em um computador que esteja executando o Windows Server 2008 R2 ou o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="d6a4e-163">Uma cópia de sombra criada no Windows Server 2008 R2 ou no Windows Server 2008 não pode ser usada em um computador que esteja executando o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="d6a4e-164">No entanto, uma cópia de sombra criada no Windows Server 2008 pode ser usada em um computador que esteja executando o Windows Server 2008 R2 e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="d6a4e-165">Para dar suporte a cópias de sombra, um sistema executando o VSS deve ter pelo menos um sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="d6a4e-166">Esse sistema de arquivos hospedará a "área de comparação" da cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="d6a4e-167">Para obter mais informações, consulte [provedor do sistema](providers.md).</span><span class="sxs-lookup"><span data-stu-id="d6a4e-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="d6a4e-168">Dada a presença de um sistema de arquivos NTFS e, considerando a opção apropriada de contexto (consulte [configurações de contexto de cópia de sombra](shadow-copy-context-configurations.md)), qualquer sistema de arquivos local com suporte pode ser copiado em sombra.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="d6a4e-169">Você pode fazer cópias de sombra somente para sistemas de arquivos montados localmente.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="d6a4e-170">Compartilhamentos remotos e outros sistemas de arquivos com montagem cruzada não podem ser copiados em sombra pelo sistema que os monta.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="d6a4e-171">Esses sistemas de arquivos podem ser copiados em sombra somente pelos sistemas que servem os sistemas de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="d6a4e-172">Gravadores e solicitantes devem especificar apenas recursos locais.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="d6a4e-173">Os recursos locais são conjuntos de arquivos cujo caminho absoluto começa com uma letra da unidade e a letra da unidade não pode ser associada a uma pasta montada em um compartilhamento remoto.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="d6a4e-174">O número máximo de cópias de sombra de software para cada volume é 512.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="d6a4e-175">No entanto, por padrão, você só pode manter 64 cópias de sombra usadas pelo recurso Cópias de Sombra de Pastas Compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="d6a4e-176">Para alterar o limite para as cópias de sombra do recurso de pastas compartilhadas, use a chave do registro [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="d6a4e-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="d6a4e-177">A infraestrutura de componentes de backup não dá suporte ao backup de recursos de cluster como componentes do gravador.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="d6a4e-178">Para fazer backup de recursos de cluster, os aplicativos devem assumir que o caminho é local para um nó de cluster específico especificado.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="d6a4e-179">A Microsoft não fornece suporte técnico de desenvolvedor ou profissional de ti para implementar restaurações de estado do sistema online no Windows (todas as versões).</span><span class="sxs-lookup"><span data-stu-id="d6a4e-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="d6a4e-180">Durante o backup e a recuperação do estado do sistema, a estratégia recomendada é fazer backup e recuperar os volumes do sistema e de inicialização, além dos arquivos enumerados pelos gravadores do estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="d6a4e-181">Os gravadores de estado do sistema são gravadores que têm o atributo de [**\_ \_ tipo de uso do VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) definido como VSS \_ UT \_ BOOTABLESYSTEMSTATE ou VSS \_ UT \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="d6a4e-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
