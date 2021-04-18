---
description: A propriedade SOURCElist é uma lista delimitada por ponto-e-vírgula de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propriedade SOURCElist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748568"
---
# <a name="sourcelist-property"></a><span data-ttu-id="b92b5-103">Propriedade SOURCElist</span><span class="sxs-lookup"><span data-stu-id="b92b5-103">SOURCELIST property</span></span>

<span data-ttu-id="b92b5-104">A propriedade **SourceList** é uma lista delimitada por ponto-e-vírgula de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b92b5-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="b92b5-105">Essa lista é anexada ao final da lista de origem existente de cada usuário para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b92b5-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="b92b5-106">O instalador localiza uma fonte enumerando a lista de caminhos de origem e usa o primeiro local acessível encontrado.</span><span class="sxs-lookup"><span data-stu-id="b92b5-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="b92b5-107">Somente essa fonte pode ser usada para o restante da instalação.</span><span class="sxs-lookup"><span data-stu-id="b92b5-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="b92b5-108">Cada caminho especificado na lista de origem deve, portanto, ser um local que tenha uma origem completa para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b92b5-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="b92b5-109">A árvore de diretórios inteira em cada local de origem deve ser a mesma e deve incluir todos os arquivos de origem necessários, incluindo todos os gabinetes.</span><span class="sxs-lookup"><span data-stu-id="b92b5-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="b92b5-110">Cada local deve ter um arquivo. msi com o mesmo nome de arquivo e código de produto.</span><span class="sxs-lookup"><span data-stu-id="b92b5-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="b92b5-111">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="b92b5-111">Default Value</span></span>

<span data-ttu-id="b92b5-112">O instalador só verificará a propriedade **SourceList** se o produto ainda não tiver sido anunciado ou instalado.</span><span class="sxs-lookup"><span data-stu-id="b92b5-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="b92b5-113">Em todos os outros casos, o instalador usa a lista de origem existente que está no registro.</span><span class="sxs-lookup"><span data-stu-id="b92b5-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="b92b5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b92b5-114">Remarks</span></span>

<span data-ttu-id="b92b5-115">As fontes adicionadas usando a propriedade **SourceList** são adicionadas diretamente ao final da lista para cada tipo de origem e sempre vêm após a origem padrão especificada pela propriedade [**SourceDir**](sourcedir.md) .</span><span class="sxs-lookup"><span data-stu-id="b92b5-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="b92b5-116">Por Windows Installer o número de fontes na propriedade **SourceList** é ilimitado.</span><span class="sxs-lookup"><span data-stu-id="b92b5-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="b92b5-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) pode ser usado para adicionar fontes de rede.</span><span class="sxs-lookup"><span data-stu-id="b92b5-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="b92b5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b92b5-118">Requirements</span></span>



| <span data-ttu-id="b92b5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92b5-119">Requirement</span></span> | <span data-ttu-id="b92b5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b92b5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b92b5-121">Versão</span><span class="sxs-lookup"><span data-stu-id="b92b5-121">Version</span></span><br/> | <span data-ttu-id="b92b5-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b92b5-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b92b5-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b92b5-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b92b5-124">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b92b5-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b92b5-125">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b92b5-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b92b5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b92b5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92b5-127">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b92b5-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="b92b5-128">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="b92b5-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




