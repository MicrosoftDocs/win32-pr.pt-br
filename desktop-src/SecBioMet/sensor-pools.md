---
title: Pools de sensores
description: Descreve três possíveis pools de sensor, privado e não atribuído.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366250"
---
# <a name="sensor-pools"></a><span data-ttu-id="52f2c-103">Pools de sensores</span><span class="sxs-lookup"><span data-stu-id="52f2c-103">Sensor Pools</span></span>

<span data-ttu-id="52f2c-104">Para dar suporte aos cenários de autenticação do Windows e à autenticação definida pelo fornecedor, o serviço de biometria do Windows organiza as unidades biométricas em três pools de sensores possíveis:</span><span class="sxs-lookup"><span data-stu-id="52f2c-104">To support both Windows authentication scenarios and vendor defined authentication, the Windows Biometric service organizes biometric units into three possible sensor pools:</span></span>

-   <span data-ttu-id="52f2c-105">**Pool privado** uma coleção de unidades biométricas alocadas para uso exclusivo por um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="52f2c-105">**Private pool** a collection of biometric units allocated for exclusive use by a client application.</span></span> <span data-ttu-id="52f2c-106">Os pools privados podem dar suporte a cenários de autenticação que não são baseados no Windows e possibilitam que um aplicativo acesse o hardware de uma unidade biométrica de uma maneira definida pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="52f2c-106">Private pools can support authentication scenarios that are not Windows-based, and they make it possible for an application to access the hardware of a biometric unit in a vendor-defined fashion.</span></span> <span data-ttu-id="52f2c-107">Pode haver tantos pools de sensores privados no sistema quanto há unidades biométricas.</span><span class="sxs-lookup"><span data-stu-id="52f2c-107">There can be as many private sensor pools on the system as there are biometric units.</span></span>
-   <span data-ttu-id="52f2c-108">**Pool do sensor do sistema** uma coleção de unidades biométricas compartilháveis que fornecem acesso aos serviços de autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="52f2c-108">**System sensor pool** a collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="52f2c-109">Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associa um SID a um modelo biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="52f2c-109">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span> <span data-ttu-id="52f2c-110">Cada provedor de serviços biométricos tem um pool de sensor do sistema.</span><span class="sxs-lookup"><span data-stu-id="52f2c-110">Each biometric service provider has one system sensor pool.</span></span>
-   <span data-ttu-id="52f2c-111">O **pool não atribuído** contém uma coleção (possivelmente vazia) de unidades biométricas que não são atribuídas ao pool do sistema ou ao pool privado.</span><span class="sxs-lookup"><span data-stu-id="52f2c-111">**Unassigned pool** contains a (possibly empty) collection of biometric units that are not assigned to either the system pool or the private pool.</span></span>

<span data-ttu-id="52f2c-112">Os aplicativos podem usar o pool de sistema compartilhado ou podem criar um pool privado composto por unidades biométricas removidas do sistema ou de pools não atribuídos.</span><span class="sxs-lookup"><span data-stu-id="52f2c-112">Applications can use the shared system pool or they can create a private pool made up of biometric units removed from the system or unassigned pools.</span></span> <span data-ttu-id="52f2c-113">Quando um aplicativo libera seu pool particular, as unidades biométricas são reconfiguradas e retornadas para seus pools originais.</span><span class="sxs-lookup"><span data-stu-id="52f2c-113">When an application releases its private pool, the biometric units are reconfigured and returned to their original pools.</span></span> <span data-ttu-id="52f2c-114">Para evitar ataques de negação de serviço, somente usuários privilegiados têm permissão para remover o último sensor do pool do sistema.</span><span class="sxs-lookup"><span data-stu-id="52f2c-114">To prevent denial of service attacks, only privileged users are permitted to remove the last sensor from the system pool.</span></span> <span data-ttu-id="52f2c-115">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="52f2c-115">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="52f2c-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="52f2c-116">In this section</span></span>



| <span data-ttu-id="52f2c-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="52f2c-117">Topic</span></span>                                                       | <span data-ttu-id="52f2c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="52f2c-118">Description</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52f2c-119">Pool de sensores privado</span><span class="sxs-lookup"><span data-stu-id="52f2c-119">Private Sensor Pool</span></span>](private-sensor-pool.md)<br/>   | <span data-ttu-id="52f2c-120">Uma coleção de unidades biométricas reservadas para uso exclusivo por um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="52f2c-120">A collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="52f2c-121">Os pools privados dão suporte a métodos de autenticação proprietários e permitem que um aplicativo cliente acesse uma unidade biométrica usando comandos de controle especificados pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="52f2c-121">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span><br/> |
| [<span data-ttu-id="52f2c-122">Pool do sensor do sistema</span><span class="sxs-lookup"><span data-stu-id="52f2c-122">System Sensor Pool</span></span>](system-sensor-pool.md)<br/>     | <span data-ttu-id="52f2c-123">Uma coleção de unidades biométricas compartilhadas que fornecem acesso aos serviços de autenticação do Windows.</span><span class="sxs-lookup"><span data-stu-id="52f2c-123">A collection of sharable biometric units that provide access to Windows authentication services.</span></span> <span data-ttu-id="52f2c-124">Esse pool é usado pelo Winlogon, pelo UAC e por qualquer outro cliente que associa um SID a um modelo biométrico específico.</span><span class="sxs-lookup"><span data-stu-id="52f2c-124">This pool is used by Winlogon, UAC, and any other client that associates a SID with a specific biometric template.</span></span><br/>                                 |
| [<span data-ttu-id="52f2c-125">Comportamento do pool do sistema</span><span class="sxs-lookup"><span data-stu-id="52f2c-125">System Pool Behavior</span></span>](system-pool-behavior.md)<br/> | <span data-ttu-id="52f2c-126">Discussão sobre as ações executadas pelo pool do sistema quando avisos de evento são enviados e quando nenhuma operação biométrica está pendente.</span><span class="sxs-lookup"><span data-stu-id="52f2c-126">Discussion about the actions taken by the system pool when event notices are sent and when no biometric operations are pending.</span></span><br/>                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="52f2c-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52f2c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52f2c-128">Sobre a API de Windows Biometric Framework</span><span class="sxs-lookup"><span data-stu-id="52f2c-128">About the Windows Biometric Framework API</span></span>](./biometric-service-api-portal.md)
</dt> </dl>

 

