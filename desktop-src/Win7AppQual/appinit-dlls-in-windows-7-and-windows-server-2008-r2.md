---
description: .
ms.assetid: 6d1f9703-6dc9-4fdc-b52f-e6bb60a2fe8d
title: AppInit_DLLs no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31db695805b751e5dcd39293d0170c7fb78a11ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797534"
---
# <a name="appinit_dlls-in-windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="14f56-103">AppInit \_ DLLs no Windows 7 e no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14f56-103">AppInit\_DLLs in Windows 7 and Windows Server 2008 R2</span></span>

## <a name="platform"></a><span data-ttu-id="14f56-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="14f56-104">Platform</span></span>

<span data-ttu-id="14f56-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="14f56-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="14f56-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14f56-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="14f56-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="14f56-107">Feature Impact</span></span>

 <span data-ttu-id="14f56-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="14f56-108">**Severity** - Low</span></span>  
<span data-ttu-id="14f56-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="14f56-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="14f56-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="14f56-110">Description</span></span>

<span data-ttu-id="14f56-111">AppInit \_ DLLs é um mecanismo que permite que uma lista arbitrária de DLLs seja carregada em cada processo de modo de usuário no sistema.</span><span class="sxs-lookup"><span data-stu-id="14f56-111">AppInit\_DLLs is a mechanism that allows an arbitrary list of DLLs to be loaded into each user mode process on the system.</span></span> <span data-ttu-id="14f56-112">A Microsoft está modificando a instalação do AppInit DLLs no Windows 7 e no Windows Server 2008 R2 para adicionar um novo requisito de assinatura de código.</span><span class="sxs-lookup"><span data-stu-id="14f56-112">Microsoft is modifying the AppInit DLLs facility in Windows 7 and Windows Server 2008 R2 to add a new code-signing requirement.</span></span> <span data-ttu-id="14f56-113">Isso ajudará a melhorar a confiabilidade e o desempenho do sistema, além de melhorar a visibilidade da origem do software.</span><span class="sxs-lookup"><span data-stu-id="14f56-113">This will help improve the system reliability and performance, as well as improve visibility into the origin of software.</span></span>

## <a name="configuration"></a><span data-ttu-id="14f56-114">Configuração</span><span class="sxs-lookup"><span data-stu-id="14f56-114">Configuration</span></span>

