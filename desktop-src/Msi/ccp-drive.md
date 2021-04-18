---
description: A \_ propriedade da unidade CCP é definida como o caminho raiz do volume removível que deve ser pesquisado por RMCCPSearch.
ms.assetid: 567b7d11-6d80-4ec5-810d-f32b9ebf5809
title: Propriedade CCP_DRIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6215881cd3a998cd63a958bfe258ad3f9872ab1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778731"
---
# <a name="ccp_drive-property"></a><span data-ttu-id="26a67-103">\_Propriedade da unidade CCP</span><span class="sxs-lookup"><span data-stu-id="26a67-103">CCP\_DRIVE property</span></span>

<span data-ttu-id="26a67-104">A propriedade da **\_ unidade CCP** é definida como o caminho raiz do volume removível que deve ser pesquisado por [RMCCPSearch](rmccpsearch-action.md).</span><span class="sxs-lookup"><span data-stu-id="26a67-104">The **CCP\_DRIVE** property is set to the root path of the removable volume that is to be searched by [RMCCPSearch](rmccpsearch-action.md).</span></span> <span data-ttu-id="26a67-105">A ação RMCCPSearch usa assinaturas de arquivo para validar se os produtos qualificados estão instalados em um sistema antes de executar uma instalação de atualização.</span><span class="sxs-lookup"><span data-stu-id="26a67-105">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before performing an upgrade installation.</span></span>

<span data-ttu-id="26a67-106">Essa propriedade normalmente é definida por meio da interface do usuário ou de uma ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="26a67-106">This property is typically set via the user interface or a custom action.</span></span> <span data-ttu-id="26a67-107">Essa propriedade deve ser definida antes que a ação [RMCCPSearch](rmccpsearch-action.md) seja executada.</span><span class="sxs-lookup"><span data-stu-id="26a67-107">This property should be set before the [RMCCPSearch](rmccpsearch-action.md) action is run.</span></span>

## <a name="requirements"></a><span data-ttu-id="26a67-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26a67-108">Requirements</span></span>



| <span data-ttu-id="26a67-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="26a67-109">Requirement</span></span> | <span data-ttu-id="26a67-110">Valor</span><span class="sxs-lookup"><span data-stu-id="26a67-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26a67-111">Versão</span><span class="sxs-lookup"><span data-stu-id="26a67-111">Version</span></span><br/> | <span data-ttu-id="26a67-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="26a67-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="26a67-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="26a67-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="26a67-114">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="26a67-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="26a67-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="26a67-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26a67-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="26a67-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a67-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="26a67-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




