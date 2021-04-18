---
description: O instalador define o valor da propriedade PrimaryVolumeSpaceRemaining como uma cadeia de caracteres que representa o número total de bytes restantes no volume referenciado pela propriedade PrimaryVolumePath, se todos os recursos selecionados no momento forem instalados.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propriedade PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752841"
---
# <a name="primaryvolumespaceremaining-property"></a><span data-ttu-id="daff3-103">Propriedade PrimaryVolumeSpaceRemaining</span><span class="sxs-lookup"><span data-stu-id="daff3-103">PrimaryVolumeSpaceRemaining property</span></span>

<span data-ttu-id="daff3-104">O instalador define o valor da propriedade **PrimaryVolumeSpaceRemaining** como uma cadeia de caracteres que representa o número total de bytes restantes no volume referenciado pela propriedade [**PrimaryVolumePath**](primaryvolumepath.md) , se todos os recursos selecionados no momento forem instalados.</span><span class="sxs-lookup"><span data-stu-id="daff3-104">The installer sets the value of the **PrimaryVolumeSpaceRemaining** property to a string representing the total number of bytes remaining on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property, if all currently selected features were installed.</span></span> <span data-ttu-id="daff3-105">Assim como acontece com a propriedade [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , esse número é expresso em unidades de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="daff3-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="daff3-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="daff3-106">Remarks</span></span>

<span data-ttu-id="daff3-107">Observação Se esse valor for para ser exibido em um [controle de texto](text-control.md)estático, o bit de [formatação](formatsize-control-attribute.md) poderá ser usado para formatar e rotular automaticamente esse número em unidades de kilobytes ou megabytes conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="daff3-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="daff3-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daff3-108">Requirements</span></span>



| <span data-ttu-id="daff3-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="daff3-109">Requirement</span></span> | <span data-ttu-id="daff3-110">Valor</span><span class="sxs-lookup"><span data-stu-id="daff3-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daff3-111">Versão</span><span class="sxs-lookup"><span data-stu-id="daff3-111">Version</span></span><br/> | <span data-ttu-id="daff3-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="daff3-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="daff3-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="daff3-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="daff3-114">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="daff3-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="daff3-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="daff3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daff3-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="daff3-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




