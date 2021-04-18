---
description: O instalador definirá a propriedade RedirectedDLLSupport se a plataforma do sistema que executa a instalação do oferecer suporte a componentes isolados.
ms.assetid: 703489c4-cac4-442c-bd96-d3927491a864
title: Propriedade RedirectedDLLSupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bed308eaf022ada5c6c8697ba47f55605f1fecbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780946"
---
# <a name="redirecteddllsupport-property"></a><span data-ttu-id="20a42-103">Propriedade RedirectedDLLSupport</span><span class="sxs-lookup"><span data-stu-id="20a42-103">RedirectedDLLSupport property</span></span>

<span data-ttu-id="20a42-104">O instalador definirá a propriedade **RedirectedDLLSupport** se a plataforma do sistema que executa a instalação do oferecer suporte a [componentes isolados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="20a42-104">The installer sets the **RedirectedDLLSupport** property if the system platform performing the installation supports [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="20a42-105">O instalador definirá a propriedade **RedirectedDLLSupport** com um valor de 1 se o sistema que estiver executando a instalação oferecer suporte a [componentes isolados](isolated-components.md) baseados em. Arquivos locais.</span><span class="sxs-lookup"><span data-stu-id="20a42-105">The installer sets the **RedirectedDLLSupport** property to a value of 1 if the system performing the installation supports [Isolated Components](isolated-components.md) based on .LOCAL files.</span></span> <span data-ttu-id="20a42-106">O instalador definirá a propriedade **RedirectedDLLSupport** com um valor de 2 se o sistema que executa a instalação do oferecer suporte ao isolamento usando qualquer um dos dois. Arquivos locais ou assemblies lado a lado do Win32.</span><span class="sxs-lookup"><span data-stu-id="20a42-106">The installer sets the **RedirectedDLLSupport** property to a value of 2 if the system that performs the installation supports isolation using either .LOCAL files or Win32 side-by-side assemblies.</span></span>

<span data-ttu-id="20a42-107">A propriedade **RedirectedDLLSupport** pode ser usada para condição da [ação IsolateComponents](isolatecomponents-action.md) na [tabela InstallUISequence](installuisequence-table.md) ou na [tabela InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="20a42-107">The **RedirectedDLLSupport** property can be used to condition the [IsolateComponents action](isolatecomponents-action.md) in the [InstallUISequence table](installuisequence-table.md) or [InstallExecuteSequence table](installexecutesequence-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20a42-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20a42-108">Requirements</span></span>



| <span data-ttu-id="20a42-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="20a42-109">Requirement</span></span> | <span data-ttu-id="20a42-110">Valor</span><span class="sxs-lookup"><span data-stu-id="20a42-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20a42-111">Versão</span><span class="sxs-lookup"><span data-stu-id="20a42-111">Version</span></span><br/> | <span data-ttu-id="20a42-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20a42-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="20a42-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="20a42-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="20a42-114">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="20a42-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="20a42-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="20a42-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20a42-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="20a42-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a42-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="20a42-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




