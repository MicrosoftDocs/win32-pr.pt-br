---
description: Registrando e cancelando o registro de chaves
ms.assetid: 90fd8df0-e2a8-4183-a50c-e6f8ea5041cc
title: Registrando e cancelando o registro de chaves
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009ee41e85027ff8eba3f6869359a9ba304f4242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753111"
---
# <a name="registering-and-deregistering-keys"></a><span data-ttu-id="97ce5-103">Registrando e cancelando o registro de chaves</span><span class="sxs-lookup"><span data-stu-id="97ce5-103">Registering and Deregistering Keys</span></span>

## <a name="registering-keys"></a><span data-ttu-id="97ce5-104">Registrando chaves</span><span class="sxs-lookup"><span data-stu-id="97ce5-104">Registering Keys</span></span>

<span data-ttu-id="97ce5-105">Um nó pode registrar chaves com [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) a qualquer momento enquanto nos Estados de rede **DRT \_ ativa**, **DRT \_ sozinha** e **DRT \_ não \_** .</span><span class="sxs-lookup"><span data-stu-id="97ce5-105">A node can register keys with [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) at anytime while in the **DRT\_ACTIVE**, **DRT\_ALONE**, and **DRT\_NO\_NETWORK** states.</span></span> <span data-ttu-id="97ce5-106">Chaves registradas em **DRT \_ sozinha** e **DRT nenhum estado de \_ \_ rede** só pode ser reconhecido por outros DRTs depois que o nó local tiver feito a transição para a **DRT \_ ativa**.</span><span class="sxs-lookup"><span data-stu-id="97ce5-106">Keys registered in **DRT\_ALONE** and **DRT\_NO\_NETWORK** states can only be recognized by other DRTs after the local node has transitioned to **DRT\_ACTIVE**.</span></span>

<span data-ttu-id="97ce5-107">Chaves idênticas não podem ser registradas na mesma instância de DRT ao usar [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span><span class="sxs-lookup"><span data-stu-id="97ce5-107">Identical keys cannot be registered within the same DRT instance when using [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider).</span></span> <span data-ttu-id="97ce5-108">Se o registro de chaves idênticas for tentado, o registro da segunda chave falhará.</span><span class="sxs-lookup"><span data-stu-id="97ce5-108">If the registration of identical keys is attempted, the registration of the second key will fail.</span></span> <span data-ttu-id="97ce5-109">O uso de chaves idênticas também deve ser evitado entre diferentes instâncias de DRT.</span><span class="sxs-lookup"><span data-stu-id="97ce5-109">The use of identical keys should also be avoided between different DRT instances.</span></span> <span data-ttu-id="97ce5-110">Pesquisa na designação de chave exclusiva essas chaves idênticas compartilhadas podem retornar qualquer uma das chaves, independentemente de quais dados estão associados à chave.</span><span class="sxs-lookup"><span data-stu-id="97ce5-110">Searches against the unique key designation these identical keys share could return any one of the keys, regardless of what data is associated to the key.</span></span>

> [!Note]  
> <span data-ttu-id="97ce5-111">Se um comportamento diferente for necessário para a implementação, um provedor de segurança poderá ser criado no lugar do [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) para acomodar.</span><span class="sxs-lookup"><span data-stu-id="97ce5-111">If different behavior is required for implementation, a security provider can be created in place of [**DrtCreateDerivedKeySecurityProvider**](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) to accommodate.</span></span>

 

## <a name="deregistering-keys"></a><span data-ttu-id="97ce5-112">Cancelando o registro de chaves</span><span class="sxs-lookup"><span data-stu-id="97ce5-112">Deregistering Keys</span></span>

<span data-ttu-id="97ce5-113">Um nó pode cancelar o registro de uma chave a qualquer momento depois de ser registrado.</span><span class="sxs-lookup"><span data-stu-id="97ce5-113">A node can deregister a key anytime after it has been registered.</span></span> <span data-ttu-id="97ce5-114">No entanto, somente o aplicativo que registrou a chave pode cancelar seu registro.</span><span class="sxs-lookup"><span data-stu-id="97ce5-114">However, only the application that registered the key can deregister it.</span></span> <span data-ttu-id="97ce5-115">Um aplicativo pode cancelar o registro de uma chave do nó local usando a função [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) .</span><span class="sxs-lookup"><span data-stu-id="97ce5-115">An application can deregister a key from the local node using the [**DrtUnregisterKey**](/windows/desktop/api/drt/nf-drt-drtunregisterkey) function.</span></span> <span data-ttu-id="97ce5-116">Após a conclusão, a função dispara um evento de alteração de chave de tipo folha de um **\_ evento \_ \_ \_ DRT** ; informando o aplicativo, bem como outros nós que participam da malha DRT.</span><span class="sxs-lookup"><span data-stu-id="97ce5-116">Upon completion the function triggers a **DRT\_EVENT\_LEAFSET\_KEY\_CHANGE** event; informing the application as well as other nodes participating in the DRT mesh.</span></span>

<span data-ttu-id="97ce5-117">Enquanto estiver no estado **DRT \_ com falha** , a chamada necessária de [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) resultará na desregistro de todas as chaves na infraestrutura DRT.</span><span class="sxs-lookup"><span data-stu-id="97ce5-117">While in the **DRT\_FAULTED** state, the required call of [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) will result in the DRT infrastructure deregistering all keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97ce5-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97ce5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97ce5-119">Pesquisando uma tabela de roteamento distribuída</span><span class="sxs-lookup"><span data-stu-id="97ce5-119">Searching a Distributed Routing Table</span></span>](searching-a-distributed-routing-table.md)
</dt> <dt>

[<span data-ttu-id="97ce5-120">Sobre tabelas de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="97ce5-120">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)
</dt> <dt>

[<span data-ttu-id="97ce5-121">Referência de API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="97ce5-121">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



