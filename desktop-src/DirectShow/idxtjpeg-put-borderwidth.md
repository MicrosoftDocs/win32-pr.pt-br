---
description: O método de Put \_ BorderWidth especifica a largura da borda sólida ao longo das bordas do padrão de apagamento.
ms.assetid: a618926a-efa4-47a2-9ce9-ae298ed41083
title: 'IDxtJpeg: método de ut_BorderWidth de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df7435b8a516b818b6d7c86e907ba75cce86f6c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759119"
---
# <a name="idxtjpegput_borderwidth-method"></a><span data-ttu-id="1655d-103">Método IDxtJpeg::p UT \_ BorderWidth</span><span class="sxs-lookup"><span data-stu-id="1655d-103">IDxtJpeg::put\_BorderWidth method</span></span>

> [!Note]  
> <span data-ttu-id="1655d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1655d-104">\[Deprecated.</span></span> <span data-ttu-id="1655d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1655d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1655d-106">O `put_BorderWidth` método especifica a largura da borda sólida ao longo das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="1655d-106">The `put_BorderWidth` method specifies the width of the solid border along the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="1655d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1655d-107">Syntax</span></span>


```C++
HRESULT put_BorderWidth(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="1655d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1655d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1655d-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1655d-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1655d-110">A largura da borda, em pixels.</span><span class="sxs-lookup"><span data-stu-id="1655d-110">The width of the border, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1655d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1655d-111">Return value</span></span>

<span data-ttu-id="1655d-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1655d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1655d-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1655d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1655d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1655d-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1655d-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1655d-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1655d-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1655d-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1655d-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1655d-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1655d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1655d-118">Requirements</span></span>



| <span data-ttu-id="1655d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1655d-119">Requirement</span></span> | <span data-ttu-id="1655d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1655d-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1655d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1655d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1655d-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1655d-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1655d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1655d-123">Library</span></span><br/> | <dl> <span data-ttu-id="1655d-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1655d-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1655d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1655d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1655d-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="1655d-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




