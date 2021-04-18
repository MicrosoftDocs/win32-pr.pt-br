---
description: O \_ método Get filename recupera o nome do arquivo de origem usado atualmente pelo detector de mídia.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'Método IMediaDet:: get_Filename (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759538"
---
# <a name="imediadetget_filename-method"></a><span data-ttu-id="67b27-103">Método de nome de arquivo IMediaDet:: get \_</span><span class="sxs-lookup"><span data-stu-id="67b27-103">IMediaDet::get\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="67b27-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="67b27-104">\[Deprecated.</span></span> <span data-ttu-id="67b27-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="67b27-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="67b27-106">O `get_Filename` método recupera o nome do arquivo de origem atualmente usado pelo detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="67b27-106">The `get_Filename` method retrieves the name of the source file currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b27-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67b27-107">Syntax</span></span>


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="67b27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67b27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b27-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="67b27-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="67b27-110">Recebe o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="67b27-110">Receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b27-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="67b27-111">Return value</span></span>

<span data-ttu-id="67b27-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67b27-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67b27-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67b27-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67b27-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="67b27-114">Remarks</span></span>

<span data-ttu-id="67b27-115">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="67b27-115">The method allocates memory for the string.</span></span> <span data-ttu-id="67b27-116">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="67b27-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="67b27-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="67b27-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="67b27-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="67b27-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="67b27-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="67b27-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67b27-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67b27-120">Requirements</span></span>



| <span data-ttu-id="67b27-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="67b27-121">Requirement</span></span> | <span data-ttu-id="67b27-122">Valor</span><span class="sxs-lookup"><span data-stu-id="67b27-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67b27-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="67b27-123">Header</span></span><br/>  | <dl> <span data-ttu-id="67b27-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="67b27-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="67b27-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="67b27-125">Library</span></span><br/> | <dl> <span data-ttu-id="67b27-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67b27-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67b27-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="67b27-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b27-128">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="67b27-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="67b27-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="67b27-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




