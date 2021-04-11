---
description: Uma CRC (verificação de redundância cíclica) de arquivos está disponível com Windows Installer.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: Verificação de CRC durante uma instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170666"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="6b5fd-103">Verificação de CRC durante uma instalação</span><span class="sxs-lookup"><span data-stu-id="6b5fd-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="6b5fd-104">Uma CRC (verificação de redundância cíclica) de arquivos está disponível com Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="6b5fd-105">A verificação de CRC é um mecanismo de verificação de erros semelhante a uma checksum, que permite que um aplicativo determine se as informações em um arquivo foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="6b5fd-106">Depois que o Windows Installer terminar de copiar um arquivo, ele obtém um valor de CRC dos arquivos de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="6b5fd-107">O instalador verifica a CRC original carimbada no arquivo e a compara com a CRC calculada a partir da cópia.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="6b5fd-108">A verificação de CRC falhará se o valor de CRC original for não nulo e for diferente do CRC calculado na cópia.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="6b5fd-109">Se o CRC original for nulo, nenhuma verificação ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="6b5fd-110">O Windows Installer faz uma verificação de CRC em um arquivo nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="6b5fd-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="6b5fd-111">Se a [Propriedade MSICHECKCRCS](msicheckcrcs.md) for definida e **msidbFileAttributesChecksum** estiver incluído no campo atributos do registro do arquivo na [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="6b5fd-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="6b5fd-112">O instalador faz a verificação de CRC uma vez após a instalação, duplicação ou movimentação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="6b5fd-113">Se a [Propriedade MSICHECKCRCS](msicheckcrcs.md) for definida e **msidbFileAttributesChecksum** estiver incluído no campo atributos do registro do arquivo na [tabela de arquivos](file-table.md), o instalador fará uma verificação de CRC depois de aplicar o patch no arquivo.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="6b5fd-114">Se o **msidbFileAttributesChecksum** for incluído no campo atributos do registro do arquivo na [tabela de arquivos](file-table.md), o instalador fará uma verificação de CRC antes de vincular as imagens.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="6b5fd-115">Se a verificação falhar antes de associar uma imagem, o instalador relatará os dois erros a seguir no arquivo de log e continuará a instalação sem associar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="6b5fd-116">Código</span><span class="sxs-lookup"><span data-stu-id="6b5fd-116">Code</span></span> | <span data-ttu-id="6b5fd-117">Mensagem</span><span class="sxs-lookup"><span data-stu-id="6b5fd-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="6b5fd-118">2941</span><span class="sxs-lookup"><span data-stu-id="6b5fd-118">2941</span></span> | <span data-ttu-id="6b5fd-119">Não é possível computar o CRC para o arquivo \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="6b5fd-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="6b5fd-120">2942</span><span class="sxs-lookup"><span data-stu-id="6b5fd-120">2942</span></span> | <span data-ttu-id="6b5fd-121">A ação de BindImage não foi executada em \[ 2 \] arquivos.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="6b5fd-122">Se a verificação falhar depois que um arquivo descompactado tiver sido copiado, duplicado ou corrigido, o instalador relatará o erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="6b5fd-123">Esse erro também será relatado se a verificação falhar depois que um arquivo compactado for copiado.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="6b5fd-124">Se o arquivo tiver o atributo **msidbFileAttributesVital** , o arquivo será considerado vital para a instalação e o usuário obterá a opção de tentar novamente ou cancelar a instalação.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="6b5fd-125">Se o arquivo for marcado como não vital na coluna atributos da tabela de [arquivos](file-table.md), o usuário poderá ignorar o erro e continuar, repetir ou cancelar a instalação.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="6b5fd-126">Código</span><span class="sxs-lookup"><span data-stu-id="6b5fd-126">Code</span></span> | <span data-ttu-id="6b5fd-127">Mensagem</span><span class="sxs-lookup"><span data-stu-id="6b5fd-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="6b5fd-128">1331</span><span class="sxs-lookup"><span data-stu-id="6b5fd-128">1331</span></span> | <span data-ttu-id="6b5fd-129">Falha ao copiar corretamente \[ o \] arquivo 2: erro de CRC.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="6b5fd-130">Observe que somente arquivos descompactados são movidos.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="6b5fd-131">Se a verificação falhar depois que um arquivo descompactado for movido, o instalador exibirá o erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="6b5fd-132">Se o arquivo tiver o atributo **msidbFileAttributesVital** , o arquivo será considerado vital para a instalação e a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="6b5fd-133">Se o arquivo for marcado como não vital na coluna atributos da tabela de [arquivos](file-table.md), o usuário obterá a opção de cancelar ou ignorar o erro e continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="6b5fd-134">Código</span><span class="sxs-lookup"><span data-stu-id="6b5fd-134">Code</span></span> | <span data-ttu-id="6b5fd-135">Mensagem</span><span class="sxs-lookup"><span data-stu-id="6b5fd-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="6b5fd-136">1332</span><span class="sxs-lookup"><span data-stu-id="6b5fd-136">1332</span></span> | <span data-ttu-id="6b5fd-137">Falha ao mover corretamente \[ 2 \] arquivos: erro de CRC.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="6b5fd-138">Se a verificação falhar depois que um arquivo descompactado for corrigido, o instalador exibirá o erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="6b5fd-139">Se o arquivo tiver o atributo **msidbFileAttributesVital** , o arquivo será considerado vital para a instalação e a instalação falhará.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="6b5fd-140">Se o arquivo for marcado como não vital na coluna atributos da tabela de [arquivos](file-table.md), o usuário obterá a opção de cancelar ou ignorar o erro e continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="6b5fd-141">Código</span><span class="sxs-lookup"><span data-stu-id="6b5fd-141">Code</span></span> | <span data-ttu-id="6b5fd-142">Mensagem</span><span class="sxs-lookup"><span data-stu-id="6b5fd-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="6b5fd-143">1333</span><span class="sxs-lookup"><span data-stu-id="6b5fd-143">1333</span></span> | <span data-ttu-id="6b5fd-144">Falha ao corrigir corretamente \[ o \] arquivo 2: erro de CRC.</span><span class="sxs-lookup"><span data-stu-id="6b5fd-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



