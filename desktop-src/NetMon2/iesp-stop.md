---
description: 'Método IESP:: Stop – o método Stop interrompe a captura atual.'
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
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103764"
---
# <a name="iespstop-method"></a><span data-ttu-id="6ad82-103">Método IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="6ad82-103">IESP::Stop method</span></span>

<span data-ttu-id="6ad82-104">O método **Stop** interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="6ad82-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad82-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ad82-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="6ad82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ad82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad82-107">*lpStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6ad82-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad82-108">Ponteiro para uma estrutura de [estatísticas](statistics.md) que contém estatísticas de rede, como total de quadros e total de bytes capturados.</span><span class="sxs-lookup"><span data-stu-id="6ad82-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad82-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6ad82-109">Return value</span></span>

<span data-ttu-id="6ad82-110">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="6ad82-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6ad82-111">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="6ad82-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="6ad82-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ad82-112">Return code</span></span>                                                                                          | <span data-ttu-id="6ad82-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ad82-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ad82-114"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad82-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6ad82-115">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="6ad82-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="6ad82-116">Chame [IESP:: Connect](iesp-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="6ad82-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="6ad82-117"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad82-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="6ad82-118">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="6ad82-118">The NPP is not capturing data.</span></span> <span data-ttu-id="6ad82-119">Chame [IESP:: Start](iesp-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="6ad82-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="6ad82-120"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="6ad82-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="6ad82-121">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad82-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="6ad82-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ad82-122">Remarks</span></span>

<span data-ttu-id="6ad82-123">Quando o método **IESP:: Stop** é chamado, monitor de rede para de capturar dados e fecha o [*arquivo de captura.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="6ad82-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="6ad82-124">(O nome do arquivo de captura foi retornado quando [IESP:: Start](iesp-start.md) foi chamado.) Agora você pode examinar o conteúdo do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="6ad82-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="6ad82-125">Quando você parar e reiniciar a captura, certifique-se de chamar o método [IESP:: Configure](iesp-configure.md) cada vez que chamar [IESP:: Start](iesp-start.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="6ad82-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad82-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ad82-126">Requirements</span></span>



| <span data-ttu-id="6ad82-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ad82-127">Requirement</span></span> | <span data-ttu-id="6ad82-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad82-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad82-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad82-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad82-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ad82-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6ad82-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad82-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad82-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6ad82-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6ad82-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6ad82-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ad82-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ad82-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6ad82-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad82-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ad82-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad82-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ad82-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6ad82-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ad82-138">IESP</span><span class="sxs-lookup"><span data-stu-id="6ad82-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="6ad82-139">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="6ad82-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="6ad82-140">IESP:: iniciar</span><span class="sxs-lookup"><span data-stu-id="6ad82-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="6ad82-141">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="6ad82-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




