---
description: O valor da propriedade Resumo da entidade transmite o nome do produto, da transformação ou do patch que é instalado pelo pacote.
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: Propriedade de resumo do assunto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747319"
---
# <a name="subject-summary-property"></a><span data-ttu-id="71836-103">Propriedade de resumo do assunto</span><span class="sxs-lookup"><span data-stu-id="71836-103">Subject Summary property</span></span>

<span data-ttu-id="71836-104">O valor da propriedade **Resumo da entidade** transmite o nome do produto, da transformação ou do patch que é instalado pelo pacote.</span><span class="sxs-lookup"><span data-stu-id="71836-104">The value of the **Subject Summary** property conveys the name of the product, transform, or patch that is installed by the package.</span></span>

<span data-ttu-id="71836-105">Cabe ao autor de um banco de dados de instalação, transformação ou pacote de patch para fornecer o valor dessa propriedade nas informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="71836-105">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="71836-106">Os autores devem fazer o seguinte para determinar o valor correto.</span><span class="sxs-lookup"><span data-stu-id="71836-106">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="71836-107">Defina a propriedade **Resumo do assunto** em um pacote de instalação para o mesmo valor que a propriedade [**ProductName**](productname.md) .</span><span class="sxs-lookup"><span data-stu-id="71836-107">Set the **Subject Summary** property in an installation package to the same value as the [**ProductName**](productname.md) property.</span></span>
-   <span data-ttu-id="71836-108">Defina a propriedade **Resumo da entidade** em uma transformação para o mesmo valor que a propriedade Resumo do **assunto** no pacote de instalação original.</span><span class="sxs-lookup"><span data-stu-id="71836-108">Set the **Subject Summary** property in a transform to the same value as the **Subject Summary** property in the original installation package.</span></span>
-   <span data-ttu-id="71836-109">Defina a propriedade **Resumo do assunto** nas informações resumidas de um pacote de patch para uma breve descrição do patch que inclui o nome do produto.</span><span class="sxs-lookup"><span data-stu-id="71836-109">Set the **Subject Summary** property in the summary information of a patch package to a short description of the patch that includes the name of the product.</span></span>

## <a name="requirements"></a><span data-ttu-id="71836-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71836-110">Requirements</span></span>



| <span data-ttu-id="71836-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="71836-111">Requirement</span></span> | <span data-ttu-id="71836-112">Valor</span><span class="sxs-lookup"><span data-stu-id="71836-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71836-113">Versão</span><span class="sxs-lookup"><span data-stu-id="71836-113">Version</span></span><br/> | <span data-ttu-id="71836-114">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="71836-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="71836-115">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="71836-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="71836-116">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="71836-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71836-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="71836-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71836-118">**PATCHNEWSUMMARYSUBJECT**</span><span class="sxs-lookup"><span data-stu-id="71836-118">**PATCHNEWSUMMARYSUBJECT**</span></span>](patchnewsummarysubject.md)
</dt> <dt>

[<span data-ttu-id="71836-119">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="71836-119">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




