---
description: A propriedade FASTOEM foi projetada para permitir que os OEMs reduzam o tempo necessário para instalar Windows Installer aplicativos para um cenário específico.
ms.assetid: 4c0af524-eb2e-4d64-bb25-3dae488d236d
title: Propriedade FASTOEM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78993a4affed62baf7e15a2b7787d83cabb9429e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754359"
---
# <a name="fastoem-property"></a><span data-ttu-id="f0581-103">Propriedade FASTOEM</span><span class="sxs-lookup"><span data-stu-id="f0581-103">FASTOEM property</span></span>

<span data-ttu-id="f0581-104">A propriedade **FASTOEM** foi projetada para permitir que os OEMs reduzam o tempo necessário para instalar Windows Installer aplicativos para um cenário específico.</span><span class="sxs-lookup"><span data-stu-id="f0581-104">The **FASTOEM** property is designed to enable OEMs to reduce the time it takes to install Windows Installer applications for a specific scenario.</span></span> <span data-ttu-id="f0581-105">Não crie a propriedade **FASTOEM** na tabela de [Propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0581-105">Do not author the **FASTOEM** property into the [Property Table](property-table.md).</span></span>

<span data-ttu-id="f0581-106">A propriedade **FASTOEM** só será aplicável se todas essas condições forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="f0581-106">The **FASTOEM** property is only applicable if all of these conditions are true:</span></span>

-   <span data-ttu-id="f0581-107">O aplicativo está sendo instalado no mesmo volume que a pasta que contém os arquivos de origem.</span><span class="sxs-lookup"><span data-stu-id="f0581-107">The application is being installed on the same volume as the folder containing the source files.</span></span>
-   <span data-ttu-id="f0581-108">Os arquivos de origem são excluídos após a instalação.</span><span class="sxs-lookup"><span data-stu-id="f0581-108">The source files are deleted after the installation.</span></span>
-   <span data-ttu-id="f0581-109">Nenhuma interface do usuário é exibida durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="f0581-109">No user interface is displayed during the installation.</span></span> <span data-ttu-id="f0581-110">O [nível da interface do usuário](user-interface-levels.md) é nenhum.</span><span class="sxs-lookup"><span data-stu-id="f0581-110">The [user interface level](user-interface-levels.md) is none.</span></span>
-   <span data-ttu-id="f0581-111">A instalação é executada no [contexto de instalação](installation-context.md)por máquina.</span><span class="sxs-lookup"><span data-stu-id="f0581-111">The installation is performed in the per-machine [installation context](installation-context.md).</span></span>
-   <span data-ttu-id="f0581-112">Há espaço suficiente no computador para uma instalação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f0581-112">There is enough space on the computer for a successful installation.</span></span>
-   <span data-ttu-id="f0581-113">Essa é a primeira vez que a instalação.</span><span class="sxs-lookup"><span data-stu-id="f0581-113">This is first time installation.</span></span> <span data-ttu-id="f0581-114">A instalação não está anunciando, reinstalando, removendo ou fazendo uma instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="f0581-114">The installation is not advertising, reinstalling, removing, or doing an administrative installation.</span></span>
-   <span data-ttu-id="f0581-115">Nenhum recurso está instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="f0581-115">No features are installed to run from source.</span></span>
-   <span data-ttu-id="f0581-116">O pacote de instalação não contém [componentes isolados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="f0581-116">The installation package contains no [isolated components](isolated-components.md).</span></span> <span data-ttu-id="f0581-117">Como os componentes isolados exigem que os arquivos de origem permaneçam localizados na origem, a propriedade **FASTOEM** não pode ser usada atualmente com componentes isolados.</span><span class="sxs-lookup"><span data-stu-id="f0581-117">Because isolated components require source files to remain located at the source, the **FASTOEM** property cannot currently be used with isolated components.</span></span>

<span data-ttu-id="f0581-118">Se todas as condições anteriores forem verdadeiras, a configuração da propriedade **FASTOEM** permitirá que Windows Installer melhore o desempenho fazendo o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f0581-118">If all of the previous conditions are true, setting the **FASTOEM** property enables Windows Installer to improve performance by doing the following:</span></span>

-   <span data-ttu-id="f0581-119">Mover em vez de copiar arquivos no mesmo volume.</span><span class="sxs-lookup"><span data-stu-id="f0581-119">Move rather than copy files on the same volume.</span></span> <span data-ttu-id="f0581-120">Isso não garante que todos os arquivos sejam movidos em vez de copiados.</span><span class="sxs-lookup"><span data-stu-id="f0581-120">This does not guarantee that all files are moved rather than copied.</span></span> <span data-ttu-id="f0581-121">Observe que, se o computador tiver vários discos rígidos, você deverá inicializar a propriedade [**ROOTDRIVE**](rootdrive.md) na linha de comando para a mesma unidade que contém a origem da instalação.</span><span class="sxs-lookup"><span data-stu-id="f0581-121">Note that if the computer has multiple hard drives, you must initialize the [**ROOTDRIVE**](rootdrive.md) property on the command line to the same drive containing the installation source.</span></span>
-   <span data-ttu-id="f0581-122">Omita essa fonte da lista de origem do aplicativo para que as instalações de reinstalação ou manutenção subsequentes sejam padronizadas para as fontes de CD-ROM especificadas na [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0581-122">Omit this source from the application's source list so that subsequent reinstallation or maintenance installations default to the CD-ROM sources specified in the [Media Table](media-table.md).</span></span>
-   <span data-ttu-id="f0581-123">Simplifique o [custo do arquivo](file-costing.md).</span><span class="sxs-lookup"><span data-stu-id="f0581-123">Streamline [file costing](file-costing.md).</span></span>
-   <span data-ttu-id="f0581-124">Suprimir mensagens de progresso enviadas do Windows Installer ao cliente.</span><span class="sxs-lookup"><span data-stu-id="f0581-124">Suppress progress messages sent from Windows Installer to the client.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0581-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0581-125">Remarks</span></span>

<span data-ttu-id="f0581-126">Como nenhuma mensagem de progresso é enviada quando **FASTOEM** é definido, é recomendável que os autores gravem manualmente um valor de 1800 para tempo limite na chave</span><span class="sxs-lookup"><span data-stu-id="f0581-126">Because no progress messages are sent when **FASTOEM** is set, it is recommended that authors manually write a value of 1800 for Timeout into the key</span></span>

<span data-ttu-id="f0581-127">**HKLM** \\ **Software** \\ **Políticas** \\ do **Microsoft** \\ **Windows** \\ **Instalador** \\ do **Tempo limite**</span><span class="sxs-lookup"><span data-stu-id="f0581-127">**HKLM**\\**SoftWare**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**Timeout**</span></span>

<span data-ttu-id="f0581-128">Timeout é um tipo **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f0581-128">Timeout is a **REG\_DWORD** type.</span></span>

<span data-ttu-id="f0581-129">Para exibir o tamanho do aplicativo em Adicionar ou remover programas no painel de controle do Windows 2000, você deve gravar manualmente o valor de EstimatedSize na chave</span><span class="sxs-lookup"><span data-stu-id="f0581-129">To display the size of the application in Add or Remove Programs in the Windows 2000 Control Panel, you must manually write the value of EstimatedSize into the key</span></span>

<span data-ttu-id="f0581-130">**HKLM** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Desinstalar** \\ o **<  Código > do produto**</span><span class="sxs-lookup"><span data-stu-id="f0581-130">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Uninstall**\\**<*Product Code*>**</span></span>

<span data-ttu-id="f0581-131">Esse é um tipo **reg \_ DWORD** e é igual ao tamanho do aplicativo em Kbytes.</span><span class="sxs-lookup"><span data-stu-id="f0581-131">This is a **REG\_DWORD** type and equals to the size of the application in Kbytes.</span></span> <span data-ttu-id="f0581-132">O instalador não grava esse valor automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f0581-132">The installer does not automatically write this value.</span></span>

<span data-ttu-id="f0581-133">Use a seguinte linha de comando de exemplo se o CD-ROM enviado para os usuários finais armazenar o pacote de instalação do aplicativo na raiz do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f0581-133">Use the following example command line if the CD-ROM shipped to end users stores the application's installation package at the root of the CD-ROM.</span></span> <span data-ttu-id="f0581-134">Observe que o rótulo de volume na [tabela de mídia](media-table.md) do arquivo. msi deve corresponder ao rótulo de volume do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f0581-134">Note that the volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span>

<span data-ttu-id="f0581-135">**Msiexec/I C: \\ TempImage \\package.msi/qn/Le logfile.txt AllUsers = 1 FASTOEM = 1 DISABLEROLLBACK = 1 ROOTDRIVE = C:\\**</span><span class="sxs-lookup"><span data-stu-id="f0581-135">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 ROOTDRIVE=C:\\**</span></span>

<span data-ttu-id="f0581-136">Use a seguinte linha de comando de exemplo se o pacote de instalação não estiver localizado na raiz do CD-ROM enviado aos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="f0581-136">Use the following example command line if the installation package is not located at the root of the CD-ROM shipped to end users.</span></span> <span data-ttu-id="f0581-137">Você deve definir a propriedade [**MEDIAPACKAGEPATH**](mediapackagepath.md) nesse caso como o caminho para o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="f0581-137">You must set the [**MEDIAPACKAGEPATH**](mediapackagepath.md) property in this case to the path to the installation package.</span></span> <span data-ttu-id="f0581-138">O rótulo de volume na [tabela de mídia](media-table.md) do arquivo. msi deve corresponder ao rótulo de volume do CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="f0581-138">The volume label in the [Media Table](media-table.md) of the .msi file must match the volume label of the CD-ROM.</span></span> <span data-ttu-id="f0581-139">Nesse caso, siga este exemplo.</span><span class="sxs-lookup"><span data-stu-id="f0581-139">In this case follow this example.</span></span>

<span data-ttu-id="f0581-140">**Msiexec/I C: \\ TempImage \\package.msi/qn/Le logfile.txt AllUsers = 1 FASTOEM = 1 DISABLEROLLBACK = 1 MEDIAPACKAGEPATH = c: \\ TempImage \\package.msi ROOTDRIVE = c:\\**</span><span class="sxs-lookup"><span data-stu-id="f0581-140">**Msiexec /I C:\\TempImage\\package.msi /qn /le logfile.txt ALLUSERS=1 FASTOEM=1 DISABLEROLLBACK=1 MEDIAPACKAGEPATH=C:\\TempImage\\package.msi ROOTDRIVE=C:\\**</span></span>

## <a name="requirements"></a><span data-ttu-id="f0581-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0581-141">Requirements</span></span>



| <span data-ttu-id="f0581-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0581-142">Requirement</span></span> | <span data-ttu-id="f0581-143">Valor</span><span class="sxs-lookup"><span data-stu-id="f0581-143">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0581-144">Versão</span><span class="sxs-lookup"><span data-stu-id="f0581-144">Version</span></span><br/> | <span data-ttu-id="f0581-145">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f0581-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f0581-146">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f0581-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f0581-147">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f0581-147">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f0581-148">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f0581-148">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f0581-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0581-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0581-150">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f0581-150">Properties</span></span>](properties.md)
</dt> </dl>

 

 




