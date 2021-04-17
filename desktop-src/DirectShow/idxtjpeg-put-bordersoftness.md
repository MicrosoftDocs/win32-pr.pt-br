---
description: O \_ método Put BorderSoftness especifica a largura da região borrada ao contrário das bordas do padrão de apagamento.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: 'IDxtJpeg: método de ut_BorderSoftness de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c72f59798ca84d01be79110cd4792da0a77f408
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759545"
---
# <a name="idxtjpegput_bordersoftness-method"></a><span data-ttu-id="530cd-103">IDxtJpeg: método UT \_ BorderSoftness:p</span><span class="sxs-lookup"><span data-stu-id="530cd-103">IDxtJpeg::put\_BorderSoftness method</span></span>

> [!Note]  
> <span data-ttu-id="530cd-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="530cd-104">\[Deprecated.</span></span> <span data-ttu-id="530cd-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="530cd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="530cd-106">O `put_BorderSoftness` método especifica a largura da região borrada ao contrário das bordas do padrão de apagamento.</span><span class="sxs-lookup"><span data-stu-id="530cd-106">The `put_BorderSoftness` method specifies the width of the blurry region around the edges of the wipe pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="530cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="530cd-107">Syntax</span></span>


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="530cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="530cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="530cd-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="530cd-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="530cd-110">A largura da região borrada, em pixels.</span><span class="sxs-lookup"><span data-stu-id="530cd-110">The width of the blurry region, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="530cd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="530cd-111">Return value</span></span>

<span data-ttu-id="530cd-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="530cd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="530cd-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="530cd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="530cd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="530cd-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="530cd-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="530cd-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="530cd-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="530cd-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="530cd-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="530cd-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="530cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="530cd-118">Requirements</span></span>



| <span data-ttu-id="530cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="530cd-119">Requirement</span></span> | <span data-ttu-id="530cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="530cd-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="530cd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="530cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="530cd-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="530cd-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="530cd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="530cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="530cd-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="530cd-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="530cd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="530cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="530cd-126">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="530cd-126">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




