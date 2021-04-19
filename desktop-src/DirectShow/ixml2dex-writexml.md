---
description: O método WriteXML converte uma linha do tempo em uma cadeia de caracteres XML.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'Método IXml2Dex:: WriteXML (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782191"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="eed9a-103">Método IXml2Dex:: WriteXML</span><span class="sxs-lookup"><span data-stu-id="eed9a-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="eed9a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="eed9a-104">\[Deprecated.</span></span> <span data-ttu-id="eed9a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eed9a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eed9a-106">O `WriteXML` método traduz uma linha do tempo para uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="eed9a-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed9a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eed9a-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="eed9a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eed9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed9a-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="eed9a-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="eed9a-110">Ponteiro para a interface **IUnknown** do objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="eed9a-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="eed9a-111">*pbstrXML*</span><span class="sxs-lookup"><span data-stu-id="eed9a-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="eed9a-112">Ponteiro para uma variável do tipo BSTR que recebe a cadeia de caracteres XML que descreve a linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="eed9a-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eed9a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eed9a-113">Return value</span></span>

<span data-ttu-id="eed9a-114">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="eed9a-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="eed9a-115">Se não houver memória suficiente para a conversão, retornará E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="eed9a-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="eed9a-116">Caso contrário, retorna outro código de erro.</span><span class="sxs-lookup"><span data-stu-id="eed9a-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed9a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="eed9a-117">Remarks</span></span>

<span data-ttu-id="eed9a-118">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="eed9a-118">The method allocates memory for the string.</span></span> <span data-ttu-id="eed9a-119">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="eed9a-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="eed9a-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="eed9a-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eed9a-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eed9a-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eed9a-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eed9a-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eed9a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed9a-123">Requirements</span></span>



| <span data-ttu-id="eed9a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed9a-124">Requirement</span></span> | <span data-ttu-id="eed9a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="eed9a-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eed9a-126">Versão</span><span class="sxs-lookup"><span data-stu-id="eed9a-126">Version</span></span><br/> | <span data-ttu-id="eed9a-127">Internet Explorer 4,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="eed9a-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="eed9a-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eed9a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="eed9a-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eed9a-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eed9a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eed9a-130">Library</span></span><br/> | <dl> <span data-ttu-id="eed9a-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eed9a-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed9a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="eed9a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed9a-133">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="eed9a-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="eed9a-134">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="eed9a-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




