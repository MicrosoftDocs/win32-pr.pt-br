---
title: Método IMsTscAxEvents OnAuthenticationWarningDisplayed
description: Chamado antes de um controle ActiveX exibir uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo erro de certificado).
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAuthenticationWarningDisplayed
- Método OnAuthenticationWarningDisplayed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAuthenticationWarningDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085487"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="698b6-106">Método IMsTscAxEvents:: OnAuthenticationWarningDisplayed</span><span class="sxs-lookup"><span data-stu-id="698b6-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="698b6-107">Chamado antes de um controle ActiveX exibir uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo erro de certificado).</span><span class="sxs-lookup"><span data-stu-id="698b6-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="698b6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="698b6-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="698b6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="698b6-109">Parameters</span></span>

<span data-ttu-id="698b6-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="698b6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="698b6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="698b6-111">Return value</span></span>

<span data-ttu-id="698b6-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="698b6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="698b6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="698b6-113">Remarks</span></span>

<span data-ttu-id="698b6-114">Se necessário, a propriedade [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) da interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) pode ser usada para garantir que a caixa de diálogo de autenticação modal a ser exibida será pai de uma janela especificada (isso pode ser necessário para impedir que os usuários usem outras caixas de diálogo enquanto a caixa de diálogo de autenticação for exibida).</span><span class="sxs-lookup"><span data-stu-id="698b6-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="698b6-115">Por padrão, o pai é a janela de controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="698b6-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="698b6-116">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="698b6-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="698b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="698b6-117">Requirements</span></span>



| <span data-ttu-id="698b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="698b6-118">Requirement</span></span> | <span data-ttu-id="698b6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="698b6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="698b6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="698b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="698b6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="698b6-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="698b6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="698b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="698b6-123">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="698b6-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="698b6-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="698b6-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="698b6-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="698b6-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="698b6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="698b6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="698b6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="698b6-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="698b6-128">IID</span><span class="sxs-lookup"><span data-stu-id="698b6-128">IID</span></span><br/>                      | <span data-ttu-id="698b6-129">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="698b6-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="698b6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="698b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="698b6-131">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="698b6-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="698b6-132">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="698b6-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="698b6-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="698b6-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





