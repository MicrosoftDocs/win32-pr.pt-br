---
description: O \_ método Put matiz especifica o valor de matiz a ser chaveada. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ matiz.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: 'IDxtKey: método de ut_Hue de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9d2b08f3e805edc8b8860495fc105f0cfdf6768f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760742"
---
# <a name="idxtkeyput_hue-method"></a><span data-ttu-id="d75c6-104">Método IDxtKey::p UT \_ matiz</span><span class="sxs-lookup"><span data-stu-id="d75c6-104">IDxtKey::put\_Hue method</span></span>

> [!Note]  
> <span data-ttu-id="d75c6-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d75c6-105">\[Deprecated.</span></span> <span data-ttu-id="d75c6-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d75c6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d75c6-107">O `put_Hue` método especifica o valor de matiz a ser chaveada.</span><span class="sxs-lookup"><span data-stu-id="d75c6-107">The `put_Hue` method specifies the hue value on which to key.</span></span> <span data-ttu-id="d75c6-108">Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ matiz.</span><span class="sxs-lookup"><span data-stu-id="d75c6-108">This property applies only when the key type is DXTKEY\_HUE.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75c6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d75c6-109">Syntax</span></span>


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d75c6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d75c6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75c6-111">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d75c6-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75c6-112">O valor de matiz para o qual fazer a chave.</span><span class="sxs-lookup"><span data-stu-id="d75c6-112">The hue value on which to key.</span></span> <span data-ttu-id="d75c6-113">O intervalo válido é de 0 a 360.</span><span class="sxs-lookup"><span data-stu-id="d75c6-113">The valid range is from 0 to 360.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75c6-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d75c6-114">Return value</span></span>

<span data-ttu-id="d75c6-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d75c6-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d75c6-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d75c6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d75c6-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d75c6-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d75c6-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d75c6-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d75c6-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d75c6-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d75c6-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d75c6-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d75c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d75c6-121">Requirements</span></span>



| <span data-ttu-id="d75c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75c6-122">Requirement</span></span> | <span data-ttu-id="d75c6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d75c6-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d75c6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d75c6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d75c6-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d75c6-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d75c6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d75c6-126">Library</span></span><br/> | <dl> <span data-ttu-id="d75c6-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d75c6-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75c6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d75c6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75c6-129">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="d75c6-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="d75c6-130">**IDxtKey::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="d75c6-130">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




