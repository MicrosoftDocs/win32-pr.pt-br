---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceRequired como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos selecionados no volume referenciado pela propriedade PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propriedade PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749784"
---
# <a name="primaryvolumespacerequired-property"></a><span data-ttu-id="279dd-103">Propriedade PrimaryVolumeSpaceRequired</span><span class="sxs-lookup"><span data-stu-id="279dd-103">PrimaryVolumeSpaceRequired property</span></span>

<span data-ttu-id="279dd-104">O instalador define o valor da propriedade **PrimaryVolumeSpaceRequired** como uma cadeia de caracteres que representa o número total de bytes exigidos por todos os recursos selecionados no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) .</span><span class="sxs-lookup"><span data-stu-id="279dd-104">The installer sets the value of the **PrimaryVolumeSpaceRequired** property to a string representing the total number of bytes required by all selected features on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span> <span data-ttu-id="279dd-105">Assim como acontece com a propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , esse número é expresso em unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="279dd-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="279dd-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="279dd-106">Remarks</span></span>

<span data-ttu-id="279dd-107">Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="279dd-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="279dd-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="279dd-108">Requirements</span></span>



| <span data-ttu-id="279dd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="279dd-109">Requirement</span></span> | <span data-ttu-id="279dd-110">Valor</span><span class="sxs-lookup"><span data-stu-id="279dd-110">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="279dd-111">Versão</span><span class="sxs-lookup"><span data-stu-id="279dd-111">Version</span></span><br/> | <span data-ttu-id="279dd-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="279dd-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="279dd-113">Windows Installer 4,0 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="279dd-113">Windows Installer 4.0 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="279dd-114">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="279dd-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="279dd-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="279dd-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="279dd-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="279dd-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="279dd-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="279dd-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




