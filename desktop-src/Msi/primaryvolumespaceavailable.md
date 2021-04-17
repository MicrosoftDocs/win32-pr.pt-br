---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceAvailable como uma cadeia de caracteres que representa o número total de bytes disponíveis, em unidades de 512, no volume referenciado pela propriedade PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propriedade PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747955"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="507cd-103">Propriedade PrimaryVolumeSpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="507cd-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="507cd-104">O instalador define o valor da propriedade **PrimaryVolumeSpaceAvailable** como uma cadeia de caracteres que representa o número total de bytes disponíveis, em unidades de 512, no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="507cd-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="507cd-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="507cd-105">Remarks</span></span>

<span data-ttu-id="507cd-106">Por exemplo, se [**PrimaryVolumePath**](primaryvolumepath.md) for definido como "D:" e o volume D: tiver 446.134.272 bytes livres, **PrimaryVolumeSpaceAvailable** será definido como 871356.</span><span class="sxs-lookup"><span data-stu-id="507cd-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="507cd-107">Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="507cd-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="507cd-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="507cd-108">Requirements</span></span>



| <span data-ttu-id="507cd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="507cd-109">Requirement</span></span> | <span data-ttu-id="507cd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="507cd-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="507cd-111">Versão</span><span class="sxs-lookup"><span data-stu-id="507cd-111">Version</span></span><br/> | <span data-ttu-id="507cd-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="507cd-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="507cd-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="507cd-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="507cd-114">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="507cd-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="507cd-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="507cd-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="507cd-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="507cd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507cd-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="507cd-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




