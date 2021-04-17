---
description: O método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'Método IESP:: getcontrolstate (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c791d5dc1f5d5321268fef2fb5cf91e04d9ecff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779973"
---
# <a name="iespgetcontrolstate-method"></a><span data-ttu-id="0726d-103">Método IESP:: getcontrolstate</span><span class="sxs-lookup"><span data-stu-id="0726d-103">IESP::GetControlState method</span></span>

<span data-ttu-id="0726d-104">O método **Getcontrolstate** recupera o estado da [*captura*](c.md), o que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="0726d-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="0726d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0726d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="0726d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0726d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0726d-107">*IsRunnning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0726d-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0726d-108">Indicador de que a captura atual está em execução, incluindo se a captura está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0726d-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="0726d-109">*IsPaused* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0726d-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0726d-110">Indicador de que a captura atual está em pausa.</span><span class="sxs-lookup"><span data-stu-id="0726d-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0726d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0726d-111">Return value</span></span>

<span data-ttu-id="0726d-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="0726d-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0726d-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="0726d-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0726d-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0726d-114">Return code</span></span>                                                                                          | <span data-ttu-id="0726d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0726d-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0726d-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="0726d-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0726d-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="0726d-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="0726d-118">Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="0726d-118">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0726d-119"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="0726d-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="0726d-120">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0726d-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0726d-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0726d-121">Remarks</span></span>

<span data-ttu-id="0726d-122">Esse método pode ser chamado sempre que o NPP estiver conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="0726d-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="0726d-123">Você pode usar esse método para descobrir se uma captura está em execução, se a captura estiver pausada ou se a captura foi interrompida, mas o NPP ainda está conectado.</span><span class="sxs-lookup"><span data-stu-id="0726d-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="0726d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0726d-124">Requirements</span></span>



| <span data-ttu-id="0726d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0726d-125">Requirement</span></span> | <span data-ttu-id="0726d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0726d-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0726d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0726d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0726d-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0726d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0726d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0726d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0726d-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0726d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0726d-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0726d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0726d-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0726d-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0726d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0726d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0726d-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0726d-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0726d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="0726d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0726d-136">IESP</span><span class="sxs-lookup"><span data-stu-id="0726d-136">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="0726d-137">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="0726d-137">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="0726d-138">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="0726d-138">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="0726d-139">IESP:: iniciar</span><span class="sxs-lookup"><span data-stu-id="0726d-139">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="0726d-140">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="0726d-140">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




