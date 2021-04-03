---
title: Método IMsTscAxEvents OnServiceMessageReceived
description: Chamado quando o cliente recebe uma mensagem do sistema.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnServiceMessageReceived
- Método OnServiceMessageReceived Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644797"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="aa359-106">Método IMsTscAxEvents:: OnServiceMessageReceived</span><span class="sxs-lookup"><span data-stu-id="aa359-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="aa359-107">Chamado quando o cliente recebe uma mensagem do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa359-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa359-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa359-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="aa359-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa359-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa359-110">*mensagens* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa359-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa359-111">Especifica a mensagem do sistema.</span><span class="sxs-lookup"><span data-stu-id="aa359-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa359-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa359-112">Return value</span></span>

<span data-ttu-id="aa359-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="aa359-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa359-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa359-114">Remarks</span></span>

<span data-ttu-id="aa359-115">Para obter mais informações sobre mensagens do sistema, consulte [Configurar mensagens para um servidor Gateway área de trabalho remota](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="aa359-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa359-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa359-116">Requirements</span></span>



| <span data-ttu-id="aa359-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa359-117">Requirement</span></span> | <span data-ttu-id="aa359-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa359-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa359-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa359-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aa359-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa359-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="aa359-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa359-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aa359-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa359-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="aa359-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa359-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa359-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa359-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa359-125">DLL</span><span class="sxs-lookup"><span data-stu-id="aa359-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa359-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa359-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa359-127">IID</span><span class="sxs-lookup"><span data-stu-id="aa359-127">IID</span></span><br/>                      | <span data-ttu-id="aa359-128">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="aa359-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="aa359-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa359-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa359-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="aa359-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

