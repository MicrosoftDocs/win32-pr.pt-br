---
description: 'Método IRTC:: getcontrolstate – o método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.'
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'Método IRTC:: getcontrolstate (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2e41ad3e4119fffbada26fe3ebebdfe3bf82043
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110704"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="21e31-103">Método IRTC:: getcontrolstate</span><span class="sxs-lookup"><span data-stu-id="21e31-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="21e31-104">O método **Getcontrolstate** recupera o estado da [*captura*](c.md), o que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="21e31-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e31-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21e31-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="21e31-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21e31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e31-107">*IsRunnning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="21e31-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21e31-108">Indicador de que a captura atual está em execução, incluindo se a captura está em pausa.</span><span class="sxs-lookup"><span data-stu-id="21e31-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="21e31-109">*IsPaused* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="21e31-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21e31-110">Indicador de que a captura atual está em pausa.</span><span class="sxs-lookup"><span data-stu-id="21e31-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e31-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="21e31-111">Return value</span></span>

<span data-ttu-id="21e31-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="21e31-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="21e31-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="21e31-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="21e31-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="21e31-114">Return code</span></span>                                                                                          | <span data-ttu-id="21e31-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="21e31-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21e31-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="21e31-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="21e31-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="21e31-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="21e31-118">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="21e31-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="21e31-119"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="21e31-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="21e31-120">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="21e31-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="21e31-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="21e31-121">Remarks</span></span>

<span data-ttu-id="21e31-122">Esse método pode ser chamado sempre que o NPP estiver conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="21e31-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="21e31-123">Você pode usar esse método para descobrir se uma captura está em execução, se a captura estiver pausada ou se a captura foi interrompida, mas o NPP ainda está conectado.</span><span class="sxs-lookup"><span data-stu-id="21e31-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e31-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21e31-124">Requirements</span></span>



| <span data-ttu-id="21e31-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="21e31-125">Requirement</span></span> | <span data-ttu-id="21e31-126">Valor</span><span class="sxs-lookup"><span data-stu-id="21e31-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e31-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21e31-127">Minimum supported client</span></span><br/> | <span data-ttu-id="21e31-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21e31-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="21e31-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21e31-129">Minimum supported server</span></span><br/> | <span data-ttu-id="21e31-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="21e31-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="21e31-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="21e31-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="21e31-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="21e31-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="21e31-133">DLL</span><span class="sxs-lookup"><span data-stu-id="21e31-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21e31-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21e31-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21e31-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="21e31-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21e31-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="21e31-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="21e31-137">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="21e31-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="21e31-138">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="21e31-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="21e31-139">IRTC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="21e31-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="21e31-140">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="21e31-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




