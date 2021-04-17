---
description: O método Get Outlog \_ recupera o log de erros atual deste objeto.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Método IAMSetErrorLog:: get_ErrorLog (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747566"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="8c501-103">Método de log de erros IAMSetErrorLog:: get \_</span><span class="sxs-lookup"><span data-stu-id="8c501-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="8c501-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="8c501-104">\[Deprecated.</span></span> <span data-ttu-id="8c501-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c501-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8c501-106">O `get_ErrorLog` método recupera o log de erros atual para este objeto.</span><span class="sxs-lookup"><span data-stu-id="8c501-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c501-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c501-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8c501-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c501-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c501-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8c501-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8c501-110">Recebe um ponteiro para a interface [**IAMErrorLog**](iamerrorlog.md) do log de erros.</span><span class="sxs-lookup"><span data-stu-id="8c501-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="8c501-111">Se a linha do tempo não tiver um log de erros, o valor será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8c501-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c501-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c501-112">Return value</span></span>

<span data-ttu-id="8c501-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8c501-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8c501-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8c501-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c501-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c501-115">Remarks</span></span>

<span data-ttu-id="8c501-116">Se o valor retornado em *PVal* não for **NULL**, a interface [**IAMErrorLog**](iamerrorlog.md) terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="8c501-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="8c501-117">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="8c501-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="8c501-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="8c501-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8c501-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8c501-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8c501-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8c501-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8c501-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c501-121">Requirements</span></span>



| <span data-ttu-id="8c501-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c501-122">Requirement</span></span> | <span data-ttu-id="8c501-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8c501-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c501-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c501-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8c501-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c501-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8c501-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c501-126">Library</span></span><br/> | <dl> <span data-ttu-id="8c501-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8c501-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c501-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c501-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c501-129">**Interface IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="8c501-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="8c501-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="8c501-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




