---
description: Saiba mais sobre o método IAMFilterData::P arseFilterData, que desempacota os dados do Registro binário para um filtro. Essa interface foi substituída.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Método IAMFilterData::P arseFilterData (Fil \_ data.h)
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
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989441"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="2cd56-104">Método IAMFilterData::P arseFilterData</span><span class="sxs-lookup"><span data-stu-id="2cd56-104">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="2cd56-105">Essa interface foi substituída.</span><span class="sxs-lookup"><span data-stu-id="2cd56-105">This interface has been deprecated.</span></span> <span data-ttu-id="2cd56-106">Novos aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="2cd56-106">New applications should not use it.</span></span>

 

<span data-ttu-id="2cd56-107">O `ParseFilterData` método desempacotará os dados do Registro binário para um filtro.</span><span class="sxs-lookup"><span data-stu-id="2cd56-107">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="2cd56-108">Normalmente, não há motivo para um aplicativo chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="2cd56-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="2cd56-109">O [**método IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) fornece uma maneira mais conveniente de acessar os dados do registro de filtro.</span><span class="sxs-lookup"><span data-stu-id="2cd56-109">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cd56-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2cd56-110">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="2cd56-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cd56-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cd56-112">*rgbFilterData* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-112">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-113">Ponteiro para os dados binários do Registro.</span><span class="sxs-lookup"><span data-stu-id="2cd56-113">Pointer to the binary registry data.</span></span> <span data-ttu-id="2cd56-114">Você pode obter esses dados recuperando a propriedade "FilterData" do moniker de filtro.</span><span class="sxs-lookup"><span data-stu-id="2cd56-114">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="2cd56-115">Os dados são armazenados como **uma SAFEARRAY** de bytes (MATRIZ VT \_ UI1 \| \_ VT).</span><span class="sxs-lookup"><span data-stu-id="2cd56-115">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-116">*cb* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-116">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-117">Especifica o tamanho dos dados binários, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2cd56-117">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2cd56-118">*prgbRegFilter2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2cd56-118">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cd56-119">Endereço de uma variável que recebe um ponteiro para os dados desempacodados.</span><span class="sxs-lookup"><span data-stu-id="2cd56-119">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="2cd56-120">Quando o método retornar, castirá-lo para um [**tipo REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) para acessar os dados de filtro.</span><span class="sxs-lookup"><span data-stu-id="2cd56-120">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="2cd56-121">O chamador deve liberar a memória chamando o **método CoTaskMemFree.**</span><span class="sxs-lookup"><span data-stu-id="2cd56-121">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cd56-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2cd56-122">Return value</span></span>

<span data-ttu-id="2cd56-123">Se o método for bem-sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2cd56-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="2cd56-124">Se falhar, retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="2cd56-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cd56-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cd56-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2cd56-126">O header Fil \_ data.h está localizado no diretório [Exemplo do Mapeador](mapper-sample.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2cd56-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2cd56-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cd56-127">Requirements</span></span>



| <span data-ttu-id="2cd56-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cd56-128">Requirement</span></span> | <span data-ttu-id="2cd56-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2cd56-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd56-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2cd56-130">Header</span></span><br/> | <dl> <span data-ttu-id="2cd56-131"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd56-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="2cd56-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2cd56-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="2cd56-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cd56-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2cd56-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cd56-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cd56-135">**IAMFilterData Interface**</span><span class="sxs-lookup"><span data-stu-id="2cd56-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




