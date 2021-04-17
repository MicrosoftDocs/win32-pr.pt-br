---
description: Observe que essa interface foi preterida.
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
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766309"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="b5313-103">Método IAMFilterData:: CreateFilterData</span><span class="sxs-lookup"><span data-stu-id="b5313-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="b5313-104">Essa interface foi substituída.</span><span class="sxs-lookup"><span data-stu-id="b5313-104">This interface has been deprecated.</span></span> <span data-ttu-id="b5313-105">Novos aplicativos não devem usá-lo.</span><span class="sxs-lookup"><span data-stu-id="b5313-105">New applications should not use it.</span></span>

 

<span data-ttu-id="b5313-106">O `CreateFilterData` método cria dados de registro binários para um filtro.</span><span class="sxs-lookup"><span data-stu-id="b5313-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="b5313-107">Esses dados podem ser gravados no registro como uma \_ subchave binária reg chamada FilterData, na chave CLSID do filtro.</span><span class="sxs-lookup"><span data-stu-id="b5313-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="b5313-108">Normalmente, não há motivo para um aplicativo chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="b5313-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="b5313-109">O método [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) cria automaticamente os dados binários e os adiciona ao local correto no registro.</span><span class="sxs-lookup"><span data-stu-id="b5313-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="b5313-110">Para obter mais informações, consulte [como registrar filtros do DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b5313-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5313-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5313-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="b5313-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5313-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5313-113">*prf2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5313-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5313-114">Ponteiro para uma estrutura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) que contém as informações de filtro.</span><span class="sxs-lookup"><span data-stu-id="b5313-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="b5313-115">*prgbFilterData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5313-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5313-116">Endereço de uma variável que recebe um ponteiro para os dados binários.</span><span class="sxs-lookup"><span data-stu-id="b5313-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="b5313-117">O método aloca a memória para os dados.</span><span class="sxs-lookup"><span data-stu-id="b5313-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="b5313-118">O chamador deve liberar a memória chamando o método **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="b5313-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="b5313-119">*PCB* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5313-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5313-120">Ponteiro para uma variável que recebe o tamanho dos dados binários, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b5313-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5313-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5313-121">Return value</span></span>

<span data-ttu-id="b5313-122">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5313-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b5313-123">Se falhar, retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="b5313-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5313-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5313-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5313-125">O cabeçalho Fil \_ Data. h está localizado no diretório de [exemplo do mapeador](mapper-sample.md) no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="b5313-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5313-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5313-126">Requirements</span></span>



| <span data-ttu-id="b5313-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5313-127">Requirement</span></span> | <span data-ttu-id="b5313-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b5313-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5313-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5313-129">Header</span></span><br/> | <dl> <span data-ttu-id="b5313-130"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5313-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="b5313-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b5313-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="b5313-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5313-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b5313-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5313-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5313-134">**Interface IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="b5313-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 




