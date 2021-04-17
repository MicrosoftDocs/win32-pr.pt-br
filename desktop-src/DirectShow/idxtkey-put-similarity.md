---
description: O \_ método Put similaridade especifica o intervalo de dados de cor que se torna transparente. Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'IDxtKey: método de ut_Similarity de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812817"
---
# <a name="idxtkeyput_similarity-method"></a><span data-ttu-id="451bc-105">Método de similaridade IDxtKey::p UT \_</span><span class="sxs-lookup"><span data-stu-id="451bc-105">IDxtKey::put\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="451bc-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="451bc-106">\[Deprecated.</span></span> <span data-ttu-id="451bc-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="451bc-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="451bc-108">O `put_Similarity` método especifica o intervalo de dados de cor que se torna transparente.</span><span class="sxs-lookup"><span data-stu-id="451bc-108">The `put_Similarity` method specifies the range of color data that becomes transparent.</span></span> <span data-ttu-id="451bc-109">Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente.</span><span class="sxs-lookup"><span data-stu-id="451bc-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="451bc-110">Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="451bc-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="451bc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="451bc-111">Syntax</span></span>


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="451bc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="451bc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="451bc-113">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="451bc-113">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="451bc-114">Especifica o valor de similaridade.</span><span class="sxs-lookup"><span data-stu-id="451bc-114">Specifies the similarity value.</span></span> <span data-ttu-id="451bc-115">O intervalo válido é de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="451bc-115">The valid range is from 0 to 100.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="451bc-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="451bc-116">Return value</span></span>

<span data-ttu-id="451bc-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="451bc-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="451bc-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="451bc-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="451bc-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="451bc-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="451bc-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="451bc-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="451bc-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="451bc-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="451bc-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="451bc-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="451bc-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="451bc-123">Requirements</span></span>



| <span data-ttu-id="451bc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="451bc-124">Requirement</span></span> | <span data-ttu-id="451bc-125">Valor</span><span class="sxs-lookup"><span data-stu-id="451bc-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="451bc-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="451bc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="451bc-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="451bc-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="451bc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="451bc-128">Library</span></span><br/> | <dl> <span data-ttu-id="451bc-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="451bc-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="451bc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="451bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="451bc-131">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="451bc-131">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="451bc-132">**IDxtKey::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="451bc-132">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




