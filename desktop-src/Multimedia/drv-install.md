---
title: Mensagem de DRV_INSTALL (mmsystem. h)
description: Notifica o driver que está sendo instalado. O driver deve criar e inicializar quaisquer chaves e valores de registro necessários e verificar se os drivers de suporte e o hardware estão instalados e corretamente configurados.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- Multimídia do Windows de mensagem DRV_INSTALL
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919147"
---
# <a name="drv_install-message"></a><span data-ttu-id="fc818-105">Mensagem de instalação do DRV \_</span><span class="sxs-lookup"><span data-stu-id="fc818-105">DRV\_INSTALL message</span></span>

<span data-ttu-id="fc818-106">Notifica o driver que está sendo instalado.</span><span class="sxs-lookup"><span data-stu-id="fc818-106">Notifies the driver that is it being installed.</span></span> <span data-ttu-id="fc818-107">O driver deve criar e inicializar quaisquer chaves e valores de registro necessários e verificar se os drivers de suporte e o hardware estão instalados e corretamente configurados.</span><span class="sxs-lookup"><span data-stu-id="fc818-107">The driver should create and initialize any needed registry keys and values and verify that the supporting drivers and hardware are installed and properly configured.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc818-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc818-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc818-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span><span class="sxs-lookup"><span data-stu-id="fc818-109"><span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*</span></span>
</dt> <dd>

<span data-ttu-id="fc818-110">Identificador do driver instalável.</span><span class="sxs-lookup"><span data-stu-id="fc818-110">Identifier of the installable driver.</span></span> <span data-ttu-id="fc818-111">Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .</span><span class="sxs-lookup"><span data-stu-id="fc818-111">This is the same value previously returned by the driver from the [**DRV\_OPEN**](drv-open.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="fc818-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span><span class="sxs-lookup"><span data-stu-id="fc818-112"><span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*</span></span>
</dt> <dd>

<span data-ttu-id="fc818-113">Identificador da instância de driver instalável.</span><span class="sxs-lookup"><span data-stu-id="fc818-113">Handle of the installable driver instance.</span></span>

</dd> <dt>

<span data-ttu-id="fc818-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="fc818-114"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="fc818-115">Endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fc818-115">Address of a [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) structure or **NULL**.</span></span> <span data-ttu-id="fc818-116">Se uma estrutura for fornecida, ela conterá os nomes da chave do registro e do valor associado ao driver.</span><span class="sxs-lookup"><span data-stu-id="fc818-116">If a structure is given, it contains the names of the registry key and value associated with the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc818-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fc818-117">Return Value</span></span>

<span data-ttu-id="fc818-118">Retorna um destes valores:</span><span class="sxs-lookup"><span data-stu-id="fc818-118">Returns one of these values:</span></span>



| <span data-ttu-id="fc818-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc818-119">Requirement</span></span> | <span data-ttu-id="fc818-120">Valor</span><span class="sxs-lookup"><span data-stu-id="fc818-120">Value</span></span> |
|-----------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc818-121">DRVCNF \_ OK</span><span class="sxs-lookup"><span data-stu-id="fc818-121">DRVCNF\_OK</span></span>      | <span data-ttu-id="fc818-122">A instalação foi bem-sucedida; nenhuma ação adicional é necessária.</span><span class="sxs-lookup"><span data-stu-id="fc818-122">The installation is successful; no further action is required.</span></span>                             |
| <span data-ttu-id="fc818-123">DRVCNF \_ cancelar</span><span class="sxs-lookup"><span data-stu-id="fc818-123">DRVCNF\_CANCEL</span></span>  | <span data-ttu-id="fc818-124">Falha na instalação..</span><span class="sxs-lookup"><span data-stu-id="fc818-124">The installation failed..</span></span>                                                                  |
| <span data-ttu-id="fc818-125">\_reinicialização DRVCNF</span><span class="sxs-lookup"><span data-stu-id="fc818-125">DRVCNF\_RESTART</span></span> | <span data-ttu-id="fc818-126">A instalação foi bem-sucedida, mas não entrará em vigor até que o sistema seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="fc818-126">The installation is successful, but it does not take effect until the system is restarted.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fc818-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc818-127">Remarks</span></span>

<span data-ttu-id="fc818-128">O parâmetro *lParam1* não é usado.</span><span class="sxs-lookup"><span data-stu-id="fc818-128">The *lParam1* parameter is not used.</span></span>

<span data-ttu-id="fc818-129">Alguns drivers instaláveis acrescentam informações de configuração ao valor atribuído ao valor de registro associado ao driver.</span><span class="sxs-lookup"><span data-stu-id="fc818-129">Some installable drivers append configuration information to the value assigned to the registry value associated with the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc818-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc818-130">Requirements</span></span>



| <span data-ttu-id="fc818-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc818-131">Requirement</span></span> | <span data-ttu-id="fc818-132">Valor</span><span class="sxs-lookup"><span data-stu-id="fc818-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc818-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc818-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fc818-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc818-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fc818-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc818-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fc818-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fc818-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fc818-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fc818-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc818-138"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc818-138"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc818-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc818-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc818-140">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="fc818-140">Installable Drivers</span></span>](installable-drivers.md)
</dt> <dt>

[<span data-ttu-id="fc818-141">Mensagens de driver instaláveis</span><span class="sxs-lookup"><span data-stu-id="fc818-141">Installable Driver Messages</span></span>](installable-driver-messages.md)
</dt> </dl>

 

