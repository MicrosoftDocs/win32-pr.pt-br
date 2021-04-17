---
description: O método getmedianame recupera o nome do arquivo de origem representado por esse objeto de origem.
ms.assetid: 6f468628-10e1-4746-9c3a-6dae9aa3f6ad
title: 'Método IAMTimelineSrc:: getmedianame (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3727d57371e5c7bab4f9d693a247b6b62a3ada17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789942"
---
# <a name="iamtimelinesrcgetmedianame-method"></a><span data-ttu-id="102d5-103">Método IAMTimelineSrc:: getmedianame</span><span class="sxs-lookup"><span data-stu-id="102d5-103">IAMTimelineSrc::GetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="102d5-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="102d5-104">\[Deprecated.</span></span> <span data-ttu-id="102d5-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="102d5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="102d5-106">O `GetMediaName` método recupera o nome do arquivo de origem representado por esse objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="102d5-106">The `GetMediaName` method retrieves the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="102d5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="102d5-107">Syntax</span></span>


```C++
HRESULT GetMediaName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="102d5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="102d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102d5-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="102d5-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="102d5-110">Recebe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="102d5-110">Receives the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102d5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="102d5-111">Return value</span></span>

<span data-ttu-id="102d5-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="102d5-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="102d5-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="102d5-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="102d5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="102d5-114">Remarks</span></span>

<span data-ttu-id="102d5-115">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="102d5-115">The method allocates memory for the string.</span></span> <span data-ttu-id="102d5-116">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="102d5-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="102d5-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="102d5-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="102d5-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="102d5-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="102d5-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="102d5-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="102d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="102d5-120">Requirements</span></span>



| <span data-ttu-id="102d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="102d5-121">Requirement</span></span> | <span data-ttu-id="102d5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="102d5-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="102d5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="102d5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="102d5-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="102d5-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="102d5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="102d5-125">Library</span></span><br/> | <dl> <span data-ttu-id="102d5-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="102d5-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102d5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="102d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102d5-128">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="102d5-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="102d5-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="102d5-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




