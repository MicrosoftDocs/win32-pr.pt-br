---
description: Importante essa API é preterida.
ms.assetid: 4e6eb2df-a917-4533-b9f1-8da39598d0b8
title: Provedores de serviço de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5431d8ddda1be977e2a33297613633343fc2f9c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370645"
---
# <a name="cryptographic-service-providers"></a><span data-ttu-id="8ccc4-103">Provedores de serviço de criptografia</span><span class="sxs-lookup"><span data-stu-id="8ccc4-103">Cryptographic Service Providers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8ccc4-104">Essa API está preterida.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-104">This API is deprecated.</span></span> <span data-ttu-id="8ccc4-105">O software novo e o existente devem começar a usar [APIs de próxima geração de criptografia.](/windows/desktop/SecCNG/cng-portal)</span><span class="sxs-lookup"><span data-stu-id="8ccc4-105">New and existing software should start using [Cryptography Next Generation APIs.](/windows/desktop/SecCNG/cng-portal)</span></span> <span data-ttu-id="8ccc4-106">A Microsoft poderá remover essa API em versões futuras.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-106">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="8ccc4-107">Um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) contém implementações de algoritmos e padrões de criptografia.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-107">A [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) contains implementations of cryptographic standards and algorithms.</span></span> <span data-ttu-id="8ccc4-108">No mínimo, um CSP consiste em uma dll ( [*biblioteca de vínculo dinâmico*](../secgloss/d-gly.md) ) que implementa as funções no [*CryptoSPI*](../secgloss/c-gly.md) (uma interface de [*programa do sistema*](../secgloss/s-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="8ccc4-108">At a minimum, a CSP consists of a [*dynamic-link library*](../secgloss/d-gly.md) (DLL) that implements the functions in [*CryptoSPI*](../secgloss/c-gly.md) (a [*system program interface*](../secgloss/s-gly.md)).</span></span> <span data-ttu-id="8ccc4-109">A maioria dos CSPs contém a implementação de todas as suas próprias funções.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-109">Most CSPs contain the implementation of all of their own functions.</span></span> <span data-ttu-id="8ccc4-110">Alguns CSPs, no entanto, implementam suas funções principalmente em um programa de serviço baseado no Windows gerenciado pelo Gerenciador de controle de serviços do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-110">Some CSPs, however, implement their functions mainly in a Windows-based service program managed by the Windows service control manager.</span></span> <span data-ttu-id="8ccc4-111">Outras implementam funções em hardware, como um [*cartão inteligente*](../secgloss/s-gly.md) ou um co-processador seguro.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-111">Others implement functions in hardware, such as a [*smart card*](../secgloss/s-gly.md) or secure coprocessor.</span></span> <span data-ttu-id="8ccc4-112">Se um CSP não implementar suas próprias funções, a DLL atuará como uma camada de passagem, facilitando a comunicação entre o sistema operacional e a implementação do CSP real.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-112">If a CSP does not implement its own functions, the DLL acts as a pass-through layer, facilitating the communication between the operating system and the actual CSP implementation.</span></span>

<span data-ttu-id="8ccc4-113">Esta seção inclui os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-113">This section includes the following topics.</span></span>



| <span data-ttu-id="8ccc4-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="8ccc4-114">Topic</span></span>                                                                                      | <span data-ttu-id="8ccc4-115">Sumário</span><span class="sxs-lookup"><span data-stu-id="8ccc4-115">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ccc4-116">Tipos de provedor criptográfico</span><span class="sxs-lookup"><span data-stu-id="8ccc4-116">Cryptographic Provider Types</span></span>](cryptographic-provider-types.md)                           | <span data-ttu-id="8ccc4-117">Os tipos de provedor criptográfico são famílias de provedores de serviços de criptografia que compartilham formatos de dados e protocolos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-117">Cryptographic provider types are families of cryptographic services providers that share data formats and cryptographic protocols.</span></span> <span data-ttu-id="8ccc4-118">Os formatos de dados incluem esquemas de [*preenchimento*](../secgloss/p-gly.md) de algoritmos, [*comprimentos de chave*](../secgloss/k-gly.md)e modos padrão.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-118">Data formats include algorithms [*padding*](../secgloss/p-gly.md) schemes, [*key lengths*](../secgloss/k-gly.md), and default modes.</span></span> |
| [<span data-ttu-id="8ccc4-119">Provedores de serviços de criptografia da Microsoft</span><span class="sxs-lookup"><span data-stu-id="8ccc4-119">Microsoft Cryptographic Service Providers</span></span>](microsoft-cryptographic-service-providers.md) | <span data-ttu-id="8ccc4-120">Informações detalhadas sobre os CSPs disponíveis atualmente na Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8ccc4-120">Detailed information about CSPs currently available from Microsoft.</span></span>                                                                                                                                                                                                                                                                                       |



 

 

 
