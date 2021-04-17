---
description: O objeto SummaryInfo é usado para ler, criar e atualizar propriedades de documento do fluxo de informações resumidas de um objeto de armazenamento.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Objeto SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747736"
---
# <a name="summaryinfo-object"></a><span data-ttu-id="d3466-103">Objeto SummaryInfo</span><span class="sxs-lookup"><span data-stu-id="d3466-103">SummaryInfo object</span></span>

<span data-ttu-id="d3466-104">O objeto **SummaryInfo** é usado para ler, criar e atualizar propriedades de documento do [fluxo de informações resumidas](summary-information-stream.md) de um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d3466-104">The **SummaryInfo** object is used to read, create, and update document properties from the [summary information stream](summary-information-stream.md) of a storage object.</span></span>

## <a name="members"></a><span data-ttu-id="d3466-105">Membros</span><span class="sxs-lookup"><span data-stu-id="d3466-105">Members</span></span>

<span data-ttu-id="d3466-106">O objeto **SummaryInfo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d3466-106">The **SummaryInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="d3466-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3466-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="d3466-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d3466-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d3466-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3466-109">Methods</span></span>

<span data-ttu-id="d3466-110">O objeto **SummaryInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d3466-110">The **SummaryInfo** object has these methods.</span></span>



| <span data-ttu-id="d3466-111">Método</span><span class="sxs-lookup"><span data-stu-id="d3466-111">Method</span></span>                                 | <span data-ttu-id="d3466-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3466-112">Description</span></span>                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3466-113">**Mantenha**</span><span class="sxs-lookup"><span data-stu-id="d3466-113">**Persist**</span></span>](summaryinfo-persist.md) | <span data-ttu-id="d3466-114">Formata e grava as propriedades armazenadas anteriormente no fluxo de [informações de resumo](summary-information-stream.md)padrão.</span><span class="sxs-lookup"><span data-stu-id="d3466-114">Formats and writes the previously stored properties into the standard [summary information stream](summary-information-stream.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d3466-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d3466-115">Properties</span></span>

<span data-ttu-id="d3466-116">O objeto **SummaryInfo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d3466-116">The **SummaryInfo** object has these properties.</span></span>



| <span data-ttu-id="d3466-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d3466-117">Property</span></span>                                                                             | <span data-ttu-id="d3466-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d3466-118">Description</span></span>                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3466-119">**Propriedade Property (objeto SummaryInfo)**</span><span class="sxs-lookup"><span data-stu-id="d3466-119">**Property Property (SummaryInfo Object)**</span></span>](summaryinfo-summaryinfo.md)<br/> | <span data-ttu-id="d3466-120">Obtém ou define o valor da propriedade especificada no fluxo de informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="d3466-120">Gets or sets the value for the specified property in the summary information stream.</span></span><br/> |
| [<span data-ttu-id="d3466-121">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="d3466-121">**PropertyCount**</span></span>](summaryinfo-propertycount.md)<br/>                        | <span data-ttu-id="d3466-122">Indica o número atual de valores de propriedade no objeto de informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="d3466-122">Indicates the current number of property values in the summary information object.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d3466-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3466-123">Requirements</span></span>



| <span data-ttu-id="d3466-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3466-124">Requirement</span></span> | <span data-ttu-id="d3466-125">Valor</span><span class="sxs-lookup"><span data-stu-id="d3466-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3466-126">Versão</span><span class="sxs-lookup"><span data-stu-id="d3466-126">Version</span></span><br/> | <span data-ttu-id="d3466-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d3466-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d3466-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d3466-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d3466-129">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="d3466-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d3466-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d3466-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3466-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3466-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d3466-132">IID</span><span class="sxs-lookup"><span data-stu-id="d3466-132">IID</span></span><br/>     | <span data-ttu-id="d3466-133">IID \_ ISummaryInfo é definido como 000C109B-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d3466-133">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="d3466-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3466-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3466-135">**Propriedade SummaryInformation (objeto Database)**</span><span class="sxs-lookup"><span data-stu-id="d3466-135">**SummaryInformation Property (Database Object)**</span></span>](database-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="d3466-136">**Propriedade SummaryInformation (objeto do instalador)**</span><span class="sxs-lookup"><span data-stu-id="d3466-136">**SummaryInformation Property (Installer Object)**</span></span>](installer-summaryinformation.md)
</dt> <dt>

[<span data-ttu-id="d3466-137">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d3466-137">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




