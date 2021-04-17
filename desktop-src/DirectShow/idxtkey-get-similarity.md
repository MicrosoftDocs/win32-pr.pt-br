---
description: O \_ método obter similaridade recupera o intervalo de dados de cor que se torna transparente. Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Método IDxtKey:: get_Similarity (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754244"
---
# <a name="idxtkeyget_similarity-method"></a><span data-ttu-id="5275a-105">Método de similaridade IDxtKey:: get \_</span><span class="sxs-lookup"><span data-stu-id="5275a-105">IDxtKey::get\_Similarity method</span></span>

> [!Note]  
> <span data-ttu-id="5275a-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5275a-106">\[Deprecated.</span></span> <span data-ttu-id="5275a-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5275a-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5275a-108">O `get_Similarity` método recupera o intervalo de dados de cor que se torna transparente.</span><span class="sxs-lookup"><span data-stu-id="5275a-108">The `get_Similarity` method retrieves the range of color data that becomes transparent.</span></span> <span data-ttu-id="5275a-109">Em valores mais altos, um intervalo mais amplo de cores semelhantes é transparente.</span><span class="sxs-lookup"><span data-stu-id="5275a-109">At higher values, a wider range of similar colors is transparent.</span></span> <span data-ttu-id="5275a-110">Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB ou DXTKEY \_ NONRED.</span><span class="sxs-lookup"><span data-stu-id="5275a-110">This property applies only when the key type is DXTKEY\_RGB or DXTKEY\_NONRED.</span></span>

## <a name="syntax"></a><span data-ttu-id="5275a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5275a-111">Syntax</span></span>


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5275a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5275a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5275a-113">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5275a-113">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5275a-114">Recebe o valor de similaridade.</span><span class="sxs-lookup"><span data-stu-id="5275a-114">Receives the similarity value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5275a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5275a-115">Return value</span></span>

<span data-ttu-id="5275a-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5275a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5275a-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5275a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5275a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5275a-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5275a-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5275a-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5275a-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5275a-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5275a-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5275a-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5275a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5275a-122">Requirements</span></span>



| <span data-ttu-id="5275a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5275a-123">Requirement</span></span> | <span data-ttu-id="5275a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5275a-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5275a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5275a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5275a-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5275a-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5275a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5275a-127">Library</span></span><br/> | <dl> <span data-ttu-id="5275a-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5275a-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5275a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5275a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5275a-130">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="5275a-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="5275a-131">**IDxtKey:: obter \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="5275a-131">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




