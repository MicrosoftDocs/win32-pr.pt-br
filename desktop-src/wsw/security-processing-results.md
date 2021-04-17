---
title: Resultados do processamento de segurança
description: Em um canal seguro, somente as mensagens que passam com êxito pelas verificações de segurança são entregues ao aplicativo.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Resultados de processamento de segurança Web Services para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105797901"
---
# <a name="security-processing-results"></a><span data-ttu-id="90080-106">Resultados do processamento de segurança</span><span class="sxs-lookup"><span data-stu-id="90080-106">Security Processing Results</span></span>

<span data-ttu-id="90080-107">Em um canal seguro, somente as mensagens que passam com êxito pelas verificações de segurança são entregues ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="90080-107">On a secure channel, only those messages that successfully pass security checks are delivered to the application.</span></span> <span data-ttu-id="90080-108">Para essas mensagens, alguns resultados da verificação de segurança são anexados como propriedades de mensagem, e o aplicativo pode extrair e examinar essas propriedades para executar etapas adicionais, como verificações de autorização.</span><span class="sxs-lookup"><span data-stu-id="90080-108">For these messages, some results from security verification are attached as message properties, and the application may extract and examine these properties to perform additional steps such as authorization checks.</span></span>


<span data-ttu-id="90080-109">A função [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) pode ser usada para recuperar qualquer uma das propriedades relacionadas à segurança definidas na [**\_ ID da \_ propriedade \_ da mensagem do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span><span class="sxs-lookup"><span data-stu-id="90080-109">The function [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) can be used to retrieve any of the security-related properties defined in [**WS\_MESSAGE\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id).</span></span> <span data-ttu-id="90080-110">**WsGetMessageProperty** retorna um erro para consultas que solicitam Propriedades de segurança não aplicáveis ao tipo de segurança usado no canal.</span><span class="sxs-lookup"><span data-stu-id="90080-110">**WsGetMessageProperty** returns an error for queries that ask for security properties not applicable to the type of security used on the channel.</span></span> <span data-ttu-id="90080-111">A mensagem continua a possuir as propriedades retornadas pela função de consulta.</span><span class="sxs-lookup"><span data-stu-id="90080-111">The message continues to own the properties returned by the query function.</span></span>

<span data-ttu-id="90080-112">Os seguintes elementos de API são usados com resultados de processamento de segurança.</span><span class="sxs-lookup"><span data-stu-id="90080-112">The following API elements are used with security processing results.</span></span>

| <span data-ttu-id="90080-113">Enumeração</span><span class="sxs-lookup"><span data-stu-id="90080-113">Enumeration</span></span>                                                                | <span data-ttu-id="90080-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="90080-114">Description</span></span>                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90080-115">**\_ID da \_ Propriedade do token de segurança do WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="90080-115">**WS\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | <span data-ttu-id="90080-116">Define as chaves para os campos e propriedades que podem ser extraídas de um token de segurança.</span><span class="sxs-lookup"><span data-stu-id="90080-116">Defines the keys for the fields and properties that can be extracted from a security token.</span></span> |



 



| <span data-ttu-id="90080-117">Função</span><span class="sxs-lookup"><span data-stu-id="90080-117">Function</span></span>                                                         | <span data-ttu-id="90080-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="90080-118">Description</span></span>                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="90080-119">**WsGetSecurityTokenProperty**</span><span class="sxs-lookup"><span data-stu-id="90080-119">**WsGetSecurityTokenProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | <span data-ttu-id="90080-120">Extrai um campo ou uma propriedade de um token de segurança.</span><span class="sxs-lookup"><span data-stu-id="90080-120">Extracts a field or a property from a security token.</span></span> |



 



| <span data-ttu-id="90080-121">Handle</span><span class="sxs-lookup"><span data-stu-id="90080-121">Handle</span></span>                                       | <span data-ttu-id="90080-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="90080-122">Description</span></span>                                     |
|----------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="90080-123">\_token de segurança do WS \_</span><span class="sxs-lookup"><span data-stu-id="90080-123">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md) | <span data-ttu-id="90080-124">Um identificador opaco que representa um token de segurança.</span><span class="sxs-lookup"><span data-stu-id="90080-124">An opaque handle representing a security token.</span></span> |



 

 

 




