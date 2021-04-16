---
description: Observe que essa interface foi preterida.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: 'IAMFilterData: método arseFilterData de:P (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768643"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="b3688-103">IAMFilterData: método arseFilterData de:P</span><span class="sxs-lookup"><span data-stu-id="b3688-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="b3688-104">Essa interface foi substituída.</span><span class="sxs-lookup"><span data-stu-id="b3688-104">This interface has been deprecated.</span></span> <span data-ttu-id="b3688-105">Novos aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="b3688-105">New applications should not use it.</span></span>

 

<span data-ttu-id="b3688-106">O `ParseFilterData` método desempacota os dados de registro binários para um filtro.</span><span class="sxs-lookup"><span data-stu-id="b3688-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="b3688-107">Normalmente, não há motivo para um aplicativo chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b3688-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="b3688-108">O método [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) fornece uma maneira mais conveniente de acessar os dados do registro de filtro.</span><span class="sxs-lookup"><span data-stu-id="b3688-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3688-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3688-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="b3688-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3688-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3688-111">*rgbFilterData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3688-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3688-112">Ponteiro para os dados do registro binário.</span><span class="sxs-lookup"><span data-stu-id="b3688-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="b3688-113">Você pode obter esses dados recuperando a propriedade "FilterData" do moniker do filtro.</span><span class="sxs-lookup"><span data-stu-id="b3688-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="b3688-114">Os dados são armazenados como um **SafeArray** de bytes ( \_ matriz VT UI1 \| VT \_ ).</span><span class="sxs-lookup"><span data-stu-id="b3688-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="b3688-115">*CB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3688-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3688-116">Especifica o tamanho dos dados binários, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b3688-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b3688-117">*prgbRegFilter2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3688-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3688-118">Endereço de uma variável que recebe um ponteiro para os dados desempacotados.</span><span class="sxs-lookup"><span data-stu-id="b3688-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="b3688-119">Quando o método retorna, converta esse ponteiro para um tipo [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para acessar os dados de filtro.</span><span class="sxs-lookup"><span data-stu-id="b3688-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="b3688-120">O chamador deve liberar a memória chamando o método **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="b3688-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3688-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3688-121">Return value</span></span>

<span data-ttu-id="b3688-122">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3688-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b3688-123">Se falhar, retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="b3688-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3688-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3688-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b3688-125">O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b3688-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3688-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3688-126">Requirements</span></span>



| <span data-ttu-id="b3688-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3688-127">Requirement</span></span> | <span data-ttu-id="b3688-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b3688-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3688-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3688-129">Header</span></span><br/> | <dl> <span data-ttu-id="b3688-130"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3688-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="b3688-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b3688-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="b3688-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3688-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b3688-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3688-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3688-134">**Interface IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="b3688-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




