---
description: Recupera o PROPVARIANT e a cadeia de caracteres de entrada que representa um bloco de dados. Chamar esse método é o mesmo que chamar GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Método IRichChunk:: RemoteGetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090049"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="6a8d8-104">Método IRichChunk:: RemoteGetData</span><span class="sxs-lookup"><span data-stu-id="6a8d8-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="6a8d8-105">Recupera o [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) e a cadeia de caracteres de entrada que representa um bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="6a8d8-106">Chamar esse método é o mesmo que chamar [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span><span class="sxs-lookup"><span data-stu-id="6a8d8-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a8d8-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="6a8d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a8d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8d8-109">*pFirstPos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a8d8-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8d8-110">Recebe a posição inicial de base zero do intervalo.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="6a8d8-111">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a8d8-112">*PLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a8d8-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8d8-113">Recebe o comprimento do intervalo.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-113">Receives the length of the range.</span></span> <span data-ttu-id="6a8d8-114">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a8d8-115">*ppsz* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a8d8-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8d8-116">Recebe o valor de cadeia de caracteres Unicode associado ou **nulo** se não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="6a8d8-117">*valores* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6a8d8-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8d8-118">Recebe o valor [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associado ou **VT \_ vazio** se não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="6a8d8-119">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8d8-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a8d8-120">Return value</span></span>

<span data-ttu-id="6a8d8-121">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a8d8-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a8d8-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6a8d8-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a8d8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a8d8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8d8-124">**IRichChunk**</span><span class="sxs-lookup"><span data-stu-id="6a8d8-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
