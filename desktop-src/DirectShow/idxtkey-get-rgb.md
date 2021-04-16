---
description: O \_ método Get RGB recupera a cor RGB para a chave. Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: 'Método IDxtKey:: get_RGB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ef521b28c232f8247ef38858931ae56be6bf2d25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779527"
---
# <a name="idxtkeyget_rgb-method"></a><span data-ttu-id="cfa8e-104">Método IDxtKey:: get \_ RGB</span><span class="sxs-lookup"><span data-stu-id="cfa8e-104">IDxtKey::get\_RGB method</span></span>

> [!Note]  
> <span data-ttu-id="cfa8e-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-105">\[Deprecated.</span></span> <span data-ttu-id="cfa8e-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cfa8e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cfa8e-107">O `get_RGB` método recupera a cor RGB para a chave.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-107">The `get_RGB` method retrieves the RGB color on which to key.</span></span> <span data-ttu-id="cfa8e-108">Essa propriedade só se aplica quando o tipo de chave é DXTKEY \_ RGB.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-108">This property applies only when the key type is DXTKEY\_RGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa8e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfa8e-109">Syntax</span></span>


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="cfa8e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfa8e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfa8e-111">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cfa8e-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cfa8e-112">Recebe a cor.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-112">Receives the color.</span></span> <span data-ttu-id="cfa8e-113">O valor retornado é um número hexadecimal com o formato 0xRRGGBB, em que RR é o valor vermelho, GG é o valor verde e BB é o valor azul.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-113">The returned value is a hexadecimal number with the format 0xRRGGBB, where RR is the red value, GG is the green value, and BB is the blue value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfa8e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfa8e-114">Return value</span></span>

<span data-ttu-id="cfa8e-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cfa8e-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cfa8e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa8e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfa8e-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfa8e-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cfa8e-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="cfa8e-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cfa8e-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="cfa8e-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfa8e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfa8e-121">Requirements</span></span>



| <span data-ttu-id="cfa8e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfa8e-122">Requirement</span></span> | <span data-ttu-id="cfa8e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="cfa8e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa8e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfa8e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="cfa8e-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfa8e-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cfa8e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfa8e-126">Library</span></span><br/> | <dl> <span data-ttu-id="cfa8e-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfa8e-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa8e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfa8e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa8e-129">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="cfa8e-129">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> <dt>

[<span data-ttu-id="cfa8e-130">**IDxtKey:: obter \_ KeyType**</span><span class="sxs-lookup"><span data-stu-id="cfa8e-130">**IDxtKey::get\_KeyType**</span></span>](idxtkey-get-keytype.md)
</dt> </dl>

 

 




