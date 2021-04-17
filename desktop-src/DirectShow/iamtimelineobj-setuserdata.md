---
description: O método SetUserData define dados persistentes definidos pelo aplicativo.
ms.assetid: 195d8e92-a25c-40ff-8cc7-c1f05bdd76ab
title: 'Método IAMTimelineObj:: SetUserData (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7e09aafd614234827a704d8b9997f27981eb7c45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759547"
---
# <a name="iamtimelineobjsetuserdata-method"></a><span data-ttu-id="1a27b-103">Método IAMTimelineObj:: SetUserData</span><span class="sxs-lookup"><span data-stu-id="1a27b-103">IAMTimelineObj::SetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="1a27b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1a27b-104">\[Deprecated.</span></span> <span data-ttu-id="1a27b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a27b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a27b-106">O `SetUserData` método define dados persistentes definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a27b-106">The `SetUserData` method sets application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a27b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a27b-107">Syntax</span></span>


```C++
HRESULT SetUserData(
   BYTE *pData,
   long Size
);
```



## <a name="parameters"></a><span data-ttu-id="1a27b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a27b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a27b-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="1a27b-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="1a27b-110">Ponteiro para um buffer que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="1a27b-110">Pointer to a buffer containing the data.</span></span>

</dd> <dt>

<span data-ttu-id="1a27b-111">*Tamanho*</span><span class="sxs-lookup"><span data-stu-id="1a27b-111">*Size*</span></span> 
</dt> <dd>

<span data-ttu-id="1a27b-112">Tamanho dos dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="1a27b-112">Size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a27b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a27b-113">Return value</span></span>

<span data-ttu-id="1a27b-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a27b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a27b-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a27b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a27b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a27b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a27b-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1a27b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a27b-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a27b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a27b-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a27b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a27b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a27b-120">Requirements</span></span>



| <span data-ttu-id="1a27b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a27b-121">Requirement</span></span> | <span data-ttu-id="1a27b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1a27b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a27b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a27b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1a27b-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a27b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a27b-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a27b-125">Library</span></span><br/> | <dl> <span data-ttu-id="1a27b-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a27b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a27b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a27b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a27b-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="1a27b-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="1a27b-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1a27b-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




