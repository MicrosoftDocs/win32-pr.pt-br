---
description: A propriedade Resumo de palavras-chave em bancos de dados de instalação ou transformações contém uma lista de palavras-chave.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Propriedade de Resumo de palavras-chave
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759218"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="dbbd6-103">Propriedade de Resumo de palavras-chave</span><span class="sxs-lookup"><span data-stu-id="dbbd6-103">Keywords Summary property</span></span>

<span data-ttu-id="dbbd6-104">A propriedade **Resumo de palavras-chave** em bancos de dados de instalação ou transformações contém uma lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="dbbd6-105">As palavras-chave podem ser usadas por navegadores de arquivos para realizar pesquisas de palavra-chaves para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="dbbd6-106">Essa propriedade contém uma lista de fontes do patch em um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="dbbd6-107">Cabe ao autor de um banco de dados de instalação, transformação ou pacote de patch para fornecer o valor dessa propriedade nas informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="dbbd6-108">Os autores devem fazer o seguinte para determinar o valor correto.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="dbbd6-109">Em um pacote de instalação, defina o valor dessa propriedade como uma lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="dbbd6-110">A palavra-chave deve incluir "instalador", bem como palavras-chave específicas do produto, e pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="dbbd6-111">Em uma transformação, defina o valor dessa propriedade como uma lista de palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="dbbd6-112">A palavra-chave deve incluir "instalador", bem como palavras-chave específicas do produto, e pode ser localizada.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="dbbd6-113">Em um pacote de patch, defina o valor dessa propriedade como uma lista delimitada por ponto-e-vírgula de locais de rede ou URL para as fontes do patch.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="dbbd6-114">Quando o patch é instalado, o instalador o adiciona à lista de origem do pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="dbbd6-115">Se o patch armazenado em cache se tornar ausente, o instalador poderá pesquisar uma origem no local original, um local adicionado à lista de origem pela propriedade **Resumo de palavras-chave** ou um local adicionado à lista de origem usando as funções [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) ou [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) .</span><span class="sxs-lookup"><span data-stu-id="dbbd6-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbbd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbbd6-116">Requirements</span></span>



| <span data-ttu-id="dbbd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbbd6-117">Requirement</span></span> | <span data-ttu-id="dbbd6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="dbbd6-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbbd6-119">Versão</span><span class="sxs-lookup"><span data-stu-id="dbbd6-119">Version</span></span><br/> | <span data-ttu-id="dbbd6-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dbbd6-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dbbd6-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dbbd6-122">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="dbbd6-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbbd6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbbd6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbbd6-124">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="dbbd6-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




