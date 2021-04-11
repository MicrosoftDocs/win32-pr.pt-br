---
description: Usando o CRM do COM+ em um ambiente de cluster
ms.assetid: 753461c5-880c-4df0-b552-b962dc06524f
title: Usando o CRM do COM+ em um ambiente de cluster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a05ff281748c35128349ef5d0d0f43d7beae86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296097"
---
# <a name="using-the-com-crm-in-a-cluster-environment"></a><span data-ttu-id="dd474-103">Usando o CRM do COM+ em um ambiente de cluster</span><span class="sxs-lookup"><span data-stu-id="dd474-103">Using the COM+ CRM in a Cluster Environment</span></span>

<span data-ttu-id="dd474-104">Ao desenvolver o CRMs do COM+ para trabalhar em ambientes de cluster, o principal fator a ser considerado é se um CRM específico se preocupa com o nó do cluster em que ele está operando.</span><span class="sxs-lookup"><span data-stu-id="dd474-104">When developing COM+ CRMs to work in cluster environments, the main factor to consider is whether a specific CRM cares which node of the cluster it is operating on.</span></span> <span data-ttu-id="dd474-105">Por exemplo, se o recurso gerenciado pelo CRM for o sistema de arquivos da máquina ou o registro, todas as alterações serão específicas para o nó em que o aplicativo do servidor do CRM está sendo executado no momento.</span><span class="sxs-lookup"><span data-stu-id="dd474-105">For example, if the resource managed by the CRM is the machine file system or registry, any changes are specific to the node that the CRM server application is running on at the time.</span></span> <span data-ttu-id="dd474-106">Nesse caso, o failover do aplicativo do servidor do CRM para outro nó não seria desejável.</span><span class="sxs-lookup"><span data-stu-id="dd474-106">In this case, failover of the CRM server application to another node would not be desirable.</span></span> <span data-ttu-id="dd474-107">Em um caso diferente, em que o CRM está gerenciando algum recurso comum ao cluster, o failover do aplicativo do servidor do CRM para outro nó é útil.</span><span class="sxs-lookup"><span data-stu-id="dd474-107">In a different case, where the CRM is managing some resource common to the cluster, failover of the CRM server application to another node is useful.</span></span>

<span data-ttu-id="dd474-108">O local do diretório padrão para os arquivos de log do CRM é o mesmo diretório do arquivo de log do DTC.</span><span class="sxs-lookup"><span data-stu-id="dd474-108">The default directory location for CRM log files is the same directory as the DTC log file.</span></span> <span data-ttu-id="dd474-109">Em clusters, o arquivo de log do DTC é colocado em um disco compartilhado que faz failover entre os nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="dd474-109">On clusters, the DTC log file is placed on a shared disk that is failed over between the nodes of the cluster.</span></span> <span data-ttu-id="dd474-110">Isso significa que o comportamento padrão para aplicativos do servidor CRM é fazer failover entre os nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="dd474-110">This means that the default behavior for CRM server applications is to failover between nodes of the cluster.</span></span> <span data-ttu-id="dd474-111">Portanto, se um CRM específico exigir o comportamento alternativo de não fazer failover entre os nós, o local do arquivo de log do CRM para esse aplicativo de servidor CRM específico deverá ser alterado.</span><span class="sxs-lookup"><span data-stu-id="dd474-111">Therefore, if a specific CRM requires the alternative behavior of not failing over between nodes, the location of the CRM log file for that particular CRM server application should be changed.</span></span>

<span data-ttu-id="dd474-112">Além disso, se o failover for necessário para o aplicativo CRM, ele deverá ser configurado como um aplicativo genérico em um grupo de clusters.</span><span class="sxs-lookup"><span data-stu-id="dd474-112">In addition, if failover is required for the CRM application, it should be configured as a generic application in a cluster group.</span></span> <span data-ttu-id="dd474-113">Sua dependência deve ser DTC.</span><span class="sxs-lookup"><span data-stu-id="dd474-113">Its dependency should be DTC.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd474-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd474-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd474-115">Conceitos do Gerenciador de recursos de compensação COM+</span><span class="sxs-lookup"><span data-stu-id="dd474-115">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



