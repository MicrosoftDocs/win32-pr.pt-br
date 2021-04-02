---
description: O futuro da criptografia e das comunicações seguras não podem ser facilmente previstos.
ms.assetid: 41c1758d-1213-47a6-81d5-7755b41c3007
title: Estendendo a funcionalidade de CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec079a9ba81d7b264d317664f3c6e971d521090
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922681"
---
# <a name="extending-cryptoapi-functionality"></a><span data-ttu-id="8e43e-103">Estendendo a funcionalidade de CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="8e43e-103">Extending CryptoAPI Functionality</span></span>

<span data-ttu-id="8e43e-104">O futuro da [*criptografia*](../secgloss/c-gly.md) e das comunicações seguras não podem ser facilmente previstos.</span><span class="sxs-lookup"><span data-stu-id="8e43e-104">The future of [*cryptography*](../secgloss/c-gly.md) and secure communications cannot easily be predicted.</span></span> <span data-ttu-id="8e43e-105">Novos tipos de certificado podem surgir, várias extensões de certificado podem encontrar uso comum e novos tipos de mensagem podem ser introduzidos.</span><span class="sxs-lookup"><span data-stu-id="8e43e-105">New certificate types might emerge, various certificate extensions might find common usage, and new message types might be introduced.</span></span> <span data-ttu-id="8e43e-106">Por isso, a extensibilidade faz parte do design das principais funções de [*CryptoAPI*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8e43e-106">Because of this, extensibility is part of the design of key [*CryptoAPI*](../secgloss/c-gly.md) functions.</span></span>

<span data-ttu-id="8e43e-107">As seções a seguir apresentam visões gerais sobre o uso de OIDs para estender funções de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="8e43e-107">The following sections present overviews on the use of OIDs for extending CryptoAPI functions.</span></span>



| <span data-ttu-id="8e43e-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="8e43e-108">Topic</span></span>                                                                              | <span data-ttu-id="8e43e-109">Sumário</span><span class="sxs-lookup"><span data-stu-id="8e43e-109">Contents</span></span>                                                                                                                            |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8e43e-110">Visão geral de OID</span><span class="sxs-lookup"><span data-stu-id="8e43e-110">OID Overview</span></span>](oid-overview.md)                                                   | <span data-ttu-id="8e43e-111">Conceitos básicos de OID.</span><span class="sxs-lookup"><span data-stu-id="8e43e-111">OID fundamental concepts.</span></span>                                                                                                           |
| [<span data-ttu-id="8e43e-112">Criando a nova funcionalidade</span><span class="sxs-lookup"><span data-stu-id="8e43e-112">Creating the New Functionality</span></span>](creating-the-new-functionality.md)               | <span data-ttu-id="8e43e-113">Criando OIDs e funções para estender o uso de APIs existentes.</span><span class="sxs-lookup"><span data-stu-id="8e43e-113">Creating OIDs and functions to extend the use of existing APIs.</span></span>                                                                     |
| [<span data-ttu-id="8e43e-114">Registrando a nova funcionalidade</span><span class="sxs-lookup"><span data-stu-id="8e43e-114">Registering the New Functionality</span></span>](registering-the-new-functionality.md)         | <span data-ttu-id="8e43e-115">Configurando novas funções relacionadas a OID.</span><span class="sxs-lookup"><span data-stu-id="8e43e-115">Setting up new OID-related functions.</span></span>                                                                                               |
| [<span data-ttu-id="8e43e-116">Instalando a nova funcionalidade</span><span class="sxs-lookup"><span data-stu-id="8e43e-116">Installing the New Functionality</span></span>](installing-the-new-functionality.md)           | <span data-ttu-id="8e43e-117">Instalando funções de OID na memória para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8e43e-117">Installing OID functions to memory to improve performance.</span></span>                                                                          |
| [<span data-ttu-id="8e43e-118">Estendendo a funcionalidade CertOpenStore</span><span class="sxs-lookup"><span data-stu-id="8e43e-118">Extending CertOpenStore Functionality</span></span>](extending-certopenstore-functionality.md) | <span data-ttu-id="8e43e-119">Estendendo a funcionalidade [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) usando a função instalável ou registrada do provedor de repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="8e43e-119">Extending [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) functionality using installable or registered certificate-store-provider function.</span></span> |



 

 

 
