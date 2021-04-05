---
title: Método IMsTscAxEvents OnConfirmClose
description: Chamado quando o cliente chama o método IMsRdpClient RequestClose.
ms.assetid: fb149fbc-9415-4c4c-8d4b-e22214ac38cb
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnConfirmClose
- Método OnConfirmClose Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnConfirmClose
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConfirmClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 623196033e23a964857a6a604c7eca3904f32c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086491"
---
# <a name="imstscaxeventsonconfirmclose-method"></a><span data-ttu-id="0a6fa-106">Método IMsTscAxEvents:: OnConfirmClose</span><span class="sxs-lookup"><span data-stu-id="0a6fa-106">IMsTscAxEvents::OnConfirmClose method</span></span>

<span data-ttu-id="0a6fa-107">Chamado quando o cliente chama o método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) .</span><span class="sxs-lookup"><span data-stu-id="0a6fa-107">Called when the client calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method.</span></span> <span data-ttu-id="0a6fa-108">Em resposta a esse evento, o usuário deve ser solicitado a confirmar o fechamento da conexão.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-108">In response to this event, the user should be prompted to confirm closing the connection.</span></span> <span data-ttu-id="0a6fa-109">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-109">For more information, see the following Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a6fa-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a6fa-110">Syntax</span></span>


```C++
void OnConfirmClose(
  [out] VARIANT_BOOL *pfAllowClose
);
```



## <a name="parameters"></a><span data-ttu-id="0a6fa-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a6fa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a6fa-112">*pfAllowClose* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0a6fa-112">*pfAllowClose* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a6fa-113">Se **Variant \_ true**, o padrão, indica que o usuário deseja fechar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-113">If **VARIANT\_TRUE**, the default, indicates that the user wants to close the connection.</span></span> <span data-ttu-id="0a6fa-114">Se **Variant \_ false**, indica que o usuário não deseja fechar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-114">If **VARIANT\_FALSE**, indicates that the user does not want to close the connection.</span></span> <span data-ttu-id="0a6fa-115">Para obter mais informações, consulte a seção Comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-115">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a6fa-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a6fa-116">Return value</span></span>

<span data-ttu-id="0a6fa-117">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a6fa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a6fa-118">Remarks</span></span>

<span data-ttu-id="0a6fa-119">Quando um aplicativo de contêiner chama o método [**IMsRdpClient:: RequestClose**](imsrdpclient-requestclose.md) , esse método retorna um valor que indica se o contêiner deve aguardar a ocorrência de um evento **OnConfirmClose** antes de fechar a conexão de controle.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-119">When a container application calls the [**IMsRdpClient::RequestClose**](imsrdpclient-requestclose.md) method, that method returns a value indicating whether the container should wait for an **OnConfirmClose** event to occur before closing the control connection.</span></span> <span data-ttu-id="0a6fa-120">Se **RequestClose** retornar **controlCloseWaitForEvents** e o usuário estiver conectado e conectado à sua sessão de serviços de área de trabalho remota, o evento **OnConfirmClose** será acionado.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-120">If **RequestClose** returns **controlCloseWaitForEvents**, and the user is connected and logged on to their Remote Desktop Services session, the **OnConfirmClose** event fires.</span></span> <span data-ttu-id="0a6fa-121">Nesse ponto, o aplicativo de contêiner pode solicitar o usuário, perguntando se o usuário deseja fechar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-121">At that point the container application can prompt the user, asking whether the user wants to close the connection.</span></span> <span data-ttu-id="0a6fa-122">Se o usuário quiser fechar a conexão, o aplicativo deverá definir o parâmetro *pfAllowClose* como **Variant \_ true** e continuar com o fechamento da conexão.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-122">If the user wants to close the connection, the application should set the *pfAllowClose* parameter to **VARIANT\_TRUE** and proceed with closing the connection.</span></span> <span data-ttu-id="0a6fa-123">Se o usuário não quiser fechar, o aplicativo deverá definir *pfAllowClose* como **Variant \_ false** e deixar a conexão aberta.</span><span class="sxs-lookup"><span data-stu-id="0a6fa-123">If the user does not want to close, the application should set *pfAllowClose* to **VARIANT\_FALSE** and leave the connection open.</span></span>

<span data-ttu-id="0a6fa-124">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a6fa-124">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a6fa-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a6fa-125">Requirements</span></span>



| <span data-ttu-id="0a6fa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a6fa-126">Requirement</span></span> | <span data-ttu-id="0a6fa-127">Valor</span><span class="sxs-lookup"><span data-stu-id="0a6fa-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6fa-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a6fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6fa-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a6fa-129">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0a6fa-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a6fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6fa-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a6fa-131">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0a6fa-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a6fa-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a6fa-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a6fa-133"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a6fa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0a6fa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a6fa-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a6fa-135"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a6fa-136">IID</span><span class="sxs-lookup"><span data-stu-id="0a6fa-136">IID</span></span><br/>                      | <span data-ttu-id="0a6fa-137">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="0a6fa-137">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="0a6fa-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a6fa-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6fa-139">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="0a6fa-139">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





