---
title: Bluetooth e WSASetService
description: O Bluetooth usa a função WSASetService para registrar ou remover uma instância de serviço no namespace do Bluetooth (NS \_ BTH) do registro.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth de Bluetooth
- WSASetService Bluetooth
- Bluetooth e Bluetooth WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454097"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="d26fe-106">Bluetooth e WSASetService</span><span class="sxs-lookup"><span data-stu-id="d26fe-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="d26fe-107">O Bluetooth usa a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar ou remover uma instância de serviço no namespace do Bluetooth (ns \_ BTH) do registro.</span><span class="sxs-lookup"><span data-stu-id="d26fe-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="d26fe-108">O identificador retornado por esta operação só pode ser usado para excluir o serviço.</span><span class="sxs-lookup"><span data-stu-id="d26fe-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="d26fe-109">O Bluetooth tem dois meios de anunciar serviços usando a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="d26fe-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="d26fe-110">O aplicativo pode fazer com que o sistema anuncie um registro de serviço SDP simples de Bluetooth, construído a partir de membros padrão na estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="d26fe-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="d26fe-111">O aplicativo pode fazer com que o sistema Anuncie seu próprio registro de SDP de Bluetooth passando uma estrutura de [**\_ \_ serviço BTH Set**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) no membro **lpBlob** da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="d26fe-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="d26fe-112">Essa é uma abordagem mais complexa.</span><span class="sxs-lookup"><span data-stu-id="d26fe-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="d26fe-113">Os registros SDP anunciados pelo [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) não persistem depois que o processo que o publicou foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="d26fe-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="d26fe-114">O uso de [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) com Bluetooth tem os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="d26fe-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="d26fe-115">O parâmetro *lpqsRegInfo* é o endereço da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="d26fe-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="d26fe-116">O parâmetro *essOperation* é uma enumeração que contém uma das operações mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d26fe-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="d26fe-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d26fe-117">Value</span></span>                  | <span data-ttu-id="d26fe-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d26fe-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d26fe-119">registro de RNRSERVICE \_</span><span class="sxs-lookup"><span data-stu-id="d26fe-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="d26fe-120">Começa a anunciar o serviço para a consulta de rádios remotos usando o protocolo de SDP Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d26fe-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="d26fe-121">RNRSERVICE \_ Cancelar registro</span><span class="sxs-lookup"><span data-stu-id="d26fe-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="d26fe-122">Inválido.</span><span class="sxs-lookup"><span data-stu-id="d26fe-122">Not valid.</span></span> <span data-ttu-id="d26fe-123">Retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="d26fe-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="d26fe-124">RNRSERVICE \_ excluir</span><span class="sxs-lookup"><span data-stu-id="d26fe-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="d26fe-125">Interrompe o anúncio do serviço.</span><span class="sxs-lookup"><span data-stu-id="d26fe-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="d26fe-126">Os identificadores de serviço descobertos durante uma chamada de [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) ou [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) são incompatíveis com a operação de exclusão de RNRSERVICE \_ .</span><span class="sxs-lookup"><span data-stu-id="d26fe-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="d26fe-127">O parâmetro *dwControlFlags* é reservado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d26fe-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="d26fe-128">Para obter mais informações e uma lista de opções de soquete Bluetooth, consulte [Opções de soquete e Bluetooth](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="d26fe-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d26fe-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d26fe-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d26fe-130">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d26fe-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 