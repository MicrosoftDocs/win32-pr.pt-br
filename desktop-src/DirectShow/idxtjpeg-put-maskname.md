---
description: O \_ método Put mascaraname especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento.
ms.assetid: f2b93c1e-479e-46c1-afe3-25b0ef720ab3
title: 'IDxtJpeg: método de ut_MaskName de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f74fe09572b95ff1508021b3fa2ae4f9888f2d5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757675"
---
# <a name="idxtjpegput_maskname-method"></a><span data-ttu-id="af856-103">Método IDxtJpeg::p UT \_ maskname</span><span class="sxs-lookup"><span data-stu-id="af856-103">IDxtJpeg::put\_MaskName method</span></span>

> [!Note]  
> <span data-ttu-id="af856-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="af856-104">\[Deprecated.</span></span> <span data-ttu-id="af856-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af856-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="af856-106">O `put_MaskName` método especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento.</span><span class="sxs-lookup"><span data-stu-id="af856-106">The `put_MaskName` method specifies the name of a JPEG file to use as the wipe mask.</span></span> <span data-ttu-id="af856-107">Essa máscara será usada em vez de uma das máscaras de apagamento internas.</span><span class="sxs-lookup"><span data-stu-id="af856-107">This mask will be used instead of one of the built-in wipe masks.</span></span> <span data-ttu-id="af856-108">O arquivo deve conter um gradiente monocromático de 8 bits por pixel.</span><span class="sxs-lookup"><span data-stu-id="af856-108">The file must contain a monochrome, 8-bits-per-pixel gradient.</span></span> <span data-ttu-id="af856-109">O gradiente é usado como uma máscara para definir a progressão do apagamento.</span><span class="sxs-lookup"><span data-stu-id="af856-109">The gradient is used as a mask to define the wipe's progression.</span></span>

## <a name="syntax"></a><span data-ttu-id="af856-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af856-110">Syntax</span></span>


```C++
HRESULT put_MaskName(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="af856-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af856-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af856-112">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="af856-112">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af856-113">Especifica o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="af856-113">Specifies the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af856-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af856-114">Return value</span></span>

<span data-ttu-id="af856-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="af856-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="af856-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="af856-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="af856-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="af856-117">Remarks</span></span>

<span data-ttu-id="af856-118">Para reverter para uma máscara interna, defina a propriedade **MaskNum** .</span><span class="sxs-lookup"><span data-stu-id="af856-118">To revert to a built-in mask, set the **MaskNum** property.</span></span>

> [!Note]  
> <span data-ttu-id="af856-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="af856-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="af856-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="af856-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="af856-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="af856-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af856-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af856-122">Requirements</span></span>



| <span data-ttu-id="af856-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="af856-123">Requirement</span></span> | <span data-ttu-id="af856-124">Valor</span><span class="sxs-lookup"><span data-stu-id="af856-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af856-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af856-125">Header</span></span><br/>  | <dl> <span data-ttu-id="af856-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="af856-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="af856-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af856-127">Library</span></span><br/> | <dl> <span data-ttu-id="af856-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af856-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af856-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="af856-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af856-130">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="af856-130">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> <dt>

[<span data-ttu-id="af856-131">**IDxtJpeg::p UT \_ MaskNum**</span><span class="sxs-lookup"><span data-stu-id="af856-131">**IDxtJpeg::put\_MaskNum**</span></span>](idxtjpeg-put-masknum.md)
</dt> </dl>

 

 




