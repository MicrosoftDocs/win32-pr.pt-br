---
description: O método Put log de erros \_ especifica um registro de erro para o objeto.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: 'IAMSetErrorLog: método de ut_ErrorLog de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757685"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="31188-103">Método IAMSetErrorLog::p UT log de \_ erros</span><span class="sxs-lookup"><span data-stu-id="31188-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="31188-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="31188-104">\[Deprecated.</span></span> <span data-ttu-id="31188-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="31188-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="31188-106">O `put_ErrorLog` método especifica um log de erros para o objeto.</span><span class="sxs-lookup"><span data-stu-id="31188-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="31188-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31188-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="31188-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31188-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31188-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31188-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31188-110">Ponteiro para a interface [**IAMErrorLog**](iamerrorlog.md) do log de erros.</span><span class="sxs-lookup"><span data-stu-id="31188-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31188-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31188-111">Return value</span></span>

<span data-ttu-id="31188-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="31188-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31188-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31188-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="31188-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="31188-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="31188-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="31188-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="31188-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="31188-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="31188-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="31188-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="31188-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31188-118">Requirements</span></span>



| <span data-ttu-id="31188-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="31188-119">Requirement</span></span> | <span data-ttu-id="31188-120">Valor</span><span class="sxs-lookup"><span data-stu-id="31188-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31188-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31188-121">Header</span></span><br/>  | <dl> <span data-ttu-id="31188-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="31188-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="31188-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31188-123">Library</span></span><br/> | <dl> <span data-ttu-id="31188-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31188-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31188-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="31188-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31188-126">**Interface IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="31188-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="31188-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="31188-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




