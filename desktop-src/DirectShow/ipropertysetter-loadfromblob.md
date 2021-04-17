---
description: O método LoadFromBlob carrega dados de propriedade de um formato de persistência.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'Método IPropertySetter:: LoadFromBlob (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783384"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="73ab3-103">Método IPropertySetter:: LoadFromBlob</span><span class="sxs-lookup"><span data-stu-id="73ab3-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="73ab3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="73ab3-104">\[Deprecated.</span></span> <span data-ttu-id="73ab3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73ab3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="73ab3-106">O `LoadFromBlob` método carrega dados de propriedade de um formato de persistência.</span><span class="sxs-lookup"><span data-stu-id="73ab3-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ab3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73ab3-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="73ab3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73ab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ab3-109">*cSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ab3-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ab3-110">Tamanho dos dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="73ab3-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="73ab3-111">*PB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="73ab3-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ab3-112">Ponteiro para uma matriz de bytes que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="73ab3-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ab3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73ab3-113">Return value</span></span>

<span data-ttu-id="73ab3-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73ab3-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73ab3-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73ab3-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73ab3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="73ab3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73ab3-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="73ab3-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="73ab3-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="73ab3-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="73ab3-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="73ab3-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73ab3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73ab3-120">Requirements</span></span>



| <span data-ttu-id="73ab3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ab3-121">Requirement</span></span> | <span data-ttu-id="73ab3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="73ab3-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73ab3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73ab3-123">Header</span></span><br/>  | <dl> <span data-ttu-id="73ab3-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="73ab3-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="73ab3-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73ab3-125">Library</span></span><br/> | <dl> <span data-ttu-id="73ab3-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73ab3-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ab3-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="73ab3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ab3-128">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="73ab3-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="73ab3-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="73ab3-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




