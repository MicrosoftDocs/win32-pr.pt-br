---
description: Especifica um filtro de compactação a ser usado ao renderizar o grupo especificado.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: 'Método ISmartRenderEngine:: SetGroupCompressor (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810214"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a><span data-ttu-id="d2d26-103">Método ISmartRenderEngine:: SetGroupCompressor</span><span class="sxs-lookup"><span data-stu-id="d2d26-103">ISmartRenderEngine::SetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="d2d26-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d2d26-104">\[Deprecated.</span></span> <span data-ttu-id="d2d26-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d2d26-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d2d26-106">Especifica um filtro de compactação a ser usado ao renderizar o grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="d2d26-106">Specifies a compression filter to use when rendering the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d26-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2d26-107">Syntax</span></span>


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="d2d26-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2d26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d26-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="d2d26-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d26-110">Índice de base zero do grupo.</span><span class="sxs-lookup"><span data-stu-id="d2d26-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="d2d26-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="d2d26-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d26-112">Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro de compactação.</span><span class="sxs-lookup"><span data-stu-id="d2d26-112">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d26-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2d26-113">Return value</span></span>

<span data-ttu-id="d2d26-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d2d26-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d2d26-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d2d26-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2d26-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2d26-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d2d26-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d2d26-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d2d26-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d2d26-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d2d26-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d2d26-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d2d26-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2d26-120">Requirements</span></span>



| <span data-ttu-id="d2d26-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d26-121">Requirement</span></span> | <span data-ttu-id="d2d26-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d2d26-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d26-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2d26-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d2d26-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d26-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d2d26-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2d26-125">Library</span></span><br/> | <dl> <span data-ttu-id="d2d26-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2d26-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d26-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2d26-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d26-128">**Interface ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="d2d26-128">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="d2d26-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d2d26-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




