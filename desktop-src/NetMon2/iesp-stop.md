---
description: O método Stop interrompe a captura atual.
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: 'Método IESP:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 50dfb274e1355af93c473609f95607e6b3faf1fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789514"
---
# <a name="iespstop-method"></a><span data-ttu-id="dc61d-103">Método IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="dc61d-103">IESP::Stop method</span></span>

<span data-ttu-id="dc61d-104">O método **Stop** interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="dc61d-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc61d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc61d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="dc61d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc61d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc61d-107">*lpStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="dc61d-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc61d-108">Ponteiro para uma estrutura de [estatísticas](statistics.md) que contém estatísticas de rede, como total de quadros e total de bytes capturados.</span><span class="sxs-lookup"><span data-stu-id="dc61d-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc61d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc61d-109">Return value</span></span>

<span data-ttu-id="dc61d-110">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="dc61d-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dc61d-111">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="dc61d-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dc61d-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="dc61d-112">Return code</span></span>                                                                                          | <span data-ttu-id="dc61d-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dc61d-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc61d-114"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dc61d-115">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="dc61d-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="dc61d-116">Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="dc61d-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="dc61d-117"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="dc61d-118">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="dc61d-118">The NPP is not capturing data.</span></span> <span data-ttu-id="dc61d-119">Chame [IESP:: Start](iesp-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="dc61d-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="dc61d-120"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="dc61d-121">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="dc61d-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="dc61d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc61d-122">Remarks</span></span>

<span data-ttu-id="dc61d-123">Quando o método **IESP:: Stop** é chamado, monitor de rede para de capturar dados e fecha o [*arquivo de captura.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="dc61d-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="dc61d-124">(O nome do arquivo de captura foi retornado quando [IESP:: Start](iesp-start.md) foi chamado.) Agora você pode examinar o conteúdo do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="dc61d-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="dc61d-125">Quando você parar e reiniciar a captura, certifique-se de chamar o método [IESP:: Configure](iesp-configure.md) cada vez que chamar [IESP:: Start](iesp-start.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="dc61d-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc61d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc61d-126">Requirements</span></span>



| <span data-ttu-id="dc61d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc61d-127">Requirement</span></span> | <span data-ttu-id="dc61d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dc61d-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc61d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc61d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dc61d-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc61d-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dc61d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc61d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dc61d-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dc61d-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dc61d-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dc61d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc61d-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dc61d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="dc61d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc61d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc61d-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc61d-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc61d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc61d-138">IESP</span><span class="sxs-lookup"><span data-stu-id="dc61d-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="dc61d-139">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="dc61d-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="dc61d-140">IESP:: iniciar</span><span class="sxs-lookup"><span data-stu-id="dc61d-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="dc61d-141">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="dc61d-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




