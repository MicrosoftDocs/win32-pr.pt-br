---
title: Função de retorno de chamada PxeProviderInitialize
description: Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e a prepara para receber solicitações do cliente.
ms.assetid: 433b051c-9fde-4589-92e2-58d3774826ac
keywords:
- Função de retorno de chamada do PxeProviderInitialize serviços de implantação do Windows
topic_type:
- apiref
api_name:
- PxeProviderInitialize
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b8d8fed4c1cc91c2090b957894b4f6641adad32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796238"
---
# <a name="pxeproviderinitialize-callback-function"></a><span data-ttu-id="8eff4-104">Função de retorno de chamada PxeProviderInitialize</span><span class="sxs-lookup"><span data-stu-id="8eff4-104">PxeProviderInitialize callback function</span></span>

<span data-ttu-id="8eff4-105">Uma exportação de uma DLL (biblioteca de vínculo dinâmico) do provedor que inicializa o provedor e a prepara para receber solicitações do cliente.</span><span class="sxs-lookup"><span data-stu-id="8eff4-105">An export from a provider dynamic-link library (DLL) that initializes the provider and prepares it to receive client requests.</span></span> <span data-ttu-id="8eff4-106">Os provedores são necessários para exportar a função *PxeProviderInitialize* .</span><span class="sxs-lookup"><span data-stu-id="8eff4-106">Providers are required to export the *PxeProviderInitialize* function.</span></span> <span data-ttu-id="8eff4-107">Qualquer retorno de chamada para o provedor deve ser registrado com uma chamada para a função [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) durante o processamento de *PxeProviderInitialize*.</span><span class="sxs-lookup"><span data-stu-id="8eff4-107">Any callbacks to the provider must be registered with a call to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function during the processing of *PxeProviderInitialize*.</span></span> <span data-ttu-id="8eff4-108">No retorno dessa função, o provedor deve ser totalmente inicializado e estar pronto para processar solicitações de cliente.</span><span class="sxs-lookup"><span data-stu-id="8eff4-108">On the return of this function, the provider must be fully initialized and ready to process client requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eff4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8eff4-109">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderInitialize(
  _In_ HANDLE hProvider,
  _In_ HKEY   hProviderKey
);
```



## <a name="parameters"></a><span data-ttu-id="8eff4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8eff4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eff4-111">*hProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8eff4-111">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff4-112">Identificador para a instância do provedor.</span><span class="sxs-lookup"><span data-stu-id="8eff4-112">Handle to the provider instance.</span></span> <span data-ttu-id="8eff4-113">Esse identificador deve ser armazenado pelo provedor e usado em qualquer chamada subsequente.</span><span class="sxs-lookup"><span data-stu-id="8eff4-113">This handle must be stored by the provider and used in any subsequent calls.</span></span> <span data-ttu-id="8eff4-114">Esse identificador é válido até que a função de retorno de chamada [*PxeProviderShutdown*](pxeprovidershutdown.md) seja chamada.</span><span class="sxs-lookup"><span data-stu-id="8eff4-114">This handle is valid until the [*PxeProviderShutdown*](pxeprovidershutdown.md) callback function is called.</span></span>

</dd> <dt>

<span data-ttu-id="8eff4-115">*hProviderKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8eff4-115">*hProviderKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff4-116">Identificador para uma chave do registro onde as informações de configuração do provedor serão armazenadas.</span><span class="sxs-lookup"><span data-stu-id="8eff4-116">Handle to a registry key where provider configuration information is to be stored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eff4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8eff4-117">Return value</span></span>

<span data-ttu-id="8eff4-118">Se a inicialização do provedor for bem-sucedida, o retorno de chamada deverá retornar o **erro de \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="8eff4-118">If the provider initialization succeeds, the callback should return **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="8eff4-119">Em caso de falha, um código de erro apropriado deve ser retornado.</span><span class="sxs-lookup"><span data-stu-id="8eff4-119">In case of failure, an appropriate error code should be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eff4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8eff4-120">Requirements</span></span>



| <span data-ttu-id="8eff4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eff4-121">Requirement</span></span> | <span data-ttu-id="8eff4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8eff4-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8eff4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eff4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8eff4-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8eff4-124">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8eff4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8eff4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8eff4-126">Windows Server 2008, Windows Server 2003 com aplicativos de área de trabalho do SP2 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="8eff4-126">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8eff4-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8eff4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eff4-128">Funções de servidor dos serviços de implantação do Windows</span><span class="sxs-lookup"><span data-stu-id="8eff4-128">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="8eff4-129">*PxeProviderShutdown*</span><span class="sxs-lookup"><span data-stu-id="8eff4-129">*PxeProviderShutdown*</span></span>](pxeprovidershutdown.md)
</dt> </dl>

 

 





