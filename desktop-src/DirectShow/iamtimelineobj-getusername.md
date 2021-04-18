---
description: O método GetUserName recupera o nome definido pelo aplicativo do objeto.
ms.assetid: 7d172ec5-9cb7-4418-a628-a109944077a6
title: 'Método IAMTimelineObj:: GetUserName (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: efca014493cb5631e058927256bd1586aaca7ab7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785340"
---
# <a name="iamtimelineobjgetusername-method"></a><span data-ttu-id="4bb14-103">Método IAMTimelineObj:: GetUserName</span><span class="sxs-lookup"><span data-stu-id="4bb14-103">IAMTimelineObj::GetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="4bb14-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4bb14-104">\[Deprecated.</span></span> <span data-ttu-id="4bb14-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4bb14-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4bb14-106">O `GetUserName` método recupera o nome definido pelo aplicativo do objeto.</span><span class="sxs-lookup"><span data-stu-id="4bb14-106">The `GetUserName` method retrieves the object's application-defined name.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bb14-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4bb14-107">Syntax</span></span>


```C++
HRESULT GetUserName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4bb14-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4bb14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb14-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="4bb14-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb14-110">Recebe o nome do objeto como um **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="4bb14-110">Receives the name of the object as a **BSTR**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bb14-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-111">Return value</span></span>

<span data-ttu-id="4bb14-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4bb14-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bb14-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4bb14-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bb14-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4bb14-114">Remarks</span></span>

<span data-ttu-id="4bb14-115">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4bb14-115">The method allocates memory for the string.</span></span> <span data-ttu-id="4bb14-116">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="4bb14-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="4bb14-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4bb14-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4bb14-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4bb14-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4bb14-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4bb14-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4bb14-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bb14-120">Requirements</span></span>



| <span data-ttu-id="4bb14-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bb14-121">Requirement</span></span> | <span data-ttu-id="4bb14-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4bb14-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb14-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4bb14-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4bb14-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bb14-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4bb14-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4bb14-125">Library</span></span><br/> | <dl> <span data-ttu-id="4bb14-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4bb14-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb14-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4bb14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb14-128">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="4bb14-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4bb14-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="4bb14-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




