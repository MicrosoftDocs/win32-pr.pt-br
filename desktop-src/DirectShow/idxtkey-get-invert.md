---
description: O \_ método Get Invert recupera um valor booliano que indica se a operação de chave está invertida. Essa propriedade se aplica a todos os tipos de chave, exceto DXTKEY \_ alfa.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Método IDxtKey:: get_Invert (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51b95758adf6690f6d4fa479ac1cc2c585fa9352
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789680"
---
# <a name="idxtkeyget_invert-method"></a><span data-ttu-id="9283c-104">\_Método inverter IDxtKey:: Get</span><span class="sxs-lookup"><span data-stu-id="9283c-104">IDxtKey::get\_Invert method</span></span>

> [!Note]  
> <span data-ttu-id="9283c-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9283c-105">\[Deprecated.</span></span> <span data-ttu-id="9283c-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9283c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9283c-107">O `get_Invert` método recupera um valor booliano que indica se a operação de chave é invertida.</span><span class="sxs-lookup"><span data-stu-id="9283c-107">The `get_Invert` method retrieves a Boolean value indicating whether the key operation is inverted.</span></span> <span data-ttu-id="9283c-108">Essa propriedade se aplica a todos os tipos de chave, exceto DXTKEY \_ alfa.</span><span class="sxs-lookup"><span data-stu-id="9283c-108">This property applies to all key types except DXTKEY\_ALPHA.</span></span>

## <a name="syntax"></a><span data-ttu-id="9283c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9283c-109">Syntax</span></span>


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="9283c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9283c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9283c-111">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9283c-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9283c-112">Recebe um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9283c-112">Receives one of the following values.</span></span>



| <span data-ttu-id="9283c-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9283c-113">Value</span></span>     | <span data-ttu-id="9283c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9283c-114">Description</span></span>                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="9283c-115">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9283c-115">**TRUE**</span></span>  | <span data-ttu-id="9283c-116">Os pixels na imagem subjacente são invertidos em relação à operação padrão.</span><span class="sxs-lookup"><span data-stu-id="9283c-116">Pixels in the overlying image are inverted with respect to the default operation.</span></span> |
| <span data-ttu-id="9283c-117">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="9283c-117">**FALSE**</span></span> | <span data-ttu-id="9283c-118">Os pixels na imagem subjacente são tornados transparentes da maneira padrão.</span><span class="sxs-lookup"><span data-stu-id="9283c-118">Pixels in the overlying image are made transparent in the default manner.</span></span>         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9283c-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9283c-119">Return value</span></span>

<span data-ttu-id="9283c-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9283c-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9283c-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9283c-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9283c-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="9283c-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9283c-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9283c-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9283c-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9283c-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9283c-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9283c-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9283c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9283c-126">Requirements</span></span>



| <span data-ttu-id="9283c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9283c-127">Requirement</span></span> | <span data-ttu-id="9283c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9283c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9283c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9283c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9283c-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9283c-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9283c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9283c-131">Library</span></span><br/> | <dl> <span data-ttu-id="9283c-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9283c-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9283c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9283c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9283c-134">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="9283c-134">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="9283c-135">**IDxtKey:: obter \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="9283c-135">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




