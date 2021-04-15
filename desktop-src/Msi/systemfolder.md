---
description: O instalador define a propriedade SystemFolder como o caminho completo da pasta do sistema.
ms.assetid: 23883638-8d3d-4c2a-8ebf-0c306cf01e05
title: Propriedade SystemFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2abce6e4aa91289ef17134ab3cb878a665d3097c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760826"
---
# <a name="systemfolder-property"></a><span data-ttu-id="b37d9-103">Propriedade SystemFolder</span><span class="sxs-lookup"><span data-stu-id="b37d9-103">SystemFolder property</span></span>

<span data-ttu-id="b37d9-104">O instalador define a propriedade **SystemFolder** como o caminho completo da pasta do sistema.</span><span class="sxs-lookup"><span data-stu-id="b37d9-104">The installer sets the **SystemFolder** property to the full path of the System folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="b37d9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b37d9-105">Remarks</span></span>

<span data-ttu-id="b37d9-106">O instalador define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="b37d9-106">The installer sets this property.</span></span> <span data-ttu-id="b37d9-107">Por exemplo, no Windows de 32 bits, o valor pode ser C: \\ Windows \\ System32.</span><span class="sxs-lookup"><span data-stu-id="b37d9-107">For example, on 32-bit Windows the value may be C:\\Windows\\System32.</span></span> <span data-ttu-id="b37d9-108">No Windows de 64 bits, o valor pode ser C: \\ Windows \\ SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="b37d9-108">On 64-bit Windows, the value may be C:\\Windows\\SysWow64.</span></span>

<span data-ttu-id="b37d9-109">Essa pasta normalmente é um subdiretório da pasta do Windows.</span><span class="sxs-lookup"><span data-stu-id="b37d9-109">This folder is normally a subdirectory of the Windows folder.</span></span> <span data-ttu-id="b37d9-110">No entanto, ele reside em um servidor quando configurado para janelas compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="b37d9-110">However, it resides on a server when configured for Shared Windows.</span></span>

<span data-ttu-id="b37d9-111">Essa pasta é local, mesmo quando configurada para janelas compartilhadas.</span><span class="sxs-lookup"><span data-stu-id="b37d9-111">This folder is local, even when configured for shared Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="b37d9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b37d9-112">Requirements</span></span>



| <span data-ttu-id="b37d9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b37d9-113">Requirement</span></span> | <span data-ttu-id="b37d9-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b37d9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b37d9-115">Versão</span><span class="sxs-lookup"><span data-stu-id="b37d9-115">Version</span></span><br/> | <span data-ttu-id="b37d9-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b37d9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b37d9-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b37d9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b37d9-118">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b37d9-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b37d9-119">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b37d9-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b37d9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b37d9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b37d9-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b37d9-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




