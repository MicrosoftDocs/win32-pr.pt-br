---
description: O \_ método Put RGB especifica a cor RGB para a chave. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: 'IDxtKey: método de ut_RGB de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0b7d282ceb4a693d5a390b8df9b935f0e415d150
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759117"
---
# <a name="idxtkeyput_rgb-method"></a><span data-ttu-id="be459-104">Método IDxtKey::p UT \_ RGB</span><span class="sxs-lookup"><span data-stu-id="be459-104">IDxtKey::put\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="be459-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="be459-105">\[Deprecated.</span></span> <span data-ttu-id="be459-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be459-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="be459-107">O `put_RGB` método especifica a cor RGB para a chave.</span><span class="sxs-lookup"><span data-stu-id="be459-107">The `put_RGB` method specifies the RGB color on which to key.</span></span> <span data-ttu-id="be459-108">Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="be459-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="be459-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be459-109">Syntax</span></span>


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a><span data-ttu-id="be459-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be459-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be459-111">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be459-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be459-112">Especifica a cor como um número hexadecimal com o formato 0xRRGGBB, em que RR é o valor vermelho, GG é o valor verde e BB é o valor azul.</span><span class="sxs-lookup"><span data-stu-id="be459-112">Specifies the color as a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be459-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be459-113">Return value</span></span>

<span data-ttu-id="be459-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="be459-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="be459-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="be459-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="be459-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="be459-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="be459-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="be459-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="be459-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="be459-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="be459-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="be459-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="be459-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be459-120">Requirements</span></span>



| <span data-ttu-id="be459-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="be459-121">Requirement</span></span> | <span data-ttu-id="be459-122">Valor</span><span class="sxs-lookup"><span data-stu-id="be459-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be459-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be459-123">Header</span></span><br/>  | <dl> <span data-ttu-id="be459-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="be459-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="be459-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be459-125">Library</span></span><br/> | <dl> <span data-ttu-id="be459-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be459-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be459-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="be459-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be459-128">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="be459-128">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="be459-129">**IDxtKey::p UT \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="be459-129">**IDxtKey::put\_KeyType**</span></span>](idxtkey-put-keytype.md)
</dt> </dl>

 

 




