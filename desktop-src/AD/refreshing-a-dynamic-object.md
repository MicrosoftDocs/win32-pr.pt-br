---
title: Atualizando um objeto dinâmico
description: Um cliente pode atualizar a TTL (vida útil) de uma determinada entrada de diretório para mantê-la ativa em uma das duas maneiras de executar uma atualização LDAP para o valor de seu atributo entryTTL antes que a entrada seja coletada pelo lixo.
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7866c423fcb715289793a7beefa564150954257
ms.sourcegitcommit: 4d6ff888fd5825e78bc8fd5cdb21d4b542205039
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105769080"
---
# <a name="refreshing-a-dynamic-object"></a><span data-ttu-id="68b91-103">Atualizando um objeto dinâmico</span><span class="sxs-lookup"><span data-stu-id="68b91-103">Refreshing a Dynamic Object</span></span>

<span data-ttu-id="68b91-104">Um cliente pode atualizar a TTL (vida útil) de uma determinada entrada de diretório para mantê-la ativa em uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="68b91-104">A client can refresh the Time To Live (TTL) of a given directory entry to keep it alive in one of two ways:</span></span>

-   <span data-ttu-id="68b91-105">Executar uma atualização LDAP para o valor de seu atributo **entryTTL** antes que a entrada seja coletada pelo lixo.</span><span class="sxs-lookup"><span data-stu-id="68b91-105">Performing an LDAP update to the value of its **entryTTL** attribute before the entry is garbage collected.</span></span> <span data-ttu-id="68b91-106">Esse método de atualização de uma entrada dinâmica no diretório é um recurso adicional (opcional) de Active Directory Domain Services que não é especificado pelo RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="68b91-106">This method of refreshing a dynamic entry in the directory is an additional (optional) feature of Active Directory Domain Services that is not specified by RFC 2589.</span></span>
-   <span data-ttu-id="68b91-107">Executar uma operação estendida LDAP com um OID de 1.3.6.1.4.1.1466.101.119.1 para a atualização de TTL, conforme estipulado no RFC 2589.</span><span class="sxs-lookup"><span data-stu-id="68b91-107">Performing an LDAP extended operation with an OID of 1.3.6.1.4.1.1466.101.119.1 for TTL refresh, as stipulated in the RFC 2589.</span></span> <span data-ttu-id="68b91-108">Esse OID é definido como **o \_ \_ OID de \_ op \_ estendido de TTL LDAP** em WINLDAP. H.</span><span class="sxs-lookup"><span data-stu-id="68b91-108">This OID is defined as **LDAP\_TTL\_EXTENDED\_OP\_OID** in WINLDAP.H.</span></span>

 
<span data-ttu-id="68b91-109">\* \* Comentário \* \* \*: os objetos dinâmicos são removidos pelo coletor de lixo quando expiraram, não há nenhuma fase do objeto sendo uma marca de exclusão quando expirado.</span><span class="sxs-lookup"><span data-stu-id="68b91-109">\*\*Remark\*\*\*: Dynamic objects are removed by Garbage Collector when they have expired, there is no phase of the object being a tombstone when it has expired.</span></span> <span data-ttu-id="68b91-110">Você precisa ter cuidado com a latência de replicação do AD ao atualizar objetos.</span><span class="sxs-lookup"><span data-stu-id="68b91-110">You need to be careful with the AD replication latency when you refresh objects.</span></span> <span data-ttu-id="68b91-111">Você precisa garantir que a atualização para atualizar o TTL chegue cedo o suficiente para que todas as réplicas do contexto de nomenclatura (catálogo completo e global) vejam a transação de atualização antes que o objeto expire localmente.</span><span class="sxs-lookup"><span data-stu-id="68b91-111">You have to ensure that the update to refresh the TTL arrives early enough so all replicas of the naming context (full and global catalog) see the refresh transaction before the object expires locally.</span></span>

 




