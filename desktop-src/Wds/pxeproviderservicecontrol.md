---
title: Função de retorno de chamada PxeProviderServiceControl
description: Chamado quando um código de controle de serviço é recebido pelo serviço WDS.
ms.assetid: 180ddcda-d111-4c81-9177-db99cbf1449f
keywords:
- Função de retorno de chamada do PxeProviderServiceControl serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderServiceControl
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c8a2c71b7b386254622758efa5f3dc5269a131d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105814068"
---
# <a name="pxeproviderservicecontrol-callback-function"></a><span data-ttu-id="da23e-104">Função de retorno de chamada PxeProviderServiceControl</span><span class="sxs-lookup"><span data-stu-id="da23e-104">PxeProviderServiceControl callback function</span></span>

<span data-ttu-id="da23e-105">Chamado quando um código de controle de serviço é recebido pelo serviço WDS.</span><span class="sxs-lookup"><span data-stu-id="da23e-105">Called when a service control code is received by the WDS service.</span></span> <span data-ttu-id="da23e-106">Essa função de retorno de chamada é registrada chamando a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o parâmetro *CallbackType* definido como **\_ controle de serviço de retorno de chamada \_ \_ PXE**.</span><span class="sxs-lookup"><span data-stu-id="da23e-106">This callback function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SERVICE\_CONTROL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="da23e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da23e-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderServiceControl(
  _In_ PVOID pContext,
       DWORD dwControl
);
```



## <a name="parameters"></a><span data-ttu-id="da23e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da23e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da23e-109">*pContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da23e-109">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da23e-110">Valor de contexto passado para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="da23e-110">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> <dt>

<span data-ttu-id="da23e-111">*dwControl*</span><span class="sxs-lookup"><span data-stu-id="da23e-111">*dwControl*</span></span> 
</dt> <dd>

<span data-ttu-id="da23e-112">Código de controle.</span><span class="sxs-lookup"><span data-stu-id="da23e-112">Control code.</span></span> <span data-ttu-id="da23e-113">Para obter a lista de valores possíveis, consulte o parâmetro *dwControl* da função [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) .</span><span class="sxs-lookup"><span data-stu-id="da23e-113">For the list of possible values, see the *dwControl* parameter of the [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da23e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da23e-114">Return value</span></span>

<span data-ttu-id="da23e-115">Se o provedor for desligado com êxito, o retorno de chamada deverá retornar o **erro de \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="da23e-115">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="da23e-116">Em caso de falha, um código de erro apropriado deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="da23e-116">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="da23e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da23e-117">Requirements</span></span>



| <span data-ttu-id="da23e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="da23e-118">Requirement</span></span> | <span data-ttu-id="da23e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="da23e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da23e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da23e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da23e-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="da23e-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="da23e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da23e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da23e-123">Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="da23e-123">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da23e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="da23e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da23e-125">Funções de servidor dos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="da23e-125">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="da23e-126">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="da23e-126">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

