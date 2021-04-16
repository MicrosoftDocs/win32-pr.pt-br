---
description: O método Stop interrompe a captura atual.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'Método IStats:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751410"
---
# <a name="istatsstop-method"></a><span data-ttu-id="44752-103">Método IStats:: Stop</span><span class="sxs-lookup"><span data-stu-id="44752-103">IStats::Stop method</span></span>

<span data-ttu-id="44752-104">O método **Stop** interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="44752-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="44752-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44752-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="44752-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44752-106">Parameters</span></span>

<span data-ttu-id="44752-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="44752-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44752-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44752-108">Return value</span></span>

<span data-ttu-id="44752-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="44752-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="44752-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="44752-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="44752-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="44752-111">Return code</span></span>                                                                                            | <span data-ttu-id="44752-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="44752-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="44752-113"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="44752-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="44752-114">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="44752-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="44752-115">Chame o método [IStats:: Connect](istats-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="44752-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="44752-116"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="44752-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="44752-117">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="44752-117">The NPP is not capturing data.</span></span> <span data-ttu-id="44752-118">Chame o método [IStats:: Start](istats-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="44752-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="44752-119"><dt>**NMERR \_ \_ somente não estatísticas \_**</dt></span><span class="sxs-lookup"><span data-stu-id="44752-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="44752-120">O NPP está conectado à rede, mas não com o método [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="44752-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="44752-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="44752-121">Remarks</span></span>

<span data-ttu-id="44752-122">Ao reiniciar a captura após **IStats:: Stop** ter sido chamado, certifique-se de chamar o método [IStats:: Configure](istats-configure.md) cada vez que chamar [IStats:: Start](istats-start.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="44752-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="44752-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44752-123">Requirements</span></span>



| <span data-ttu-id="44752-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="44752-124">Requirement</span></span> | <span data-ttu-id="44752-125">Valor</span><span class="sxs-lookup"><span data-stu-id="44752-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44752-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44752-126">Minimum supported client</span></span><br/> | <span data-ttu-id="44752-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44752-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="44752-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44752-128">Minimum supported server</span></span><br/> | <span data-ttu-id="44752-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44752-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="44752-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44752-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="44752-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44752-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="44752-132">DLL</span><span class="sxs-lookup"><span data-stu-id="44752-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44752-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44752-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44752-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="44752-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44752-135">IStats</span><span class="sxs-lookup"><span data-stu-id="44752-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="44752-136">IStats:: conectar</span><span class="sxs-lookup"><span data-stu-id="44752-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="44752-137">IStats:: configurar</span><span class="sxs-lookup"><span data-stu-id="44752-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="44752-138">IStats:: iniciar</span><span class="sxs-lookup"><span data-stu-id="44752-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




