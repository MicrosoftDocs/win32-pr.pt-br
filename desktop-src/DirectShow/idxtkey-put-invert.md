---
description: O \_ método Put Invert especifica se a operação de chave é invertida. Essa propriedade se aplica a todos os tipos de chave, exceto DXTKEY \_ alfa.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: 'IDxtKey: método de ut_Invert de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3e4b807770d0eeb985c982b61b8390695cc42327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812818"
---
# <a name="idxtkeyput_invert-method"></a><span data-ttu-id="420db-104">Método IDxtKey::p UT \_ inverter</span><span class="sxs-lookup"><span data-stu-id="420db-104">IDxtKey::put\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="420db-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="420db-105">\[Deprecated.</span></span> <span data-ttu-id="420db-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="420db-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="420db-107">O `put_Invert` método especifica se a operação de chave é invertida.</span><span class="sxs-lookup"><span data-stu-id="420db-107">The `put_Invert` method specifies whether the key operation is inverted.</span></span> <span data-ttu-id="420db-108">Essa propriedade se aplica a todos os tipos de chave, exceto DXTKEY \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="420db-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="420db-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="420db-109">Syntax</span></span>


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="420db-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="420db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="420db-111">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="420db-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="420db-112">Especifica um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="420db-112">Specifies a Boolean value.</span></span> <span data-ttu-id="420db-113">Se **for true**, os pixels na imagem subjacente serão invertidos em relação à operação padrão.</span><span class="sxs-lookup"><span data-stu-id="420db-113">If **TRUE**, pixels in the overlying image are inverted with respect to the default operation.</span></span> <span data-ttu-id="420db-114">Se **for false**, os pixels na imagem subjacente serão tornados transparentes da maneira padrão.</span><span class="sxs-lookup"><span data-stu-id="420db-114">If **FALSE**, pixels in the overlying image are made transparent in the default manner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="420db-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="420db-115">Return value</span></span>

<span data-ttu-id="420db-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="420db-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="420db-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="420db-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="420db-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="420db-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="420db-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="420db-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="420db-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="420db-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="420db-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="420db-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="420db-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="420db-122">Requirements</span></span>



| <span data-ttu-id="420db-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="420db-123">Requirement</span></span> | <span data-ttu-id="420db-124">Valor</span><span class="sxs-lookup"><span data-stu-id="420db-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="420db-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="420db-125">Header</span></span><br/>  | <dl> <span data-ttu-id="420db-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="420db-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="420db-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="420db-127">Library</span></span><br/> | <dl> <span data-ttu-id="420db-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="420db-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="420db-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="420db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="420db-130">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="420db-130">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="420db-131">**IDxtKey::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="420db-131">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




