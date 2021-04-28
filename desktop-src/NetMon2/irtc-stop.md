---
description: 'Método IRTC:: Stop – o método Stop interrompe a captura atual.'
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'Método IRTC:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113514"
---
# <a name="irtcstop-method"></a><span data-ttu-id="c816f-103">Método IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="c816f-103">IRTC::Stop method</span></span>

<span data-ttu-id="c816f-104">O método **Stop** interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="c816f-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c816f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c816f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="c816f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c816f-106">Parameters</span></span>

<span data-ttu-id="c816f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c816f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c816f-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c816f-108">Return value</span></span>

<span data-ttu-id="c816f-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="c816f-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c816f-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="c816f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c816f-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c816f-111">Return code</span></span>                                                                                          | <span data-ttu-id="c816f-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c816f-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c816f-113"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="c816f-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c816f-114">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="c816f-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="c816f-115">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="c816f-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c816f-116"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="c816f-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="c816f-117">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="c816f-117">The NPP is not capturing data.</span></span> <span data-ttu-id="c816f-118">Chame [IRTC:: Start](irtc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="c816f-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c816f-119"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="c816f-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="c816f-120">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c816f-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c816f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c816f-121">Remarks</span></span>

<span data-ttu-id="c816f-122">Ao reiniciar a captura depois de chamar o método **IRTC:: Stop** , chame [IRTC:: Configure](irtc-configure.md) cada vez que você chamar [IRTC:: Start](irtc-start.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="c816f-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c816f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c816f-123">Requirements</span></span>



| <span data-ttu-id="c816f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c816f-124">Requirement</span></span> | <span data-ttu-id="c816f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c816f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c816f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c816f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c816f-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c816f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c816f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c816f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c816f-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c816f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c816f-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c816f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c816f-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c816f-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c816f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c816f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c816f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c816f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c816f-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c816f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c816f-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="c816f-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="c816f-136">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="c816f-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="c816f-137">IRTC:: configurar</span><span class="sxs-lookup"><span data-stu-id="c816f-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="c816f-138">IRTC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="c816f-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




