---
description: Fazer backup de volumes enquanto os aplicativos em um sistema continuam a gravar nos volumes. Minimize o tempo de inatividade do aplicativo Criando rapidamente um instantâneo (cópia de sombra) de um volume que duplica todos os dados. Execute o backup de multivolume.
ms.assetid: 1eca1e3e-fc86-44b5-b3c4-bcee41bc5a43
title: Serviço de Cópias de Sombra de Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438ef32f1cbbc5fc82878486d9ad35b549f4535a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763762"
---
# <a name="volume-shadow-copy-service"></a><span data-ttu-id="b8c69-105">Serviço de Cópias de Sombra de Volume</span><span class="sxs-lookup"><span data-stu-id="b8c69-105">Volume Shadow Copy Service</span></span>

## <a name="purpose"></a><span data-ttu-id="b8c69-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="b8c69-106">Purpose</span></span>

<span data-ttu-id="b8c69-107">O Serviço de Cópias de Sombra de Volume (VSS) é um conjunto de interfaces COM que implementa uma estrutura para permitir que os backups de volume sejam executados enquanto os aplicativos em um sistema continuam a gravar nos volumes.</span><span class="sxs-lookup"><span data-stu-id="b8c69-107">The Volume Shadow Copy Service (VSS) is a set of COM interfaces that implements a framework to allow volume backups to be performed while applications on a system continue to write to the volumes.</span></span>

<span data-ttu-id="b8c69-108">Para obter uma introdução ao VSS para administradores do sistema, consulte [serviço de cópias de sombra de volume](/windows-server/storage/file-server/volume-shadow-copy-service) na biblioteca do TechNet.</span><span class="sxs-lookup"><span data-stu-id="b8c69-108">For an introduction to VSS for system administrators, see [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service) in the TechNet Library.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b8c69-109">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="b8c69-109">Run-time requirements</span></span>

<span data-ttu-id="b8c69-110">O VSS tem suporte no Microsoft Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="b8c69-110">VSS is supported on Microsoft Windows XP and later.</span></span> <span data-ttu-id="b8c69-111">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da documentação para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="b8c69-111">For information about run-time requirements for a particular programming element, see the Requirements section of the documentation for that element.</span></span>

<span data-ttu-id="b8c69-112">Todos os aplicativos VSS de 32 bits (solicitantes, provedores e gravadores) devem ser executados como aplicativos nativos de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b8c69-112">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="b8c69-113">Não há suporte para executá-los em WOW64.</span><span class="sxs-lookup"><span data-stu-id="b8c69-113">Running them under WOW64 is not supported.</span></span> <span data-ttu-id="b8c69-114">Para obter mais informações, consulte [supported Configurations and Restrictions](usage-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="b8c69-114">For more information, see [Supported Configurations and Restrictions](usage-conventions.md).</span></span>

<span data-ttu-id="b8c69-115">**Windows Server 2003 e Windows XP:** A execução de solicitantes do VSS de 32 bits no WOW64 tem suporte, mas não para backups de estado do sistema.</span><span class="sxs-lookup"><span data-stu-id="b8c69-115">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="b8c69-116">Não há suporte para a execução de provedores VSS de 32 bits e gravadores no WOW64.</span><span class="sxs-lookup"><span data-stu-id="b8c69-116">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="b8c69-117">O suporte para a execução de solicitantes de 32 bits no WOW64 foi removido no Windows Vista e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="b8c69-117">Support for running 32-bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

> [!Note]  
> <span data-ttu-id="b8c69-118">Uma cópia de sombra criada no Windows Server 2003 R2 ou no Windows Server 2003 não pode ser usada em um computador que esteja executando o Windows Server 2008 R2 ou o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b8c69-118">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="b8c69-119">Uma cópia de sombra criada no Windows Server 2008 R2 ou no Windows Server 2008 não pode ser usada em um computador que esteja executando o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8c69-119">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="b8c69-120">No entanto, uma cópia de sombra criada no Windows Server 2008 pode ser usada em um computador que esteja executando o Windows Server 2008 R2 e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="b8c69-120">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="b8c69-121">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b8c69-121">In this section</span></span>



| <span data-ttu-id="b8c69-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="b8c69-122">Topic</span></span>                                                          | <span data-ttu-id="b8c69-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8c69-123">Description</span></span>                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8c69-124">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b8c69-124">Overview</span></span>](volume-shadow-copy-service-overview.md)<br/> | <span data-ttu-id="b8c69-125">Descreve o modelo de objeto do VSS, estratégias de backup e restauração e como criar provedores, solicitantes e gravadores do VSS.</span><span class="sxs-lookup"><span data-stu-id="b8c69-125">Describes the VSS object model, backup and restore strategies, and how to create VSS providers, requesters, and writers.</span></span><br/> |
| [<span data-ttu-id="b8c69-126">Referência</span><span class="sxs-lookup"><span data-stu-id="b8c69-126">Reference</span></span>](volume-shadow-copy-reference.md)<br/>       | <span data-ttu-id="b8c69-127">Descreve classes VSS, tipos de dados, enumerações, funções, interfaces e estruturas.</span><span class="sxs-lookup"><span data-stu-id="b8c69-127">Describes VSS classes, data types, enumerations, functions, interfaces, and structures.</span></span><br/>                                  |



 

## <a name="additional-resources"></a><span data-ttu-id="b8c69-128">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="b8c69-128">Additional resources</span></span>



|                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c69-129">Windows Vista e posterior</span><span class="sxs-lookup"><span data-stu-id="b8c69-129">Windows Vista and later</span></span>            | <span data-ttu-id="b8c69-130">O VSS está disponível no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b8c69-130">VSS is available in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b8c69-131">Você pode instalar o SDK para Windows 7 e Windows Server 2008 R2 no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="b8c69-131">You can install the SDK for Windows 7 and Windows Server 2008 R2 from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).</span></span> <span data-ttu-id="b8c69-132">Você também pode baixar a [versão ISO](https://www.microsoft.com/download/details.aspx?id=8442) do SDK no centro de download do Windows.</span><span class="sxs-lookup"><span data-stu-id="b8c69-132">You can also download the [ISO version](https://www.microsoft.com/download/details.aspx?id=8442) of the SDK from the Windows Download Center.</span></span> <span data-ttu-id="b8c69-133">As versões anteriores do SDK podem ser baixadas na [página de Download SDK do Windows](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8c69-133">Previous versions of the SDK can be downloaded from the [Windows SDK Download Page](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span> |
| <span data-ttu-id="b8c69-134">Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="b8c69-134">Windows Server 2003 and Windows XP</span></span> | <span data-ttu-id="b8c69-135">O VSS está disponível no SDK do Serviço de Cópias de Sombra de Volume 7,2, que pode ser baixado no [centro de download do Windows](https://www.microsoft.com/download/details.aspx?id=23490).</span><span class="sxs-lookup"><span data-stu-id="b8c69-135">VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="b8c69-136">Observe que os arquivos vssapi. lib de 64 bits nos diretórios no diretório do Win2003 \\ obj podem ser usados para as versões de 64 bits do Windows Server 2003 e do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b8c69-136">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 and Windows XP.</span></span>                                                                                                                                                                 |



 

 

 
