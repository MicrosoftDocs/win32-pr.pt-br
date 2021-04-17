---
title: Função de retorno de chamada PxeProviderShutdown
description: Chamado para desligar o provedor.
ms.assetid: 436d7428-18f9-4b73-b346-79c9a0738c31
keywords:
- Função de retorno de chamada do PxeProviderShutdown serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderShutdown
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17698c5fa1f6ce6bd5443d0244ebc6ce6082ec33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762372"
---
# <a name="pxeprovidershutdown-callback-function"></a><span data-ttu-id="7975f-104">Função de retorno de chamada PxeProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="7975f-104">PxeProviderShutdown callback function</span></span>

<span data-ttu-id="7975f-105">Chamado para desligar o provedor.</span><span class="sxs-lookup"><span data-stu-id="7975f-105">Called to shutdown the provider.</span></span> <span data-ttu-id="7975f-106">Essa função é registrada chamando a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) com o parâmetro *CallbackType* definido como **\_ \_ desligamento de retorno de chamada PXE**.</span><span class="sxs-lookup"><span data-stu-id="7975f-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_SHUTDOWN**.</span></span> <span data-ttu-id="7975f-107">Depois que essa função é chamada, o identificador *hProvider* passado para a função [*PxeProviderInitialize*](pxeproviderinitialize.md) não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="7975f-107">After this function is called, the *hProvider* handle passed to the [*PxeProviderInitialize*](pxeproviderinitialize.md) function is no longer valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="7975f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7975f-108">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderShutdown(
  _In_ PVOID pContext
);
```



## <a name="parameters"></a><span data-ttu-id="7975f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7975f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7975f-110">*pContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7975f-110">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7975f-111">Valor de contexto passado para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="7975f-111">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7975f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7975f-112">Return value</span></span>

<span data-ttu-id="7975f-113">Se o provedor for desligado com êxito, o retorno de chamada deverá retornar o **erro de \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="7975f-113">If the provider shutdown succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="7975f-114">Em caso de falha, um código de erro apropriado deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="7975f-114">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7975f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7975f-115">Requirements</span></span>



| <span data-ttu-id="7975f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7975f-116">Requirement</span></span> | <span data-ttu-id="7975f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7975f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7975f-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7975f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7975f-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7975f-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="7975f-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7975f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7975f-121">Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="7975f-121">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7975f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7975f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7975f-123">Funções de servidor dos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="7975f-123">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="7975f-124">*PxeProviderInitialize*</span><span class="sxs-lookup"><span data-stu-id="7975f-124">*PxeProviderInitialize*</span></span>](pxeproviderinitialize.md)
</dt> <dt>

[<span data-ttu-id="7975f-125">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="7975f-125">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> </dl>

 

 





