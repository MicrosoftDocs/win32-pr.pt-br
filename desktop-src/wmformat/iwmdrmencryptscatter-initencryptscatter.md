---
title: Método IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: O método InitEncryptScatter Inicializa a interface IWMDRMEncryptScatter para uso.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Formato de mídia do Windows do método InitEncryptScatter
- Método InitEncryptScatter Windows Media Format, interface IWMDRMEncryptScatter
- Formato de mídia do Windows de interface IWMDRMEncryptScatter, método InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753624"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="0dc5d-106">Método IWMDRMEncryptScatter:: InitEncryptScatter</span><span class="sxs-lookup"><span data-stu-id="0dc5d-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="0dc5d-107">O método **InitEncryptScatter** Inicializa a interface **IWMDRMEncryptScatter** para uso.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc5d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0dc5d-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="0dc5d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0dc5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc5d-110">*cStreams* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dc5d-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc5d-111">Número de elementos na matriz *rgInfos* .</span><span class="sxs-lookup"><span data-stu-id="0dc5d-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="0dc5d-112">Esse também é o número de fluxos incluídos nos dados a serem criptografados.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="0dc5d-113">*rgInfos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0dc5d-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc5d-114">Matriz de uma ou mais estruturas de [**\_ \_ \_ informações de dispersão de WMDRM Encrypt**](wmdrm-encrypt-scatter-info.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc5d-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="0dc5d-115">Cada elemento contém informações de criptografia para um fluxo.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="0dc5d-116">O número de elementos nesta matriz deve ser igual ao valor de *cStreams*.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc5d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0dc5d-117">Return value</span></span>

<span data-ttu-id="0dc5d-118">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0dc5d-119">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0dc5d-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0dc5d-120">Return code</span></span>                                                                          | <span data-ttu-id="0dc5d-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dc5d-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0dc5d-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0dc5d-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0dc5d-123">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0dc5d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dc5d-124">Remarks</span></span>

<span data-ttu-id="0dc5d-125">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0dc5d-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc5d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc5d-126">Requirements</span></span>



| <span data-ttu-id="0dc5d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc5d-127">Requirement</span></span> | <span data-ttu-id="0dc5d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="0dc5d-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc5d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0dc5d-129">Header</span></span><br/> | <dl> <span data-ttu-id="0dc5d-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc5d-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dc5d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="0dc5d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc5d-132">**EncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="0dc5d-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="0dc5d-133">**Interface IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="0dc5d-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





