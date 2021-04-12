---
title: Método IMsTscAxEvents OnAuthenticationWarningDismissed
description: Chamado depois que um controle ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnAuthenticationWarningDismissed
- Método OnAuthenticationWarningDismissed Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnAuthenticationWarningDismissed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369577"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="3804c-106">Método IMsTscAxEvents:: OnAuthenticationWarningDismissed</span><span class="sxs-lookup"><span data-stu-id="3804c-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="3804c-107">Chamado depois que um controle ActiveX exibe uma caixa de diálogo de autenticação (por exemplo, a caixa de diálogo de erro do certificado).</span><span class="sxs-lookup"><span data-stu-id="3804c-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="3804c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3804c-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="3804c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3804c-109">Parameters</span></span>

<span data-ttu-id="3804c-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3804c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3804c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3804c-111">Return value</span></span>

<span data-ttu-id="3804c-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3804c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3804c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3804c-113">Remarks</span></span>

<span data-ttu-id="3804c-114">Se necessário, a propriedade [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) da interface [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) pode ser usada para reverter qualquer pai que tenha sido feito no método [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) .</span><span class="sxs-lookup"><span data-stu-id="3804c-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="3804c-115">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3804c-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3804c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3804c-116">Requirements</span></span>



| <span data-ttu-id="3804c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3804c-117">Requirement</span></span> | <span data-ttu-id="3804c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3804c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3804c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3804c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3804c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3804c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3804c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3804c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3804c-122">Windows Server 2008, Windows Server 2008 com SP1</span><span class="sxs-lookup"><span data-stu-id="3804c-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="3804c-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3804c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3804c-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3804c-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3804c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3804c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3804c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3804c-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3804c-127">IID</span><span class="sxs-lookup"><span data-stu-id="3804c-127">IID</span></span><br/>                      | <span data-ttu-id="3804c-128">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="3804c-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3804c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3804c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3804c-130">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="3804c-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="3804c-131">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="3804c-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="3804c-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="3804c-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





