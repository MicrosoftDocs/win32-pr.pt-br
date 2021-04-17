---
description: A propriedade CostingComplete indica se o instalador concluiu o custo de espaço em disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propriedade CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752858"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="4296b-103">Propriedade CostingComplete</span><span class="sxs-lookup"><span data-stu-id="4296b-103">CostingComplete property</span></span>

<span data-ttu-id="4296b-104">A propriedade **CostingComplete** indica se o instalador concluiu o custo de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="4296b-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="4296b-105">Essa propriedade pode ser usada para criar uma caixa de diálogo disparada se o custo não tiver sido concluído.</span><span class="sxs-lookup"><span data-stu-id="4296b-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="4296b-106">A propriedade é definida dinamicamente durante o custo do espaço em disco e é definida como 1 assim que o custo é concluído.</span><span class="sxs-lookup"><span data-stu-id="4296b-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="4296b-107">Essa propriedade é inicializada como 0 pela [ação CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="4296b-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4296b-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4296b-108">Remarks</span></span>

<span data-ttu-id="4296b-109">Para obter um exemplo de como criar um "Aguarde.</span><span class="sxs-lookup"><span data-stu-id="4296b-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="4296b-110">.</span><span class="sxs-lookup"><span data-stu-id="4296b-110">.</span></span> <span data-ttu-id="4296b-111">.</span><span class="sxs-lookup"><span data-stu-id="4296b-111">.</span></span> <span data-ttu-id="4296b-112">"caixa de diálogo que aparece durante o custo de espaço em disco, consulte a seção [criação de uma condicional" Aguarde... " Caixa de mensagem](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="4296b-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4296b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4296b-113">Requirements</span></span>



| <span data-ttu-id="4296b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4296b-114">Requirement</span></span> | <span data-ttu-id="4296b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4296b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4296b-116">Versão</span><span class="sxs-lookup"><span data-stu-id="4296b-116">Version</span></span><br/> | <span data-ttu-id="4296b-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4296b-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4296b-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4296b-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4296b-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4296b-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4296b-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4296b-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4296b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4296b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4296b-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4296b-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




