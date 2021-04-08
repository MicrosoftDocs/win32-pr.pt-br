---
description: O método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'Método IDelaydC:: getcontrolstate (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8f5c3f084db788844f061ba2005d9c3ca38acef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920686"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="53fe4-103">Método IDelaydC:: getcontrolstate</span><span class="sxs-lookup"><span data-stu-id="53fe4-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="53fe4-104">O método **Getcontrolstate** recupera o estado da [*captura*](c.md), o que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="53fe4-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="53fe4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53fe4-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="53fe4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53fe4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53fe4-107">*IsRunnning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53fe4-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53fe4-108">Indicador de que a captura atual está em execução, incluindo se a captura está em pausa.</span><span class="sxs-lookup"><span data-stu-id="53fe4-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="53fe4-109">*IsPaused* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53fe4-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53fe4-110">Indicador de que a captura atual está em pausa.</span><span class="sxs-lookup"><span data-stu-id="53fe4-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53fe4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53fe4-111">Return value</span></span>

<span data-ttu-id="53fe4-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="53fe4-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="53fe4-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="53fe4-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="53fe4-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="53fe4-114">Return code</span></span>                                                                                          | <span data-ttu-id="53fe4-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="53fe4-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53fe4-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="53fe4-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="53fe4-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="53fe4-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="53fe4-118">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="53fe4-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="53fe4-119"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="53fe4-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="53fe4-120">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="53fe4-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="53fe4-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="53fe4-121">Remarks</span></span>

<span data-ttu-id="53fe4-122">Esse método pode ser chamado sempre que o NPP estiver conectado à rede usando a interface [IDelaydC](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="53fe4-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="53fe4-123">Você pode usar esse método para descobrir se uma captura está em execução, se a captura estiver pausada ou se a captura foi interrompida, mas o NPP não está desconectado.</span><span class="sxs-lookup"><span data-stu-id="53fe4-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="53fe4-124">Os métodos usados para iniciar, pausar e parar a captura são listados na lista consulte também abaixo.</span><span class="sxs-lookup"><span data-stu-id="53fe4-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="53fe4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53fe4-125">Requirements</span></span>



| <span data-ttu-id="53fe4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="53fe4-126">Requirement</span></span> | <span data-ttu-id="53fe4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="53fe4-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53fe4-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53fe4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="53fe4-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53fe4-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="53fe4-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="53fe4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="53fe4-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="53fe4-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="53fe4-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="53fe4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="53fe4-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="53fe4-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="53fe4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="53fe4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53fe4-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53fe4-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53fe4-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="53fe4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fe4-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="53fe4-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="53fe4-138">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="53fe4-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="53fe4-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="53fe4-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="53fe4-140">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="53fe4-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="53fe4-141">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="53fe4-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




