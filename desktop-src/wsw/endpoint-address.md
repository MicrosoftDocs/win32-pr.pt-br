---
title: Endereço de ponto de extremidade
description: Um endereço de ponto de extremidade representa o endereço de um serviço na rede.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Endereço do ponto de extremidade serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104561605"
---
# <a name="endpoint-address"></a><span data-ttu-id="eb9d7-106">Endereço de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="eb9d7-106">Endpoint Address</span></span>

<span data-ttu-id="eb9d7-107">Um endereço de ponto de extremidade representa o endereço de um serviço na rede.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-107">An endpoint address represents the address of a service on the network.</span></span> <span data-ttu-id="eb9d7-108">Ao abrir um [canal](channel.md), chamando a função [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , você precisa fornecer o endereço do ponto de extremidade do serviço com o qual deseja se comunicar, bem como especificar o canal que você deseja abrir.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-108">When you open a [channel](channel.md), by calling the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) function, you need to provide the endpoint address of the service you which to communicate with, as well as specifying the channel you wish to open.</span></span>


<span data-ttu-id="eb9d7-109">Um endereço de ponto de extremidade consiste em:</span><span class="sxs-lookup"><span data-stu-id="eb9d7-109">An endpoint address consists of:</span></span>

-   <span data-ttu-id="eb9d7-110">uma [URL](url.md)</span><span class="sxs-lookup"><span data-stu-id="eb9d7-110">a [URL](url.md)</span></span>
-   <span data-ttu-id="eb9d7-111">um conjunto de cabeçalhos (opcional)</span><span class="sxs-lookup"><span data-stu-id="eb9d7-111">a set of headers (optional)</span></span>
-   <span data-ttu-id="eb9d7-112">um conjunto de extensões (opcional)</span><span class="sxs-lookup"><span data-stu-id="eb9d7-112">a set of extensions (optional)</span></span>
-   <span data-ttu-id="eb9d7-113">uma [identidade](endpoint-identity.md) opcional que representa a identidade de segurança do serviço.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-113">an optional [identity](endpoint-identity.md) representing the security identity of the service.</span></span>

<span data-ttu-id="eb9d7-114">Quando uma mensagem é endereçada, a URL se torna o cabeçalho "para" da mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-114">When a message is addressed, the URL becomes the "To" header of the message.</span></span> <span data-ttu-id="eb9d7-115">Todos os cabeçalhos que fazem parte do endereço do ponto de extremidade também são adicionados à mensagem.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-115">Any headers that are part of the endpoint address are also added to the message.</span></span>

![Diagrama mostrando cabeçalhos de endereço do ponto de extremidade que estão sendo adicionados a uma mensagem.](images/endpointaddress.png)

<span data-ttu-id="eb9d7-117">Os canais abordam automaticamente todas as mensagens que são enviadas, usando a estrutura de [**\_ \_ endereço do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que foi passada para o [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span><span class="sxs-lookup"><span data-stu-id="eb9d7-117">Channels automatically address any messages that are sent, using the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure that was passed to the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel).</span></span> <span data-ttu-id="eb9d7-118">Você também pode usar a função [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) para substituir esse comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-118">You can also use the [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) function to override this default behavior.</span></span>

<span data-ttu-id="eb9d7-119">Quando [**o \_ \_ endereço do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) é passado como um parâmetro, as funções [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) e [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) criam uma cópia do parâmetro de **\_ \_ endereço do ponto de extremidade WS** na memória e seu tamanho é limitado por 65536 bytes.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-119">When [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) is passed as a parameter, the [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) and [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) functions create a copy of the **WS\_ENDPOINT\_ADDRESS** parameter in memory and its size is limited by 65536 bytes.</span></span> <span data-ttu-id="eb9d7-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) não tem essa limitação porque não requer a criação de uma cópia do parâmetro de **\_ \_ endereço de ponto de extremidade WS** .</span><span class="sxs-lookup"><span data-stu-id="eb9d7-120">[**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) does not have this limitation because it does not require creating a copy of the **WS\_ENDPOINT\_ADDRESS** parameter.</span></span>

<span data-ttu-id="eb9d7-121">As extensões especificadas no campo **extensões** do [**endereço do \_ ponto \_ de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) não são usadas para tratar a mensagem, mas sim um mecanismo de extensibilidade que pode ser usado para fornecer informações adicionais (por exemplo, metadados) sobre o serviço.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-121">The extensions specified in the **extensions** field of [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) are not used for addressing the message but instead are an extensibility mechanism that can be used to provide additional information (for example, metadata) about the service.</span></span> <span data-ttu-id="eb9d7-122">Extensões comuns podem ser lidas com a função [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .</span><span class="sxs-lookup"><span data-stu-id="eb9d7-122">Common extensions can be read with the [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) function.</span></span>

<span data-ttu-id="eb9d7-123">O campo de identidade opcional do endereço do ponto de extremidade pode incluir, por exemplo, o nome DNS do computador no qual o serviço está em execução ou o UPN da conta do Windows na qual o serviço está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="eb9d7-123">The optional identity field of the endpoint address can include, for example, the DNS name of the machine on which the service is running, or the UPN of the Windows account under which the service is running.</span></span> <span data-ttu-id="eb9d7-124">O campo de identidade não é usado para endereçar a mensagem, mas pode ser usado para obter um token de segurança para o serviço (por exemplo, para obter um tíquete Kerberos para o UPN de destino) e para verificar a identidade das respostas de serviço (por exemplo, uma identidade DNS usada para verificações de nome no certificado de serviço retornado durante o SSL).</span><span class="sxs-lookup"><span data-stu-id="eb9d7-124">The identity field is not used in addressing the message, but may be used for obtaining a security token for the service (for example, for obtaining a Kerberos ticket to the target UPN) and for verifying the identity of the service replies (for example, a DNS identity used for name checks on the service certificate returned during SSL).</span></span>

<span data-ttu-id="eb9d7-125">Os endereços de ponto de extremidade podem ser lidos e gravados usando a [serialização](serialization.md) com o valor de enumeração do **tipo de endereço de ponto de \_ extremidade \_ \_ WS** do [**\_ tipo**](/windows/desktop/api/WebServices/ne-webservices-ws_type)</span><span class="sxs-lookup"><span data-stu-id="eb9d7-125">Endpoint addresses can be read and written using [serialization](serialization.md) with the **WS\_ENDPOINT\_ADDRESS\_TYPE** enumeration value from [**WS\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type).</span></span> <span data-ttu-id="eb9d7-126">Observação para serializar um endereço de ponto de extremidade, você deve saber a versão da especificação usada para os cabeçalhos de endereçamento, conforme especificado na enumeração da [**\_ \_ versão de endereçamento do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .</span><span class="sxs-lookup"><span data-stu-id="eb9d7-126">Note in order to serialize an endpoint address, you must know the version of the specification used for the addressing headers, as specified in the [**WS\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) enumeration.</span></span>

 

 




