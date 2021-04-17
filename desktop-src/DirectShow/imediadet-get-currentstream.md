---
description: O \_ método Get CurrentStream recupera o número de fluxo usado atualmente pelo detector de mídia.
ms.assetid: 0f590498-e639-4b6b-be1d-f1e4a36282cb
title: 'Método IMediaDet:: get_CurrentStream (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e664e88862a6bc124a88ac23cedf29e687d51e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766265"
---
# <a name="imediadetget_currentstream-method"></a><span data-ttu-id="52923-103">Método IMediaDet:: get \_ CurrentStream</span><span class="sxs-lookup"><span data-stu-id="52923-103">IMediaDet::get\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="52923-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="52923-104">\[Deprecated.</span></span> <span data-ttu-id="52923-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="52923-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="52923-106">O `get_CurrentStream` método recupera o número de fluxo usado atualmente pelo detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="52923-106">The `get_CurrentStream` method retrieves the stream number currently used by the media detector.</span></span>

## <a name="syntax"></a><span data-ttu-id="52923-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52923-107">Syntax</span></span>


```C++
HRESULT get_CurrentStream(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="52923-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52923-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52923-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="52923-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="52923-110">Recebe o número do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="52923-110">Receives the current stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52923-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52923-111">Return value</span></span>

<span data-ttu-id="52923-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="52923-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="52923-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="52923-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="52923-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="52923-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="52923-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="52923-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="52923-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="52923-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="52923-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="52923-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52923-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52923-118">Requirements</span></span>



| <span data-ttu-id="52923-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52923-119">Requirement</span></span> | <span data-ttu-id="52923-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52923-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52923-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52923-121">Header</span></span><br/>  | <dl> <span data-ttu-id="52923-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="52923-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="52923-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52923-123">Library</span></span><br/> | <dl> <span data-ttu-id="52923-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52923-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52923-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="52923-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52923-126">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="52923-126">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="52923-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="52923-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




