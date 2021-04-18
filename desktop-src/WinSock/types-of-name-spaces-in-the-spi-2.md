---
description: Os três tipos de namespaces no SPI do Windows Sockets (Winsock) incluem namespaces dinâmicos, estáticos e persistentes.
ms.assetid: 2968ac98-bd40-4d37-9dd7-7870c4decd40
title: Tipos de namespaces no SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e40356987c67604755696f1a8b7224de15851ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810647"
---
# <a name="types-of-namespaces-in-the-spi"></a><span data-ttu-id="1ac16-103">Tipos de namespaces no SPI</span><span class="sxs-lookup"><span data-stu-id="1ac16-103">Types of Namespaces in the SPI</span></span>

<span data-ttu-id="1ac16-104">Há três tipos diferentes de namespaces nos quais um serviço pode ser registrado:</span><span class="sxs-lookup"><span data-stu-id="1ac16-104">There are three different types of namespaces in which a service could be registered:</span></span>

-   <span data-ttu-id="1ac16-105">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="1ac16-105">Dynamic</span></span>
-   <span data-ttu-id="1ac16-106">Estático</span><span class="sxs-lookup"><span data-stu-id="1ac16-106">Static</span></span>
-   <span data-ttu-id="1ac16-107">Persistente</span><span class="sxs-lookup"><span data-stu-id="1ac16-107">Persistent</span></span>

<span data-ttu-id="1ac16-108">Os namespaces dinâmicos permitem que os serviços se registrem com o namespace imediatamente e para que os clientes descubram os serviços disponíveis em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1ac16-108">Dynamic namespaces allow services to register with the namespace on the fly, and for clients to discover the available services at run time.</span></span> <span data-ttu-id="1ac16-109">Os namespaces dinâmicos frequentemente dependem de difusões para indicar a disponibilidade contínua de um serviço de rede.</span><span class="sxs-lookup"><span data-stu-id="1ac16-109">Dynamic namespaces frequently rely on broadcasts to indicate the continued availability of a network service.</span></span> <span data-ttu-id="1ac16-110">Exemplos de namespaces dinâmicos incluem o namespace SAP usado em um ambiente NetWare e o namespace NBP usado pelo AppleTalk.</span><span class="sxs-lookup"><span data-stu-id="1ac16-110">Examples of dynamic namespaces include the SAP namespace used within a NetWare environment and the NBP namespace used by AppleTalk.</span></span>

<span data-ttu-id="1ac16-111">Os namespaces estáticos exigem que todos os serviços sejam registrados antecipadamente, ou seja, quando o namespace é criado.</span><span class="sxs-lookup"><span data-stu-id="1ac16-111">Static namespaces require all of the services to be registered ahead of time, that is, when the namespace is created.</span></span> <span data-ttu-id="1ac16-112">O DNS é um exemplo de um namespace estático.</span><span class="sxs-lookup"><span data-stu-id="1ac16-112">The DNS is an example of a static namespace.</span></span> <span data-ttu-id="1ac16-113">Embora haja uma maneira programática de resolver nomes, não há uma maneira programática de registrar nomes.</span><span class="sxs-lookup"><span data-stu-id="1ac16-113">Although there is a programmatic way to resolve names, there is no programmatic way to register names.</span></span>

<span data-ttu-id="1ac16-114">Namespaces persistentes permitem que os serviços se registrem com o namespace em tempo real.</span><span class="sxs-lookup"><span data-stu-id="1ac16-114">Persistent namespaces allow services to register with the namespace on the fly.</span></span> <span data-ttu-id="1ac16-115">Ao contrário dos namespaces dinâmicos, no entanto, os namespaces persistentes retêm as informações de registro no armazenamento não volátil onde permanecem até o momento em que as solicitações de serviço são removidas.</span><span class="sxs-lookup"><span data-stu-id="1ac16-115">Unlike dynamic namespaces however, persistent namespaces retain the registration information in nonvolatile storage where it remains until such time as the service requests that it be removed.</span></span> <span data-ttu-id="1ac16-116">Os namespaces persistentes são Typified por serviços de diretório, como X. 500 e o NDS (serviço de diretório do NetWare).</span><span class="sxs-lookup"><span data-stu-id="1ac16-116">Persistent namespaces are typified by directory services such as X.500 and the NDS (NetWare Directory Service).</span></span> <span data-ttu-id="1ac16-117">Esses ambientes permitem a adição, exclusão e modificação de propriedades de serviço.</span><span class="sxs-lookup"><span data-stu-id="1ac16-117">These environments allow the adding, deleting, and modification of service properties.</span></span> <span data-ttu-id="1ac16-118">Além disso, o objeto de serviço que representa o serviço no serviço de diretório pode ter uma variedade de atributos associados ao serviço.</span><span class="sxs-lookup"><span data-stu-id="1ac16-118">In addition, the service object representing the service within the directory service could have a variety of attributes associated with the service.</span></span> <span data-ttu-id="1ac16-119">O atributo mais importante para aplicativos cliente são as informações de endereçamento do serviço.</span><span class="sxs-lookup"><span data-stu-id="1ac16-119">The most important attribute for client applications is the service's addressing information.</span></span>

 

 



