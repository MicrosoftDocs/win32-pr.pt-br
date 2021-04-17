---
description: Para um pacote de instalação, a propriedade Resumo do número de revisão contém o código do pacote do instalador.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Propriedade de resumo do número de revisão
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747739"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="f3eb9-103">Propriedade de resumo do número de revisão</span><span class="sxs-lookup"><span data-stu-id="f3eb9-103">Revision Number Summary property</span></span>

<span data-ttu-id="f3eb9-104">Para um pacote de instalação, a propriedade **Resumo do número de revisão** contém o código do [*pacote*](p-gly.md) do instalador.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="f3eb9-105">Para obter mais informações sobre códigos de pacote, consulte [Package codes](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3eb9-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="f3eb9-106">Para uma transformação, a propriedade **Resumo do número de revisão** lista os GUIDs de código do produto e a versão dos produtos novos e originais e o GUID do código de atualização.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="f3eb9-107">A lista é separada com ponto e vírgula da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="f3eb9-108">"Original-produto-código original-versão do produto; Código de New-Product novo – versão do produto; Atualizar código "</span><span class="sxs-lookup"><span data-stu-id="f3eb9-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="f3eb9-109">Para um pacote de patch, a propriedade **Resumo do número de revisão** especifica o código de patch GUID para o patch.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="f3eb9-110">Isso pode ser seguido por uma lista de GUIDs de código de patch para patches obsoletos que devem ser removidos quando esse patch é aplicado.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="f3eb9-111">Os códigos de patch são concatenados sem delimitadores separando GUIDs na lista.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="f3eb9-112">\* \* Windows Installer 3,0: \* \* se houver informações de sequenciamento presentes na [tabela MsiPatchSequence](msipatchsequence-table.md), Windows Installer 3,0 usará as informações de sequenciamento na tabela e ignorará a lista de patches obsoletos incluídos na propriedade **Resumo do número de revisão** .</span><span class="sxs-lookup"><span data-stu-id="f3eb9-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="f3eb9-113">Windows Installer 3,0 ainda poderá usar as informações de patch obsoletas na propriedade **Resumo do número de revisão** se o pacote não contiver uma tabela MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="f3eb9-114">\* \* Windows Installer 2,0: \* \* não há suporte para a [tabela MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f3eb9-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="f3eb9-115">Windows Installer 2,0 ainda poderá usar as informações de patch obsoletas na propriedade **Resumo do número de revisão** se o pacote não contiver uma tabela MsiPatchSequence.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="f3eb9-116">Essa propriedade de resumo é necessária.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3eb9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3eb9-117">Requirements</span></span>



| <span data-ttu-id="f3eb9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3eb9-118">Requirement</span></span> | <span data-ttu-id="f3eb9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f3eb9-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3eb9-120">Versão</span><span class="sxs-lookup"><span data-stu-id="f3eb9-120">Version</span></span><br/> | <span data-ttu-id="f3eb9-121">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f3eb9-122">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f3eb9-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f3eb9-123">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f3eb9-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3eb9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3eb9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3eb9-125">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="f3eb9-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




