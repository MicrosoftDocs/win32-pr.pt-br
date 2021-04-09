---
description: O método Disconnect desconecta o NPP da rede.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: 'IESP: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b0dac1843083d77121883b2609c32addffbae290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089960"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="de3a1-103">Método IESP::D isconnect</span><span class="sxs-lookup"><span data-stu-id="de3a1-103">IESP::Disconnect method</span></span>

<span data-ttu-id="de3a1-104">O método **Disconnect desconecta** o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="de3a1-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de3a1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="de3a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de3a1-106">Parameters</span></span>

<span data-ttu-id="de3a1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="de3a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de3a1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de3a1-108">Return value</span></span>

<span data-ttu-id="de3a1-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="de3a1-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="de3a1-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="de3a1-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="de3a1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="de3a1-111">Return code</span></span>                                                                                          | <span data-ttu-id="de3a1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="de3a1-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de3a1-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de3a1-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="de3a1-114">O NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="de3a1-114">The NPP is capturing data.</span></span> <span data-ttu-id="de3a1-115">Não é possível desconectar da rede enquanto a captura de dados está em andamento.</span><span class="sxs-lookup"><span data-stu-id="de3a1-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="de3a1-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="de3a1-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="de3a1-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="de3a1-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="de3a1-118"><dt>**NMERR \_ não \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="de3a1-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="de3a1-119">O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="de3a1-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="de3a1-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="de3a1-120">Remarks</span></span>

<span data-ttu-id="de3a1-121">Este método não pode ser chamado quando o NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="de3a1-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="de3a1-122">Você deve chamar o método **IESP:: Stop** antes de chamar **IESP::D isconnect**.</span><span class="sxs-lookup"><span data-stu-id="de3a1-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3a1-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de3a1-123">Requirements</span></span>



| <span data-ttu-id="de3a1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="de3a1-124">Requirement</span></span> | <span data-ttu-id="de3a1-125">Valor</span><span class="sxs-lookup"><span data-stu-id="de3a1-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3a1-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de3a1-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de3a1-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de3a1-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="de3a1-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de3a1-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de3a1-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de3a1-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="de3a1-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="de3a1-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="de3a1-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="de3a1-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="de3a1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="de3a1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de3a1-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de3a1-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3a1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="de3a1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3a1-135">IESP</span><span class="sxs-lookup"><span data-stu-id="de3a1-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="de3a1-136">IESP:: conectar</span><span class="sxs-lookup"><span data-stu-id="de3a1-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="de3a1-137">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="de3a1-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




