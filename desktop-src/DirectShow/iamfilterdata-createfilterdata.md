---
description: 'Saiba mais sobre o método IAMFilterData:: CreateFilterData, que cria dados de registro binários para um filtro. Essa interface foi substituída.'
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Método IAMFilterData:: CreateFilterData (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989451"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="ad202-104">Método IAMFilterData:: CreateFilterData</span><span class="sxs-lookup"><span data-stu-id="ad202-104">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="ad202-105">Essa interface foi substituída.</span><span class="sxs-lookup"><span data-stu-id="ad202-105">This interface has been deprecated.</span></span> <span data-ttu-id="ad202-106">Novos aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="ad202-106">New applications should not use it.</span></span>

 

<span data-ttu-id="ad202-107">O `CreateFilterData` método cria dados de registro binários para um filtro.</span><span class="sxs-lookup"><span data-stu-id="ad202-107">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="ad202-108">Esses dados podem ser gravados no registro como uma \_ subchave binária reg chamada FilterData, na chave CLSID do filtro.</span><span class="sxs-lookup"><span data-stu-id="ad202-108">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="ad202-109">Normalmente, não há motivo para um aplicativo chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ad202-109">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="ad202-110">O método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) cria automaticamente os dados binários e os adiciona ao local correto no registro.</span><span class="sxs-lookup"><span data-stu-id="ad202-110">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="ad202-111">Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="ad202-111">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad202-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad202-112">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="ad202-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad202-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad202-114">*prf2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad202-114">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad202-115">Ponteiro para uma estrutura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contém as informações de filtro.</span><span class="sxs-lookup"><span data-stu-id="ad202-115">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="ad202-116">*prgbFilterData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad202-116">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad202-117">Endereço de uma variável que recebe um ponteiro para os dados binários.</span><span class="sxs-lookup"><span data-stu-id="ad202-117">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="ad202-118">O método aloca a memória para os dados.</span><span class="sxs-lookup"><span data-stu-id="ad202-118">The method allocates the memory for the data.</span></span> <span data-ttu-id="ad202-119">O chamador deve liberar a memória chamando o método **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="ad202-119">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="ad202-120">*PCB* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad202-120">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad202-121">Ponteiro para uma variável que recebe o tamanho dos dados binários, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ad202-121">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad202-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad202-122">Return value</span></span>

<span data-ttu-id="ad202-123">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad202-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="ad202-124">Se falhar, retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="ad202-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad202-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad202-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ad202-126">O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="ad202-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ad202-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad202-127">Requirements</span></span>



| <span data-ttu-id="ad202-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad202-128">Requirement</span></span> | <span data-ttu-id="ad202-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ad202-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad202-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad202-130">Header</span></span><br/> | <dl> <span data-ttu-id="ad202-131"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad202-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="ad202-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ad202-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="ad202-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad202-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ad202-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad202-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad202-135">**Interface IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="ad202-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




