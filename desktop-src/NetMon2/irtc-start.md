---
description: O método Start inicia a captura.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Método IRTC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827862"
---
# <a name="irtcstart-method"></a><span data-ttu-id="f7131-103">Método IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="f7131-103">IRTC::Start method</span></span>

<span data-ttu-id="f7131-104">O método **Start** inicia a captura.</span><span class="sxs-lookup"><span data-stu-id="f7131-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7131-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7131-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="f7131-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7131-106">Parameters</span></span>

<span data-ttu-id="f7131-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f7131-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7131-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7131-108">Return value</span></span>

<span data-ttu-id="f7131-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="f7131-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="f7131-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="f7131-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="f7131-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f7131-111">Return code</span></span>                                                                                           | <span data-ttu-id="f7131-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7131-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7131-113"><dt>**captura de NMERR \_ \_ pausada**</dt></span><span class="sxs-lookup"><span data-stu-id="f7131-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="f7131-114">A captura está em um estado de pausa e deve ser interrompida para que possa ser reiniciada.</span><span class="sxs-lookup"><span data-stu-id="f7131-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="f7131-115">Chame [IRTC:: Stop](idelaydc-stop.md) para interromper a captura.</span><span class="sxs-lookup"><span data-stu-id="f7131-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="f7131-116"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f7131-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="f7131-117">A captura já foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="f7131-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="f7131-118"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f7131-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="f7131-119">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="f7131-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="f7131-120">Chame [IRTC:: Connect](irtc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="f7131-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="f7131-121"><dt>**NMERR \_ não está em \_ tempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="f7131-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="f7131-122">O NPP está conectado à rede, mas não com o método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="f7131-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="f7131-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7131-123">Remarks</span></span>

<span data-ttu-id="f7131-124">Ao reiniciar a captura usando os métodos IRTC:: Start e [IRTC:: Stop](irtc-stop.md) , você deve chamar o método [IRTC:: Configure](irtc-configure.md) para reconfigurar a conexão cada vez que chamar IRTC:: Start para reiniciar a captura de dados.</span><span class="sxs-lookup"><span data-stu-id="f7131-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="f7131-125">Você também pode iniciar e parar a captura usando os métodos [IRTC::P ause](irtc-pause.md) e [IRTC:: resume](irtc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="f7131-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f7131-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7131-126">Requirements</span></span>



| <span data-ttu-id="f7131-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7131-127">Requirement</span></span> | <span data-ttu-id="f7131-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f7131-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7131-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7131-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f7131-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7131-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="f7131-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7131-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f7131-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7131-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="f7131-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f7131-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7131-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7131-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="f7131-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f7131-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7131-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7131-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7131-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7131-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7131-138">IRTC</span><span class="sxs-lookup"><span data-stu-id="f7131-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="f7131-139">IRTC:: configurar</span><span class="sxs-lookup"><span data-stu-id="f7131-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="f7131-140">IRTC:: conectar</span><span class="sxs-lookup"><span data-stu-id="f7131-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="f7131-141">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="f7131-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="f7131-142">IRTC:: retomar</span><span class="sxs-lookup"><span data-stu-id="f7131-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="f7131-143">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="f7131-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




