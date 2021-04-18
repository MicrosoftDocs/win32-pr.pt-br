---
description: O método SetDefaultFPS define a taxa de quadros padrão do objeto de origem.
ms.assetid: ea93acde-3e05-43d5-8130-9ab2ee841b4e
title: 'Método IAMTimelineSrc:: SetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd15f0606b1a4e4ee1aacdb1b3f56d63a024708b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758679"
---
# <a name="iamtimelinesrcsetdefaultfps-method"></a><span data-ttu-id="e8ba8-103">Método IAMTimelineSrc:: SetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="e8ba8-103">IAMTimelineSrc::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="e8ba8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-104">\[Deprecated.</span></span> <span data-ttu-id="e8ba8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e8ba8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e8ba8-106">O `SetDefaultFPS` método define a taxa de quadros padrão do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-106">The `SetDefaultFPS` method sets the source object's default frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ba8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8ba8-107">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="e8ba8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8ba8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8ba8-109">*QUADROS*</span><span class="sxs-lookup"><span data-stu-id="e8ba8-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="e8ba8-110">Taxa de quadros padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-110">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8ba8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8ba8-111">Return value</span></span>

<span data-ttu-id="e8ba8-112">Retornará S \_ OK se for bem-sucedido, ou E \_ INVALIDARG se a taxa de quadros especificada for menor que zero.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-112">Returns S\_OK if successful, or E\_INVALIDARG if the specified frame rate is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ba8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8ba8-113">Remarks</span></span>

<span data-ttu-id="e8ba8-114">O mecanismo de renderização usa esse valor se ele não puder determinar a taxa de quadros do arquivo de origem original.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-114">The render engine uses this value if it cannot determine the frame rate from the original source file.</span></span>

<span data-ttu-id="e8ba8-115">Chame esse método somente para arquivos de origem sem uma taxa de quadros predefinida.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-115">Call this method only for source files without a predefined frame rate.</span></span> <span data-ttu-id="e8ba8-116">Para arquivos bitmap e JPEG, a taxa de quadros padrão é zero, o que faz com que a origem seja renderizada como uma imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-116">For bitmap and JPEG files, the default frame rate is zero, which causes the source to be rendered as a still image.</span></span> <span data-ttu-id="e8ba8-117">Para usar a imagem, como o primeiro quadro em uma sequência DIB, defina a taxa de quadros como um valor maior que zero.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-117">To use the image as the first frame in a DIB sequence set the frame rate to a value greater than zero.</span></span> <span data-ttu-id="e8ba8-118">Para obter mais informações, consulte [trabalhando com fontes](working-with-sources.md).</span><span class="sxs-lookup"><span data-stu-id="e8ba8-118">For more information, see [Working with Sources](working-with-sources.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8ba8-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e8ba8-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e8ba8-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e8ba8-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e8ba8-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e8ba8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8ba8-122">Requirements</span></span>



| <span data-ttu-id="e8ba8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ba8-123">Requirement</span></span> | <span data-ttu-id="e8ba8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="e8ba8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ba8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e8ba8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e8ba8-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ba8-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e8ba8-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8ba8-127">Library</span></span><br/> | <dl> <span data-ttu-id="e8ba8-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8ba8-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8ba8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8ba8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8ba8-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="e8ba8-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="e8ba8-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e8ba8-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




