---
description: A propriedade UpgradeCode é um GUID que representa um conjunto de produtos relacionado. O UpgradeCode é usado na tabela de atualização para pesquisar versões relacionadas do produto que já estão instaladas. Essa propriedade é usada pela ação RegisterProduct.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Propriedade UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751178"
---
# <a name="upgradecode-property"></a><span data-ttu-id="5c335-104">Propriedade UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="5c335-104">UpgradeCode property</span></span>

<span data-ttu-id="5c335-105">A propriedade **UpgradeCode** é um GUID que representa um conjunto de produtos relacionado.</span><span class="sxs-lookup"><span data-stu-id="5c335-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="5c335-106">O **UpgradeCode** é usado na [tabela de atualização](upgrade-table.md) para pesquisar versões relacionadas do produto que já estão instaladas.</span><span class="sxs-lookup"><span data-stu-id="5c335-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="5c335-107">Essa propriedade é usada pela [ação RegisterProduct](registerproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="5c335-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5c335-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c335-108">Remarks</span></span>

<span data-ttu-id="5c335-109">É altamente recomendável que os autores de pacotes de instalação especifiquem um **UpgradeCode** para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5c335-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c335-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c335-110">Requirements</span></span>



| <span data-ttu-id="5c335-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c335-111">Requirement</span></span> | <span data-ttu-id="5c335-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5c335-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c335-113">Versão</span><span class="sxs-lookup"><span data-stu-id="5c335-113">Version</span></span><br/> | <span data-ttu-id="5c335-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c335-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5c335-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5c335-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5c335-116">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5c335-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5c335-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5c335-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c335-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c335-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c335-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5c335-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="5c335-120">Aplicação de patch e atualizações</span><span class="sxs-lookup"><span data-stu-id="5c335-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="5c335-121">Preparando um aplicativo para atualizações principais futuras</span><span class="sxs-lookup"><span data-stu-id="5c335-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




