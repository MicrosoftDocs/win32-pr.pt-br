---
title: Referência da API EAPHost
description: Saiba mais sobre as APIs do EAPHost e seus componentes. Consulte informações de referência para vários tópicos de API, como o esquema XML do EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366696"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="b7758-104">Referência da API EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-104">EAPHost API Reference</span></span>

<span data-ttu-id="b7758-105">As APIs do EAPHost são divididas em três componentes: as APIs do suplicante, que podem ser chamadas diretamente de um aplicativo habilitado para EAP; as APIs do método EAP peer, que gerenciam solicitações suplicantes para um tipo de autenticação EAP específico e geram elementos interativos no cliente; e as APIS do autenticador EAP, que executam a autenticação do lado do servidor de um suplicante.</span><span class="sxs-lookup"><span data-stu-id="b7758-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="b7758-106">Os dois últimos componentes de API – o método EAP peer e as APIs do método de autenticador EAP – exigem implementação personalizada e compatível em DLLs que os expõem ao serviço EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="b7758-107">Eles não podem ser chamados diretamente do código do aplicativo; em vez disso, eles são chamados pelo EAPHost (no lado do cliente para métodos de ponto EAP e no lado do servidor para métodos de autenticador EAP) se a implementação corresponder às assinaturas de API especificadas na documentação correspondente.</span><span class="sxs-lookup"><span data-stu-id="b7758-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="b7758-108">Informações específicas de implementação de API são fornecidas em cada página de referência de função.</span><span class="sxs-lookup"><span data-stu-id="b7758-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="b7758-109">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="b7758-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="b7758-110">Topic</span></span>                                                      | <span data-ttu-id="b7758-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7758-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="b7758-112">Configurações do registro EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="b7758-113">Descreve as chaves do registro consumidas pelo EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="b7758-114">Esquema XML do EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="b7758-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="b7758-115">Topic</span></span>                                            | <span data-ttu-id="b7758-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7758-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7758-117">EAPHost e esquema herdado</span><span class="sxs-lookup"><span data-stu-id="b7758-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="b7758-118">Descreve o esquema EAPHost e o esquema herdado para criar o XML de configuração e a credencial XML.</span><span class="sxs-lookup"><span data-stu-id="b7758-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="b7758-119">Referência de API do EAPHost comum</span><span class="sxs-lookup"><span data-stu-id="b7758-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="b7758-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="b7758-120">Topic</span></span>                                                                   | <span data-ttu-id="b7758-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7758-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="b7758-122">Enumerações comuns da API EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="b7758-123">Lista as constantes comuns a todas as APIs do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="b7758-124">Estruturas comuns de API do EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="b7758-125">Lista estruturas comuns a todas as APIs do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="b7758-126">Constantes comuns da API EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="b7758-127">Lista as constantes comuns a todas as APIs do EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="b7758-128">Referência da API EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-128">EAPHost API Reference</span></span>



| <span data-ttu-id="b7758-129">Tópico</span><span class="sxs-lookup"><span data-stu-id="b7758-129">Topic</span></span>                                                                       | <span data-ttu-id="b7758-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7758-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7758-131">Referência de API do suplicante EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="b7758-132">Descreve os elementos de API disponíveis para habilitar chamadas de suplicante para EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="b7758-133">Referência da API do método par do EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="b7758-134">Descreve os elementos de API que devem ser implementados para criar uma DLL de método EAP peer que pode ser carregada e chamada por um cliente EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="b7758-135">APIs do método de autenticador EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="b7758-136">Descreve os elementos de API que devem ser implementados para criar uma DLL de método de autenticador EAP que pode ser carregada e chamada por um servidor EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b7758-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b7758-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7758-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7758-138">Sobre o EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="b7758-139">Usando o EAPHost</span><span class="sxs-lookup"><span data-stu-id="b7758-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




