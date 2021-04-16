---
description: O método WriteGrfFile grava um grafo de filtro em um arquivo no formato. GRF.
ms.assetid: 2064d2d7-34ac-465c-ae09-d125c670d0e8
title: 'Método IXml2Dex:: WriteGrfFile (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteGrfFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a411540d95a7313070a643b7b1895b564a49e089
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779840"
---
# <a name="ixml2dexwritegrffile-method"></a><span data-ttu-id="3cd6c-103">Método IXml2Dex:: WriteGrfFile</span><span class="sxs-lookup"><span data-stu-id="3cd6c-103">IXml2Dex::WriteGrfFile method</span></span>

> [!Note]  
> <span data-ttu-id="3cd6c-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-104">\[Deprecated.</span></span> <span data-ttu-id="3cd6c-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3cd6c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3cd6c-106">O `WriteGrfFile` método grava um gráfico de filtro em um arquivo no formato. GRF.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-106">The `WriteGrfFile` method writes a filter graph to a file in .grf format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd6c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cd6c-107">Syntax</span></span>


```C++
HRESULT WriteGrfFile(
   IUnknown *pGraph,
   BSTR     FileName
);
```



## <a name="parameters"></a><span data-ttu-id="3cd6c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3cd6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd6c-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="3cd6c-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd6c-110">Ponteiro para a interface **IUnknown** do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-110">Pointer to the filter graph's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="3cd6c-111">*FileName*</span><span class="sxs-lookup"><span data-stu-id="3cd6c-111">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd6c-112">Cadeia de caracteres que especifica o nome do arquivo a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-112">String that specifies the name of the file to write.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cd6c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3cd6c-113">Return value</span></span>

<span data-ttu-id="3cd6c-114">Retorna um valor **HRESULT** que depende da implementação da interface.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-114">Returns an **HRESULT** value that depends on the implementation of the interface.</span></span> <span data-ttu-id="3cd6c-115">HRESULT pode incluir uma das seguintes constantes padrão ou outros valores não listados.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-115">HRESULT can include one of the following standard constants, or other values not listed.</span></span>



| <span data-ttu-id="3cd6c-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3cd6c-116">Return code</span></span>                                                                                  | <span data-ttu-id="3cd6c-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="3cd6c-117">Description</span></span>                     |
|----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="3cd6c-118"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd6c-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="3cd6c-119">Falha.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-119">Failure.</span></span><br/>             |
| <dl> <span data-ttu-id="3cd6c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd6c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3cd6c-121">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-121">Argument is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="3cd6c-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3cd6c-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3cd6c-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-123">Success.</span></span><br/>             |



 

<span data-ttu-id="3cd6c-124">Esse método também pode retornar códigos de erro gerados por chamadas internas para os métodos **IStorage:: CreateStream** e **IPersist:: Save** .</span><span class="sxs-lookup"><span data-stu-id="3cd6c-124">This method can also return error codes generated by internal calls to the **IStorage::CreateStream** and **IPersist::Save** methods.</span></span> <span data-ttu-id="3cd6c-125">Para obter mais informações, consulte o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-125">For more information, see the Platform SDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd6c-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd6c-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3cd6c-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3cd6c-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3cd6c-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3cd6c-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3cd6c-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3cd6c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cd6c-130">Requirements</span></span>



| <span data-ttu-id="3cd6c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cd6c-131">Requirement</span></span> | <span data-ttu-id="3cd6c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3cd6c-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd6c-133">Versão</span><span class="sxs-lookup"><span data-stu-id="3cd6c-133">Version</span></span><br/> | <span data-ttu-id="3cd6c-134">Internet Explorer 4,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3cd6c-134">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="3cd6c-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3cd6c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3cd6c-136"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cd6c-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3cd6c-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3cd6c-137">Library</span></span><br/> | <dl> <span data-ttu-id="3cd6c-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cd6c-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cd6c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cd6c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cd6c-140">**Interface IXml2Dex**</span><span class="sxs-lookup"><span data-stu-id="3cd6c-140">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="3cd6c-141">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="3cd6c-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




