---
title: Mensagem de DRV_CONFIGURE (mmsystem. h)
description: Direciona o driver instalável para exibir sua caixa de diálogo de configuração e permitir que o usuário especifique novas configurações para a instância de driver instalável fornecida.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- Multimídia do Windows de mensagem DRV_CONFIGURE
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919150"
---
# <a name="drv_configure-message"></a><span data-ttu-id="135a1-104">Mensagem de configuração de DRV \_</span><span class="sxs-lookup"><span data-stu-id="135a1-104">DRV\_CONFIGURE message</span></span>

<span data-ttu-id="135a1-105">Direciona o driver instalável para exibir sua caixa de diálogo de configuração e permitir que o usuário especifique novas configurações para a instância de driver instalável fornecida.</span><span class="sxs-lookup"><span data-stu-id="135a1-105">Directs the installable driver to display its configuration dialog box and let the user specify new settings for the given installable driver instance.</span></span>

## <a name="parameters"></a><span data-ttu-id="135a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="135a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="135a1-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="135a1-107"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="135a1-108">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="135a1-108">Identifier of the installable driver.</span></span> <span data-ttu-id="135a1-109">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="135a1-109">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="135a1-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="135a1-110"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="135a1-111">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="135a1-111">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="135a1-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="135a1-112"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="135a1-113">Identificador da janela pai.</span><span class="sxs-lookup"><span data-stu-id="135a1-113">Handle of the parent window.</span></span> <span data-ttu-id="135a1-114">Essa janela é usada como a janela pai da caixa de diálogo de configuração.</span><span class="sxs-lookup"><span data-stu-id="135a1-114">This window is used as the parent window for the configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="135a1-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="135a1-115"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="135a1-116">Endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="135a1-116">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="135a1-117">Se a estrutura for fornecida, ela conterá os nomes da chave do registro e do valor associado ao driver.</span><span class="sxs-lookup"><span data-stu-id="135a1-117">If the structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="135a1-118">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="135a1-118">Return Value</span></span>

<span data-ttu-id="135a1-119">Retorna um destes valores:</span><span class="sxs-lookup"><span data-stu-id="135a1-119">Returns one of these values:</span></span>



| <span data-ttu-id="135a1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="135a1-120">Requirement</span></span> | <span data-ttu-id="135a1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="135a1-121">Value</span></span> |
|-----------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="135a1-122">DRVCNF \_ OK</span><span class="sxs-lookup"><span data-stu-id="135a1-122">DRVCNF\_OK</span></span>      | <span data-ttu-id="135a1-123">A configuração foi bem-sucedida; nenhuma ação adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="135a1-123">The configuration is successful; no further action is required.</span></span>                                    |
| <span data-ttu-id="135a1-124">DRVCNF \_ cancelar</span><span class="sxs-lookup"><span data-stu-id="135a1-124">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="135a1-125">O usuário cancelou a caixa de diálogo; nenhuma ação adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="135a1-125">The user canceled the dialog box; no further action is required.</span></span>                                   |
| <span data-ttu-id="135a1-126">\_reinicialização DRVCNF</span><span class="sxs-lookup"><span data-stu-id="135a1-126">DRVCNF\_RESTART</span></span> | <span data-ttu-id="135a1-127">A configuração foi bem-sucedida, mas as alterações não entram em vigor até que o sistema seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="135a1-127">The configuration is successful, but the changes do not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="135a1-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="135a1-128">Remarks</span></span>

<span data-ttu-id="135a1-129">Alguns drivers instaláveis acrescentam informações de configuração ao valor atribuído ao valor de registro associado ao driver.</span><span class="sxs-lookup"><span data-stu-id="135a1-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

<span data-ttu-id="135a1-130">Os valores de retorno do DRV \_ Cancel, drv \_ OK e drv \_ Restart são obsoletos; eles foram substituídos por DRVCNF \_ Cancel, DRVCNF \_ OK e DRVCNF \_ restart, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="135a1-130">The DRV\_CANCEL, DRV\_OK, and DRV\_RESTART return values are obsolete; they have been replaced by DRVCNF\_CANCEL, DRVCNF\_OK, and DRVCNF\_RESTART, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="135a1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="135a1-131">Requirements</span></span>



| <span data-ttu-id="135a1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="135a1-132">Requirement</span></span> | <span data-ttu-id="135a1-133">Valor</span><span class="sxs-lookup"><span data-stu-id="135a1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="135a1-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="135a1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="135a1-135">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="135a1-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="135a1-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="135a1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="135a1-137">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="135a1-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="135a1-138">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="135a1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="135a1-139"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="135a1-139"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="135a1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="135a1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="135a1-141">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="135a1-141">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="135a1-142">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="135a1-142">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

