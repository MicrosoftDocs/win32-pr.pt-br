---
description: 'O método GetSubObjectGUIDB recupera o GUID do subobjeto associado a este objeto Timeline. Esse método é equivalente a IAMTimelineObj:: GetSubObjectGUID, mas recebe um valor BSTR.'
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'Método IAMTimelineObj:: GetSubObjectGUIDB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758681"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="f5ffa-104">Método IAMTimelineObj:: GetSubObjectGUIDB</span><span class="sxs-lookup"><span data-stu-id="f5ffa-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="f5ffa-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-105">\[Deprecated.</span></span> <span data-ttu-id="f5ffa-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5ffa-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5ffa-107">O `GetSubObjectGUIDB` método recupera o GUID do subobjeto associado a este objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="f5ffa-108">Esse método é equivalente a [**IAMTimelineObj:: GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), mas recebe um valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="f5ffa-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ffa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5ffa-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="f5ffa-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5ffa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ffa-111">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f5ffa-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f5ffa-112">Recebe uma cadeia de caracteres que representa o GUID do subobjeto.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ffa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5ffa-113">Return value</span></span>

<span data-ttu-id="f5ffa-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5ffa-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5ffa-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5ffa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5ffa-116">Remarks</span></span>

<span data-ttu-id="f5ffa-117">O método aloca memória para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-117">The method allocates memory for the string.</span></span> <span data-ttu-id="f5ffa-118">O aplicativo deve chamar **SysFreeString** para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="f5ffa-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5ffa-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5ffa-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5ffa-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5ffa-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5ffa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ffa-122">Requirements</span></span>



| <span data-ttu-id="f5ffa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ffa-123">Requirement</span></span> | <span data-ttu-id="f5ffa-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ffa-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ffa-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5ffa-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f5ffa-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ffa-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5ffa-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5ffa-127">Library</span></span><br/> | <dl> <span data-ttu-id="f5ffa-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5ffa-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ffa-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5ffa-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ffa-130">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="f5ffa-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="f5ffa-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f5ffa-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




