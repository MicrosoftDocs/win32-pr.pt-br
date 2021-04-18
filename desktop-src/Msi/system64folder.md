---
description: O instalador define a propriedade System64Folder como o caminho completo para a pasta System64 predefinida. A propriedade System64Folder existente é definida como a pasta correspondente de 32 bits.
ms.assetid: ce25c95e-cff5-44ec-81cb-b3104fb9b987
title: Propriedade System64Folder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62e05f9067c4f5a77b5361fdefe0f5b47b9116ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750214"
---
# <a name="system64folder-property"></a><span data-ttu-id="ca07d-104">Propriedade System64Folder</span><span class="sxs-lookup"><span data-stu-id="ca07d-104">System64Folder property</span></span>

<span data-ttu-id="ca07d-105">O instalador define a propriedade **System64Folder** como o caminho completo para a pasta System64 predefinida.</span><span class="sxs-lookup"><span data-stu-id="ca07d-105">The installer sets the **System64Folder** property to the full path to the predefined System64 folder.</span></span> <span data-ttu-id="ca07d-106">A propriedade **System64Folder** existente é definida como a pasta correspondente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ca07d-106">The existing **System64Folder** property is set to the corresponding 32-bit folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca07d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca07d-107">Remarks</span></span>

<span data-ttu-id="ca07d-108">O instalador define essa propriedade no Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ca07d-108">The installer sets this property on 64-bit Windows.</span></span> <span data-ttu-id="ca07d-109">Por exemplo, no Windows de 64 bits, o valor pode ser C: \\ Window \\ System32.</span><span class="sxs-lookup"><span data-stu-id="ca07d-109">For example, on 64-bit Windows, the value may be C:\\Window\\System32.</span></span> <span data-ttu-id="ca07d-110">Essa propriedade não é usada em janelas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="ca07d-110">This property is not used on 32-bit Windows.</span></span>

<span data-ttu-id="ca07d-111">Essa pasta normalmente é um subdiretório da pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="ca07d-111">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="ca07d-112">No entanto, ele reside em um servidor quando configurado para janelas compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="ca07d-112">However, it resides on a server when configured for Shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca07d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca07d-113">Requirements</span></span>



| <span data-ttu-id="ca07d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca07d-114">Requirement</span></span> | <span data-ttu-id="ca07d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ca07d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca07d-116">Versão</span><span class="sxs-lookup"><span data-stu-id="ca07d-116">Version</span></span><br/> | <span data-ttu-id="ca07d-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ca07d-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca07d-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ca07d-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca07d-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca07d-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ca07d-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ca07d-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca07d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca07d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca07d-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ca07d-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




