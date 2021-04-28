---
description: 'Método IDelaydC:: getcontrolstate – o método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.'
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
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110764"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="c5553-103">Método IDelaydC:: getcontrolstate</span><span class="sxs-lookup"><span data-stu-id="c5553-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="c5553-104">O método **Getcontrolstate** recupera o estado da [*captura*](c.md), o que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="c5553-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5553-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5553-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="c5553-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5553-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5553-107">*IsRunnning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c5553-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5553-108">Indicador de que a captura atual está em execução, incluindo se a captura está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c5553-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="c5553-109">*IsPaused* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c5553-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5553-110">Indicador de que a captura atual está em pausa.</span><span class="sxs-lookup"><span data-stu-id="c5553-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5553-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c5553-111">Return value</span></span>

<span data-ttu-id="c5553-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c5553-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c5553-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="c5553-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c5553-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c5553-114">Return code</span></span>                                                                                          | <span data-ttu-id="c5553-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5553-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5553-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="c5553-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c5553-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="c5553-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="c5553-118">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="c5553-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c5553-119"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="c5553-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="c5553-120">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c5553-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c5553-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5553-121">Remarks</span></span>

<span data-ttu-id="c5553-122">Esse método pode ser chamado sempre que o NPP estiver conectado à rede usando a interface [IDelaydC](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="c5553-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="c5553-123">Você pode usar esse método para descobrir se uma captura está em execução, se a captura estiver pausada ou se a captura foi interrompida, mas o NPP não está desconectado.</span><span class="sxs-lookup"><span data-stu-id="c5553-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="c5553-124">Os métodos usados para iniciar, pausar e parar a captura são listados na lista consulte também abaixo.</span><span class="sxs-lookup"><span data-stu-id="c5553-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5553-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5553-125">Requirements</span></span>



| <span data-ttu-id="c5553-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5553-126">Requirement</span></span> | <span data-ttu-id="c5553-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c5553-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5553-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5553-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c5553-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5553-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c5553-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5553-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c5553-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5553-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c5553-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c5553-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5553-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5553-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c5553-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c5553-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5553-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5553-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5553-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c5553-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5553-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="c5553-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c5553-138">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="c5553-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c5553-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="c5553-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="c5553-140">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="c5553-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c5553-141">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="c5553-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




