---
title: Método IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: O método EncryptScatter desembaralha e criptografa os dados.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Formato de mídia do Windows do método EncryptScatter
- Método EncryptScatter Windows Media Format, interface IWMDRMEncryptScatter
- Formato de mídia do Windows de interface IWMDRMEncryptScatter, método EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762808"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="6cd3a-106">Método IWMDRMEncryptScatter:: EncryptScatter</span><span class="sxs-lookup"><span data-stu-id="6cd3a-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="6cd3a-107">O método **EncryptScatter** desembaralha e criptografa os dados.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd3a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cd3a-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="6cd3a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cd3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd3a-110">*cBlocks* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cd3a-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3a-111">Número de elementos na matriz *rgBlocks* .</span><span class="sxs-lookup"><span data-stu-id="6cd3a-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="6cd3a-112">*rgBlocks* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cd3a-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3a-113">Matriz de uma ou mais estruturas de [**\_ \_ \_ bloco de dispersão criptografadas WMDRM**](wmdrm-encrypt-scatter-block.md) .</span><span class="sxs-lookup"><span data-stu-id="6cd3a-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="6cd3a-114">Cada elemento descreve um bloco de dados para serem codificados e criptografados.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="6cd3a-115">*pWMCryptoData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cd3a-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3a-116">Ponteiro para uma estrutura [**WMDRMCryptoData**](wmdrmcryptodata.md) que contém parâmetros de criptografia.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="6cd3a-117">Defina como **nulo** para usar os parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="6cd3a-118">*cbOutput* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6cd3a-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3a-119">Tamanho do buffer de dados de saída passado como *pbOutput*.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="6cd3a-120">*pbOutput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6cd3a-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd3a-121">Buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd3a-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6cd3a-122">Return value</span></span>

<span data-ttu-id="6cd3a-123">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6cd3a-124">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6cd3a-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6cd3a-125">Return code</span></span>                                                                          | <span data-ttu-id="6cd3a-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cd3a-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6cd3a-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cd3a-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6cd3a-128">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6cd3a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cd3a-129">Remarks</span></span>

<span data-ttu-id="6cd3a-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6cd3a-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd3a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cd3a-131">Requirements</span></span>



| <span data-ttu-id="6cd3a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cd3a-132">Requirement</span></span> | <span data-ttu-id="6cd3a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6cd3a-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd3a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cd3a-134">Header</span></span><br/> | <dl> <span data-ttu-id="6cd3a-135"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cd3a-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cd3a-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cd3a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd3a-137">**InitEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="6cd3a-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="6cd3a-138">**Interface IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="6cd3a-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





