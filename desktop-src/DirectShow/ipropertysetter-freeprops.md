---
description: 'O método FreeProps libera recursos alocados pelo método IPropertySetter:: GetProps. Chame esse método depois de chamar GetProps, passando-o para as estruturas retornadas por GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Método IPropertySetter:: FreeProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766990"
---
# <a name="ipropertysetterfreeprops-method"></a><span data-ttu-id="ace7d-104">Método IPropertySetter:: FreeProps</span><span class="sxs-lookup"><span data-stu-id="ace7d-104">IPropertySetter::FreeProps method</span></span>

> [!Note]  
> <span data-ttu-id="ace7d-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ace7d-105">\[Deprecated.</span></span> <span data-ttu-id="ace7d-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ace7d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ace7d-107">O `FreeProps` método libera recursos alocados pelo método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="ace7d-107">The `FreeProps` method frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span> <span data-ttu-id="ace7d-108">Chame esse método depois de chamar **GetProps**, passando-o para as estruturas retornadas por **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="ace7d-108">Call this method after calling **GetProps**, passing it the structures returned by **GetProps**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace7d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ace7d-109">Syntax</span></span>


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="ace7d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ace7d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace7d-111">*cParams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace7d-111">*cParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace7d-112">O número de elementos na matriz *paParam* .</span><span class="sxs-lookup"><span data-stu-id="ace7d-112">The number of elements in the *paParam* array.</span></span>

</dd> <dt>

<span data-ttu-id="ace7d-113">*paParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace7d-113">*paParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace7d-114">Ponteiro para uma matriz de [**estruturas \_ param Dexter**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="ace7d-114">Pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="ace7d-115">*paValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ace7d-115">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace7d-116">Ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="ace7d-116">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace7d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ace7d-117">Return value</span></span>

<span data-ttu-id="ace7d-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ace7d-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ace7d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ace7d-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ace7d-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ace7d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ace7d-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ace7d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ace7d-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ace7d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ace7d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ace7d-123">Requirements</span></span>



| <span data-ttu-id="ace7d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ace7d-124">Requirement</span></span> | <span data-ttu-id="ace7d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ace7d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ace7d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ace7d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ace7d-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace7d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ace7d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ace7d-128">Library</span></span><br/> | <dl> <span data-ttu-id="ace7d-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ace7d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ace7d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="ace7d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace7d-131">**Interface IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="ace7d-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="ace7d-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ace7d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




