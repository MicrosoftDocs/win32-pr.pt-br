---
description: A interface IXml2Dex salva e carrega arquivos de projeto de serviços de edição do DirectShow (DES) em linguagem XML (XML). Essa interface também fornece métodos para ler e gravar arquivos do grafo do DirectShow (. GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interface IXml2Dex (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780049"
---
# <a name="ixml2dex-interface"></a><span data-ttu-id="84e74-104">Interface IXml2Dex</span><span class="sxs-lookup"><span data-stu-id="84e74-104">IXml2Dex interface</span></span>

> [!Note]  
> <span data-ttu-id="84e74-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="84e74-105">\[Deprecated.</span></span> <span data-ttu-id="84e74-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="84e74-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="84e74-107">A `IXml2Dex` interface salva e carrega arquivos de projeto de [serviços de edição do DirectShow](directshow-editing-services.md) (DES) em linguagem XML (XML).</span><span class="sxs-lookup"><span data-stu-id="84e74-107">The `IXml2Dex` interface saves and loads [DirectShow Editing Services](directshow-editing-services.md) (DES) project files in Extensible Markup Language (XML).</span></span> <span data-ttu-id="84e74-108">Essa interface também fornece métodos para ler e gravar arquivos do grafo do DirectShow (. GRF).</span><span class="sxs-lookup"><span data-stu-id="84e74-108">This interface also provides methods for reading and writing DirectShow graph (.grf) files.</span></span>

## <a name="members"></a><span data-ttu-id="84e74-109">Membros</span><span class="sxs-lookup"><span data-stu-id="84e74-109">Members</span></span>

<span data-ttu-id="84e74-110">A interface **IXml2Dex** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="84e74-110">The **IXml2Dex** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="84e74-111">**IXml2Dex** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="84e74-111">**IXml2Dex** also has these types of members:</span></span>

-   [<span data-ttu-id="84e74-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="84e74-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="84e74-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="84e74-113">Methods</span></span>

<span data-ttu-id="84e74-114">A interface **IXml2Dex** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="84e74-114">The **IXml2Dex** interface has these methods.</span></span>



| <span data-ttu-id="84e74-115">Método</span><span class="sxs-lookup"><span data-stu-id="84e74-115">Method</span></span>                                                      | <span data-ttu-id="84e74-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="84e74-116">Description</span></span>                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="84e74-117">**CopyXML**</span><span class="sxs-lookup"><span data-stu-id="84e74-117">**CopyXML**</span></span>](ixml2dex-copyxml.md)                         | <span data-ttu-id="84e74-118">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-118">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-119">**CreateGraphFromFile**</span><span class="sxs-lookup"><span data-stu-id="84e74-119">**CreateGraphFromFile**</span></span>](ixml2dex-creategraphfromfile.md) | <span data-ttu-id="84e74-120">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-120">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-121">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="84e74-121">**Delete**</span></span>](ixml2dex-delete.md)                           | <span data-ttu-id="84e74-122">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-122">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-123">**PasteXML**</span><span class="sxs-lookup"><span data-stu-id="84e74-123">**PasteXML**</span></span>](ixml2dex-pastexml.md)                       | <span data-ttu-id="84e74-124">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-124">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-125">**PasteXMLFile**</span><span class="sxs-lookup"><span data-stu-id="84e74-125">**PasteXMLFile**</span></span>](ixml2dex-pastexmlfile.md)               | <span data-ttu-id="84e74-126">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-126">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-127">**ReadXML**</span><span class="sxs-lookup"><span data-stu-id="84e74-127">**ReadXML**</span></span>](ixml2dex-readxml.md)                         | <span data-ttu-id="84e74-128">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-128">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-129">**ReadXMLfile**</span><span class="sxs-lookup"><span data-stu-id="84e74-129">**ReadXMLFile**</span></span>](ixml2dex-readxmlfile.md)                 | <span data-ttu-id="84e74-130">Carrega um arquivo de projeto XML.</span><span class="sxs-lookup"><span data-stu-id="84e74-130">Loads an XML project file.</span></span><br/>                                      |
| [<span data-ttu-id="84e74-131">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="84e74-131">**Reset**</span></span>](ixml2dex-reset.md)                             | <span data-ttu-id="84e74-132">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-132">Not implemented.</span></span><br/>                                                |
| [<span data-ttu-id="84e74-133">**WriteGrfFile**</span><span class="sxs-lookup"><span data-stu-id="84e74-133">**WriteGrfFile**</span></span>](ixml2dex-writegrffile.md)               | <span data-ttu-id="84e74-134">Grava um gráfico de filtro em um arquivo no formato. GRF.</span><span class="sxs-lookup"><span data-stu-id="84e74-134">Writes a filter graph to a file in .grf format.</span></span><br/>                 |
| [<span data-ttu-id="84e74-135">**WriteXML**</span><span class="sxs-lookup"><span data-stu-id="84e74-135">**WriteXML**</span></span>](ixml2dex-writexml.md)                       | <span data-ttu-id="84e74-136">Traduz uma linha do tempo para uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="84e74-136">Translates a timeline to an XML string.</span></span><br/>                         |
| [<span data-ttu-id="84e74-137">**WriteXMLfile**</span><span class="sxs-lookup"><span data-stu-id="84e74-137">**WriteXMLFile**</span></span>](ixml2dex-writexmlfile.md)               | <span data-ttu-id="84e74-138">Traduz uma linha do tempo para XML e grava os dados XML em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="84e74-138">Translates a timeline to XML and writes the XML data to a file.</span></span><br/> |
| [<span data-ttu-id="84e74-139">**WriteXMLPart**</span><span class="sxs-lookup"><span data-stu-id="84e74-139">**WriteXMLPart**</span></span>](ixml2dex-writexmlpart.md)               | <span data-ttu-id="84e74-140">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="84e74-140">Not implemented.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="84e74-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="84e74-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="84e74-142">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="84e74-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="84e74-143">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="84e74-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="84e74-144">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="84e74-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="84e74-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84e74-145">Requirements</span></span>



| <span data-ttu-id="84e74-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="84e74-146">Requirement</span></span> | <span data-ttu-id="84e74-147">Valor</span><span class="sxs-lookup"><span data-stu-id="84e74-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84e74-148">Versão</span><span class="sxs-lookup"><span data-stu-id="84e74-148">Version</span></span><br/> | <span data-ttu-id="84e74-149">Internet Explorer 4,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="84e74-149">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="84e74-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84e74-150">Header</span></span><br/>  | <dl> <span data-ttu-id="84e74-151"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="84e74-151"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="84e74-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84e74-152">Library</span></span><br/> | <dl> <span data-ttu-id="84e74-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84e74-153"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
