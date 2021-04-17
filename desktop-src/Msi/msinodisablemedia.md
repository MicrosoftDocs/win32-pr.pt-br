---
description: Defina a propriedade MSINODISABLEMEDIA para impedir que o instalador defina a propriedade DISABLEMEDIA. Definir a propriedade DISABLEMEDIA impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto.
ms.assetid: 4e1450aa-bf89-4d44-b463-4016660f5508
title: Propriedade MSINODISABLEMEDIA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93510263cbe182c66305dcc08c10d908709e1259
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748765"
---
# <a name="msinodisablemedia-property"></a><span data-ttu-id="e16b6-104">Propriedade MSINODISABLEMEDIA</span><span class="sxs-lookup"><span data-stu-id="e16b6-104">MSINODISABLEMEDIA property</span></span>

<span data-ttu-id="e16b6-105">Defina a propriedade **MSINODISABLEMEDIA** para impedir que o instalador defina a propriedade [**DISABLEMEDIA**](-disablemedia.md) .</span><span class="sxs-lookup"><span data-stu-id="e16b6-105">Set the **MSINODISABLEMEDIA** property to prevent the installer from setting the [**DISABLEMEDIA**](-disablemedia.md) property.</span></span> <span data-ttu-id="e16b6-106">Definir a propriedade **DISABLEMEDIA** impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto.</span><span class="sxs-lookup"><span data-stu-id="e16b6-106">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span>

<span data-ttu-id="e16b6-107">Quando **MSINODISABLEMEDIA** não estiver definido, o instalador poderá adicionar [**DISABLEMEDIA**](-disablemedia.md) ao fluxo de propriedade administrativa ao executar uma [instalação administrativa](administrative-installation.md).</span><span class="sxs-lookup"><span data-stu-id="e16b6-107">When **MSINODISABLEMEDIA** is not set, the installer might add [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream when performing an [administrative installation](administrative-installation.md).</span></span> <span data-ttu-id="e16b6-108">Isso impede que os usuários que instalam a partir da imagem administrativa nunca instalem a partir da mídia, como um CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="e16b6-108">This prevents users who install from the administrative image from ever installing from media, such as a CD-ROM.</span></span>

-   <span data-ttu-id="e16b6-109">Ao executar uma instalação administrativa, o instalador só adicionará [**DISABLEMEDIA**](-disablemedia.md) ao fluxo de propriedade administrativa se a propriedade de [**Resumo contagem de páginas**](page-count-summary.md) for menor que 150.</span><span class="sxs-lookup"><span data-stu-id="e16b6-109">When performing an administrative installation, the installer only adds [**DISABLEMEDIA**](-disablemedia.md) to the administrative property stream if the [**Page Count Summary**](page-count-summary.md) Property is less than 150.</span></span>

<span data-ttu-id="e16b6-110">Se [**DISABLEMEDIA**](-disablemedia.md) estiver listado na propriedade [**adminproperties**](adminproperties.md) , definir **MSINODISABLEMEDIA** impedirá que **DISABLEMEDIA** seja definido durante uma instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="e16b6-110">If [**DISABLEMEDIA**](-disablemedia.md) is listed in the [**AdminProperties**](adminproperties.md) property, setting **MSINODISABLEMEDIA** prevents **DISABLEMEDIA** from being set during an administrative installation.</span></span> <span data-ttu-id="e16b6-111">Nesse caso, o instalador pode registrar uma fonte de mídia e um usuário pode ter a opção de reinstalar a partir da origem de mídia se a imagem de instalação administrativa original ficou indisponível posteriormente.</span><span class="sxs-lookup"><span data-stu-id="e16b6-111">In this case, the installer may register a media source and a user could then have the option to reinstall from the media source if the original administrative installation image became unavailable later.</span></span>

## <a name="requirements"></a><span data-ttu-id="e16b6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e16b6-112">Requirements</span></span>



| <span data-ttu-id="e16b6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e16b6-113">Requirement</span></span> | <span data-ttu-id="e16b6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e16b6-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e16b6-115">Versão</span><span class="sxs-lookup"><span data-stu-id="e16b6-115">Version</span></span><br/> | <span data-ttu-id="e16b6-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e16b6-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e16b6-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e16b6-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e16b6-118">Windows Installer no Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e16b6-118">Windows Installer on Windows Server 2003, Windows XP, and Windows 2000.</span></span> <span data-ttu-id="e16b6-119">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e16b6-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e16b6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e16b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16b6-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e16b6-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




