---
title: Gravando clientes e servidores compatíveis com versões anteriores
description: Teoricamente, o esquema de controle de versão do RPC ajuda a impedir a comunicação inconsistente entre servidores e clientes modificados e seus correspondentes implantados.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, compatibilidade com versões anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084055"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="091e7-104">Gravando clientes e servidores compatíveis com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="091e7-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="091e7-105">Teoricamente, o esquema de controle de versão do RPC ajuda a impedir a comunicação inconsistente entre servidores e clientes modificados e seus correspondentes implantados.</span><span class="sxs-lookup"><span data-stu-id="091e7-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="091e7-106">Na prática, no entanto, os desenvolvedores geralmente devem introduzir alterações em interfaces existentes sem modificar a versão, pois os clientes e servidores anteriores devem ser capazes de se comunicar com os novos.</span><span class="sxs-lookup"><span data-stu-id="091e7-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="091e7-107">Esse é um problema maior para RPC padrão do que para COM; a consulta é uma maneira natural de procurar interfaces com suporte no COM, enquanto o tratamento de exceções de RPC deve ser usado para cobertura equivalente.</span><span class="sxs-lookup"><span data-stu-id="091e7-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="091e7-108">Esta seção aborda as melhores práticas de programação de RPC para tratar dessas situações.</span><span class="sxs-lookup"><span data-stu-id="091e7-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="091e7-109">Esta seção é dividida nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="091e7-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="091e7-110">A teoria do controle de versão para RPC e COM</span><span class="sxs-lookup"><span data-stu-id="091e7-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="091e7-111">Alterando interfaces de maneira compatível com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="091e7-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="091e7-112">Exemplos de alterações incompatíveis</span><span class="sxs-lookup"><span data-stu-id="091e7-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




