---
description: O método Disconnect desconecta o NPP da rede.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: 'IDelaydC: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089964"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="cdff7-103">Método IDelaydC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="cdff7-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="cdff7-104">O método **Disconnect desconecta** o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="cdff7-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdff7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdff7-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="cdff7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdff7-106">Parameters</span></span>

<span data-ttu-id="cdff7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cdff7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdff7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cdff7-108">Return value</span></span>

<span data-ttu-id="cdff7-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="cdff7-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="cdff7-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="cdff7-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="cdff7-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cdff7-111">Return code</span></span>                                                                                          | <span data-ttu-id="cdff7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cdff7-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdff7-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff7-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="cdff7-114">O NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="cdff7-114">The NPP is capturing data.</span></span> <span data-ttu-id="cdff7-115">Não é possível desconectar o NPP da rede durante uma captura.</span><span class="sxs-lookup"><span data-stu-id="cdff7-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="cdff7-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff7-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cdff7-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="cdff7-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="cdff7-118"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="cdff7-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="cdff7-119">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="cdff7-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cdff7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdff7-120">Remarks</span></span>

<span data-ttu-id="cdff7-121">Este método não pode ser chamado quando o NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="cdff7-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="cdff7-122">Você deve chamar o método **IDelaydC:: Stop** antes de chamar **Disconnect**.</span><span class="sxs-lookup"><span data-stu-id="cdff7-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdff7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdff7-123">Requirements</span></span>



| <span data-ttu-id="cdff7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdff7-124">Requirement</span></span> | <span data-ttu-id="cdff7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cdff7-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdff7-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdff7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cdff7-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdff7-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="cdff7-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdff7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cdff7-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cdff7-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="cdff7-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cdff7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdff7-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdff7-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="cdff7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cdff7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdff7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdff7-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdff7-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="cdff7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdff7-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="cdff7-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="cdff7-136">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="cdff7-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="cdff7-137">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="cdff7-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