<span data-ttu-id="14f56-115">Valores armazenados em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Windows Key no registro determinam o comportamento da infraestrutura AppInit \_ DLLs.</span><span class="sxs-lookup"><span data-stu-id="14f56-115">Values stored under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion \\Windows key in the registry determine the behavior of the AppInit\_DLLs infrastructure.</span></span> <span data-ttu-id="14f56-116">A tabela a seguir descreve esses valores de registro:</span><span class="sxs-lookup"><span data-stu-id="14f56-116">The table below describes these registry values:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="14f56-117">Valor</span><span class="sxs-lookup"><span data-stu-id="14f56-117">Value</span></span></th>
<th><span data-ttu-id="14f56-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="14f56-118">Description</span></span></th>
<th><span data-ttu-id="14f56-119">Valores de exemplo</span><span class="sxs-lookup"><span data-stu-id="14f56-119">Sample Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="14f56-120">LoadAppInit_DLLs (REG_DWORD) $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="14f56-120">LoadAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="14f56-121">Habilita ou desabilita globalmente AppInit_DLLs. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="14f56-121">Globally enables or disables AppInit_DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="14f56-122">0x0 – AppInit_DLLs estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="14f56-122">0x0 – AppInit_DLLs are disabled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="14f56-123">0x1 – AppInit_DLLs estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="14f56-123">0x1 – AppInit_DLLs are enabled.</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="14f56-124">AppInit_DLLs (REG_SZ)</span><span class="sxs-lookup"><span data-stu-id="14f56-124">AppInit_DLLs (REG_SZ)</span></span></td>
<td><span data-ttu-id="14f56-125">Espaço ou lista delimitada por vírgulas de DLLs a serem carregadas.</span><span class="sxs-lookup"><span data-stu-id="14f56-125">Space or comma delimited list of DLLs to load.</span></span> <span data-ttu-id="14f56-126">O caminho completo para a DLL deve ser especificado usando nomes curtos.</span><span class="sxs-lookup"><span data-stu-id="14f56-126">The complete path to the DLL should be specified using Short Names.</span></span></td>
<td><span data-ttu-id="14f56-127">C:\ PROGRA ~ 1 \ WID288 ~ 1 \ MICROS ~1.DLL</span><span class="sxs-lookup"><span data-stu-id="14f56-127">C:\ PROGRA~1\WID288~1\MICROS~1.DLL</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="14f56-128">RequireSignedAppInit_DLLs (REG_DWORD) $ {remover} $</span><span class="sxs-lookup"><span data-stu-id="14f56-128">RequireSignedAppInit_DLLs (REG_DWORD)${REMOVE}$</span></span><br />
</td>
<td rowspan="2"><span data-ttu-id="14f56-129">Carregar somente DLLs assinadas por código. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="14f56-129">Only load code-signed DLLs.${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="14f56-130">0x0 – carregar qualquer DLL.</span><span class="sxs-lookup"><span data-stu-id="14f56-130">0x0 – Load any DLLs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="14f56-131">0x1 – carregar somente DLLs assinadas por código.</span><span class="sxs-lookup"><span data-stu-id="14f56-131">0x1 – Load only code-signed DLLs.</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="14f56-132">**Windows 7**</span><span class="sxs-lookup"><span data-stu-id="14f56-132">**Windows 7**</span></span>

<span data-ttu-id="14f56-133">Todas as DLLs que são carregadas pela \_ infraestrutura AppInit DLLs devem ser assinadas por código.</span><span class="sxs-lookup"><span data-stu-id="14f56-133">All DLLs that are loaded by the AppInit\_DLLs infrastructure should be code-signed.</span></span> <span data-ttu-id="14f56-134">Nos interesses da compatibilidade de aplicativos, o sistema operacional Windows 7 carregará todas as DLLs AppInit.</span><span class="sxs-lookup"><span data-stu-id="14f56-134">In the interests of application compatibility, the Windows 7 Operating System will load all AppInit DLLs.</span></span> <span data-ttu-id="14f56-135">No entanto, a Microsoft recomenda que todos os desenvolvedores de aplicativos codifiquem suas DLLs para ajudar a melhorar a confiabilidade do Windows e se preparar para a imposição de assinatura de código em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="14f56-135">However, Microsoft recommends that all application developers code-sign their DLLs to help improve the reliability of Windows and prepare for code-signing enforcement in future versions of Windows.</span></span> <span data-ttu-id="14f56-136">A \_ chave do registro RequireSignedAppInit DLLs controla esse comportamento e seu valor no Windows 7 é definido como 0 por padrão.</span><span class="sxs-lookup"><span data-stu-id="14f56-136">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows 7 is set to 0 by default.</span></span>

<span data-ttu-id="14f56-137">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="14f56-137">**Windows Server 2008 R2**</span></span>

<span data-ttu-id="14f56-138">Todas as DLLs que são carregadas pela \_ infraestrutura de DLLs AppInit devem ser assinadas por código.</span><span class="sxs-lookup"><span data-stu-id="14f56-138">All DLLs that are loaded by the AppInit\_DLLs infrastructure must be code-signed.</span></span> <span data-ttu-id="14f56-139">A \_ chave do registro RequireSignedAppInit DLLs controla esse comportamento e seu valor no Windows Server 2008 R2 é definido como 1 por padrão.</span><span class="sxs-lookup"><span data-stu-id="14f56-139">The RequireSignedAppInit\_DLLs registry key controls this behavior and its value on Windows Server 2008 R2 is set to 1 by default.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="14f56-140">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="14f56-140">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="14f56-141">AppInit DLLs no Windows 7 e no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="14f56-141">AppInit DLLs in Windows 7 and Windows Server 2008 R2</span></span>](/windows-hardware/drivers/install/)  
</dl>

 

 
