---
description: O método getcontrolstate recupera o estado da captura, o que indica se a captura está em execução ou em pausa.
ms.assetid: 0faf2300-d9ff-4fe0-9d50-18beafd1daea
title: 'Método IStats:: getcontrolstate (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a83b5d20461b28b7022bfdc3ddbf3d5d92149c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760043"
---
# <a name="istatsgetcontrolstate-method"></a><span data-ttu-id="ab562-103">Método IStats:: getcontrolstate</span><span class="sxs-lookup"><span data-stu-id="ab562-103">IStats::GetControlState method</span></span>

<span data-ttu-id="ab562-104">O método **Getcontrolstate** recupera o estado da [*captura*](c.md), o que indica se a captura está em execução ou em pausa.</span><span class="sxs-lookup"><span data-stu-id="ab562-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab562-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab562-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="ab562-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab562-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab562-107">*IsRunnning* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ab562-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab562-108">Indicador de que a captura atual está em execução, incluindo se a captura está em pausa.</span><span class="sxs-lookup"><span data-stu-id="ab562-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="ab562-109">*IsPaused* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ab562-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab562-110">Indicador de que a captura atual está em pausa.</span><span class="sxs-lookup"><span data-stu-id="ab562-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab562-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab562-111">Return value</span></span>

<span data-ttu-id="ab562-112">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="ab562-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ab562-113">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="ab562-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ab562-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ab562-114">Return code</span></span>                                                                                            | <span data-ttu-id="ab562-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab562-115">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab562-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ab562-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="ab562-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="ab562-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="ab562-118">Chame [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="ab562-118">Call [IStats::Connect](istats-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="ab562-119"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab562-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="ab562-120">O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ab562-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="ab562-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab562-121">Remarks</span></span>

<span data-ttu-id="ab562-122">Esse método pode ser chamado sempre que o NPP estiver conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="ab562-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="ab562-123">Você pode usar esse método para descobrir se uma captura está em execução, se a captura estiver pausada ou se a captura foi interrompida, mas o NPP não está desconectado.</span><span class="sxs-lookup"><span data-stu-id="ab562-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab562-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab562-124">Requirements</span></span>



| <span data-ttu-id="ab562-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab562-125">Requirement</span></span> | <span data-ttu-id="ab562-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ab562-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab562-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab562-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ab562-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab562-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ab562-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab562-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ab562-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab562-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ab562-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab562-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab562-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab562-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ab562-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ab562-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab562-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab562-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab562-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab562-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab562-136">IStats</span><span class="sxs-lookup"><span data-stu-id="ab562-136">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="ab562-137">IStats:: conectar</span><span class="sxs-lookup"><span data-stu-id="ab562-137">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="ab562-138">IStats::P ause</span><span class="sxs-lookup"><span data-stu-id="ab562-138">IStats::Pause</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="ab562-139">IStatsC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="ab562-139">IStatsC::Start</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="ab562-140">IStatsC:: Stop</span><span class="sxs-lookup"><span data-stu-id="ab562-140">IStatsC::Stop</span></span>](istats-stop.md)
</dt> </dl>

 

 




