---
description: O método Stop interrompe a captura atual.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Método IDelaydC:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460956"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="e5424-103">Método IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="e5424-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="e5424-104">O método **Stop** interrompe a captura atual.</span><span class="sxs-lookup"><span data-stu-id="e5424-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5424-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5424-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="e5424-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5424-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5424-107">*lpStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e5424-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5424-108">Ponteiro para uma estrutura de [estatísticas](statistics.md) que contém estatísticas de rede, como total de quadros e total de bytes capturados.</span><span class="sxs-lookup"><span data-stu-id="e5424-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5424-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5424-109">Return value</span></span>

<span data-ttu-id="e5424-110">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="e5424-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="e5424-111">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="e5424-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="e5424-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5424-112">Return code</span></span>                                                                                          | <span data-ttu-id="e5424-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5424-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5424-114"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="e5424-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e5424-115">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="e5424-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="e5424-116">Chame [IDelaydC:: Connect](idelaydc-connect.md) para conectar o NPP à rede.</span><span class="sxs-lookup"><span data-stu-id="e5424-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="e5424-117"><dt>**NMERR \_ não \_ capturando**</dt></span><span class="sxs-lookup"><span data-stu-id="e5424-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="e5424-118">O NPP não está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="e5424-118">The NPP is not capturing data.</span></span> <span data-ttu-id="e5424-119">Chame [IDelaydC:: Start](idelaydc-start.md) para iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="e5424-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="e5424-120"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="e5424-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="e5424-121">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="e5424-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="e5424-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5424-122">Remarks</span></span>

<span data-ttu-id="e5424-123">Quando **IDelaydC:: Stop** é chamado, monitor de rede para de capturar dados e fecha o [*arquivo de captura*](c.md).</span><span class="sxs-lookup"><span data-stu-id="e5424-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="e5424-124">(O nome do arquivo de captura foi retornado quando [IDelaydC:: Start](idelaydc-start.md) foi chamado).</span><span class="sxs-lookup"><span data-stu-id="e5424-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="e5424-125">Agora você pode examinar o conteúdo do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e5424-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="e5424-126">Quando você parar e iniciar a captura, certifique-se de chamar o método [IDelaydC:: Configure](idelaydc-configure.md) cada vez que chamar [IDelaydC:: Start](idelaydc-start.md) para reiniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="e5424-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5424-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5424-127">Requirements</span></span>



| <span data-ttu-id="e5424-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5424-128">Requirement</span></span> | <span data-ttu-id="e5424-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e5424-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5424-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5424-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e5424-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5424-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="e5424-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5424-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e5424-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5424-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="e5424-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e5424-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5424-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5424-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="e5424-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e5424-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5424-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5424-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5424-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5424-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5424-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="e5424-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="e5424-140">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="e5424-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="e5424-141">IDelaydC:: configurar</span><span class="sxs-lookup"><span data-stu-id="e5424-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="e5424-142">IDelaydC:: iniciar</span><span class="sxs-lookup"><span data-stu-id="e5424-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="e5424-143">ESTATÍSTICA</span><span class="sxs-lookup"><span data-stu-id="e5424-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




