---
title: Método IMsTscAxEvents OnReceivedTSPublicKey
description: Chamado durante a sequência de conexão quando o cliente recupera a chave pública do servidor. Esse evento só será chamado se a propriedade NotifyTSPublicKey for VARIANT \_ true.
ms.assetid: 1db98b8b-2f08-4252-ad8b-6764fa25b300
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnReceivedTSPublicKey
- Método OnReceivedTSPublicKey Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnReceivedTSPublicKey
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnReceivedTSPublicKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337a9efabe48dee7a5a4194c3b796b95f35a0592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455385"
---
# <a name="imstscaxeventsonreceivedtspublickey-method"></a><span data-ttu-id="e61ea-107">Método IMsTscAxEvents:: OnReceivedTSPublicKey</span><span class="sxs-lookup"><span data-stu-id="e61ea-107">IMsTscAxEvents::OnReceivedTSPublicKey method</span></span>

<span data-ttu-id="e61ea-108">Chamado durante a sequência de conexão quando o cliente recupera a chave pública do servidor.</span><span class="sxs-lookup"><span data-stu-id="e61ea-108">Called during the connection sequence when the client retrieves the public key from the server.</span></span> <span data-ttu-id="e61ea-109">Esse evento só será chamado se a propriedade **NotifyTSPublicKey** for **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="e61ea-109">This event is only called if the **NotifyTSPublicKey** property is **VARIANT\_TRUE**.</span></span> <span data-ttu-id="e61ea-110">Isso ocorre após a [**desconexão**](imstscaxevents-onconnecting.md), mas antes de OnAuthenticationWarningDisplayed [**e onconnected**](imstscaxevents-onconnected.md). [](imstscaxevents-onauthenticationwarningdisplayed.md)</span><span class="sxs-lookup"><span data-stu-id="e61ea-110">This is after [**OnConnecting**](imstscaxevents-onconnecting.md), but before [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) and [**OnConnected**](imstscaxevents-onconnected.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e61ea-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e61ea-111">Syntax</span></span>


```C++
void OnReceivedTSPublicKey(
  [in]  BSTR         publicKey,
  [out] VARIANT_BOOL *pfContinueLogon
);
```



## <a name="parameters"></a><span data-ttu-id="e61ea-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e61ea-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e61ea-113">*PublicKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e61ea-113">*publicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e61ea-114">Contém a chave pública do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="e61ea-114">Contains the public key of the remote machine.</span></span>

</dd> <dt>

<span data-ttu-id="e61ea-115">*pfContinueLogon* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e61ea-115">*pfContinueLogon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e61ea-116">Um ponteiro para uma **variável \_ bool variante** que recebe se o processo de logon deve continuar.</span><span class="sxs-lookup"><span data-stu-id="e61ea-116">A pointer to a **VARIANT\_BOOL** variable that receives whether the logon process should continue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e61ea-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e61ea-117">Return value</span></span>

<span data-ttu-id="e61ea-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e61ea-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e61ea-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e61ea-119">Remarks</span></span>

<span data-ttu-id="e61ea-120">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e61ea-120">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e61ea-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e61ea-121">Requirements</span></span>



| <span data-ttu-id="e61ea-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e61ea-122">Requirement</span></span> | <span data-ttu-id="e61ea-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e61ea-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e61ea-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e61ea-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e61ea-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e61ea-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e61ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e61ea-127">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="e61ea-127">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="e61ea-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e61ea-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="e61ea-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e61ea-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e61ea-130">DLL</span><span class="sxs-lookup"><span data-stu-id="e61ea-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e61ea-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e61ea-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e61ea-132">IID</span><span class="sxs-lookup"><span data-stu-id="e61ea-132">IID</span></span><br/>                      | <span data-ttu-id="e61ea-133">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e61ea-133">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e61ea-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e61ea-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e61ea-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e61ea-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





