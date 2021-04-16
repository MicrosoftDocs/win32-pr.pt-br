---
description: O método WriteXMLfile converte uma linha do tempo em XML e grava os dados XML em um arquivo.
ms.assetid: 0a269e3d-6ca3-401e-bc22-6b4e8aacdbc9
title: 'Método IXml2Dex:: WriteXMLfile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXMLFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e8710ecb142adefbdb472bf0c18a2329e818210
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758837"
---
# <a name="ixml2dexwritexmlfile-method"></a><span data-ttu-id="82df2-103">Método IXml2Dex:: WriteXMLfile</span><span class="sxs-lookup"><span data-stu-id="82df2-103">IXml2Dex::WriteXMLFile method</span></span>

> [!Note]  
> <span data-ttu-id="82df2-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="82df2-104">\[Deprecated.</span></span> <span data-ttu-id="82df2-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="82df2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="82df2-106">O `WriteXMLFile` método converte uma linha do tempo em XML e grava os dados XML em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="82df2-106">The `WriteXMLFile` method translates a timeline to XML and writes the XML data to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="82df2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82df2-107">Syntax</span></span>


```C++
HRESULT WriteXMLFile(
   IUnknown *pTimeline,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="82df2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82df2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82df2-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="82df2-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="82df2-110">Ponteiro para a interface **IUnknown** do objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="82df2-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="82df2-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="82df2-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="82df2-112">Cadeia de caracteres que especifica o nome do arquivo a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="82df2-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82df2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82df2-113">Return value</span></span>

<span data-ttu-id="82df2-114">Retorna um valor **HRESULT** que depende da implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="82df2-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="82df2-115">O **HRESULT** pode incluir uma das seguintes constantes padrão ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="82df2-115">The **HRESULT** can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="82df2-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="82df2-116">Return code</span></span>                                                                                   | <span data-ttu-id="82df2-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="82df2-117">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="82df2-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="82df2-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="82df2-119">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="82df2-119">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="82df2-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="82df2-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="82df2-121">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="82df2-121">Insufficient memory.</span></span><br/> |
| <dl> <span data-ttu-id="82df2-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82df2-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="82df2-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="82df2-123">Success.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="82df2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="82df2-124">Remarks</span></span>

<span data-ttu-id="82df2-125">Esse método gera um arquivo XML que representa todos os componentes na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="82df2-125">This method generates an XML file that represents all the components in the timeline.</span></span>

> [!Note]  
> <span data-ttu-id="82df2-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="82df2-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="82df2-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="82df2-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="82df2-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="82df2-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="82df2-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82df2-129">Requirements</span></span>



| <span data-ttu-id="82df2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="82df2-130">Requirement</span></span> | <span data-ttu-id="82df2-131">Valor</span><span class="sxs-lookup"><span data-stu-id="82df2-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82df2-132">Versão</span><span class="sxs-lookup"><span data-stu-id="82df2-132">Version</span></span><br/> | <span data-ttu-id="82df2-133">Internet Explorer 4,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="82df2-133">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="82df2-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82df2-134">Header</span></span><br/>  | <dl> <span data-ttu-id="82df2-135"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="82df2-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="82df2-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82df2-136">Library</span></span><br/> | <dl> <span data-ttu-id="82df2-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82df2-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82df2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="82df2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82df2-139">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="82df2-139">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="82df2-140">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="82df2-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




