---
description: 'IDelaydC: método isconnect:D-o método Disconnect desconecta o NPP da rede.'
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
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110804"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="ab1b3-103">Método IDelaydC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="ab1b3-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="ab1b3-104">O método **Disconnect desconecta** o NPP da rede.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab1b3-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="ab1b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab1b3-106">Parameters</span></span>

<span data-ttu-id="ab1b3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab1b3-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ab1b3-108">Return value</span></span>

<span data-ttu-id="ab1b3-109">Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ab1b3-110">Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="ab1b3-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="ab1b3-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ab1b3-111">Return code</span></span>                                                                                          | <span data-ttu-id="ab1b3-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab1b3-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab1b3-113"><dt>**captura de NMERR \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b3-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="ab1b3-114">O NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-114">The NPP is capturing data.</span></span> <span data-ttu-id="ab1b3-115">Não é possível desconectar o NPP da rede durante uma captura.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="ab1b3-116"><dt>**NMERR \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b3-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="ab1b3-117">O NPP não está conectado à rede.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="ab1b3-118"><dt>**NMERR \_ não \_ atrasada**</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b3-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="ab1b3-119">O NPP está conectado à rede, mas não com o método [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="ab1b3-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab1b3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab1b3-120">Remarks</span></span>

<span data-ttu-id="ab1b3-121">Este método não pode ser chamado quando o NPP está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="ab1b3-122">Você deve chamar o método **IDelaydC:: Stop** antes de chamar **Disconnect**.</span><span class="sxs-lookup"><span data-stu-id="ab1b3-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1b3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab1b3-123">Requirements</span></span>



| <span data-ttu-id="ab1b3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab1b3-124">Requirement</span></span> | <span data-ttu-id="ab1b3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ab1b3-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1b3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab1b3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1b3-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab1b3-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="ab1b3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab1b3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1b3-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ab1b3-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="ab1b3-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ab1b3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab1b3-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b3-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="ab1b3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ab1b3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab1b3-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b3-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1b3-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ab1b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1b3-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="ab1b3-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="ab1b3-136">IDelaydC:: conectar</span><span class="sxs-lookup"><span data-stu-id="ab1b3-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="ab1b3-137">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="ab1b3-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




