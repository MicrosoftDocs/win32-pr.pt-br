---
description: O método getuserdata recupera os dados persistentes definidos pelo aplicativo.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'Método IAMTimelineObj:: getuserdata (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770070"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="ff7cd-103">Método IAMTimelineObj:: getuserdata</span><span class="sxs-lookup"><span data-stu-id="ff7cd-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="ff7cd-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-104">\[Deprecated.</span></span> <span data-ttu-id="ff7cd-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ff7cd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ff7cd-106">O `GetUserData` método recupera os dados persistentes definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff7cd-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="ff7cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff7cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff7cd-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="ff7cd-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7cd-110">Ponteiro para um buffer que recebe os dados.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="ff7cd-111">Para determinar o tamanho do buffer a ser alocado, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="ff7cd-112">O tamanho necessário é retornado em *psize*.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="ff7cd-113">*pSize*</span><span class="sxs-lookup"><span data-stu-id="ff7cd-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="ff7cd-114">Recebe o tamanho dos dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff7cd-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff7cd-115">Return value</span></span>

<span data-ttu-id="ff7cd-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff7cd-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff7cd-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff7cd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff7cd-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff7cd-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ff7cd-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ff7cd-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ff7cd-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ff7cd-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ff7cd-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff7cd-122">Requirements</span></span>



| <span data-ttu-id="ff7cd-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff7cd-123">Requirement</span></span> | <span data-ttu-id="ff7cd-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ff7cd-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff7cd-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff7cd-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ff7cd-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff7cd-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ff7cd-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff7cd-127">Library</span></span><br/> | <dl> <span data-ttu-id="ff7cd-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff7cd-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff7cd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff7cd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7cd-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="ff7cd-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="ff7cd-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ff7cd-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




