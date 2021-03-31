---
title: Sobre TBS
description: Um serviço de sistema que permite o compartilhamento transparente dos recursos de Trusted Platform Module (TPM).
ms.assetid: 5ab3f514-dea9-48f7-97d9-abc774e2a273
keywords:
- TBS de serviços base do TPM, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5d40b1fca688676978f274cb976afedb6e6a56
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104161783"
---
# <a name="about-tbs"></a><span data-ttu-id="2b867-104">Sobre TBS</span><span class="sxs-lookup"><span data-stu-id="2b867-104">About TBS</span></span>

<span data-ttu-id="2b867-105">O recurso TBS (serviços base do TPM) é um serviço do sistema que permite o compartilhamento transparente dos recursos do Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="2b867-105">The TPM Base Services (TBS) feature is a system service that allows transparent sharing of the Trusted Platform Module (TPM) resources.</span></span> <span data-ttu-id="2b867-106">Ele compartilha simultaneamente os recursos do TPM entre vários aplicativos no mesmo computador físico, mesmo que esses aplicativos sejam executados em máquinas virtuais diferentes.</span><span class="sxs-lookup"><span data-stu-id="2b867-106">It simultaneously shares the TPM resources among multiple applications on the same physical machine, even if those applications run on different virtual machines.</span></span> <span data-ttu-id="2b867-107">A partir do Windows 8 e do Windows Server 2012, o TBS vem pré-instalado em todos os sistemas com um TPM.</span><span class="sxs-lookup"><span data-stu-id="2b867-107">Starting with Windows 8 and Windows Server 2012, TBS comes pre-installed on all systems with a TPM.</span></span>

<span data-ttu-id="2b867-108">O Trusted Computing Group (TCG) define um Trusted Platform Module que fornece funções criptográficas projetadas para fornecer confiança na plataforma.</span><span class="sxs-lookup"><span data-stu-id="2b867-108">The Trusted Computing Group (TCG) defines a Trusted Platform Module that provides cryptographic functions designed to provide trust in the platform.</span></span> <span data-ttu-id="2b867-109">Como o TPM é implementado no hardware, ele tem recursos finitos.</span><span class="sxs-lookup"><span data-stu-id="2b867-109">Because the TPM is implemented in hardware, it has finite resources.</span></span> <span data-ttu-id="2b867-110">O TCG também define uma pilha de software que utiliza esses recursos para fornecer operações confiáveis para o software do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2b867-110">The TCG also defines a software stack that makes use of these resources to provide trusted operations for application software.</span></span> <span data-ttu-id="2b867-111">No entanto, nenhum provisionamento é feito para executar uma implementação de TSS lado a lado com o software do sistema operacional que também pode estar usando recursos do TPM.</span><span class="sxs-lookup"><span data-stu-id="2b867-111">However, no provision is made for running a TSS implementation side-by-side with operating system software that may also be using TPM resources.</span></span> <span data-ttu-id="2b867-112">O recurso TBS resolve esse problema habilitando cada pilha de software que se comunica com TBS para usar os recursos do TPM verificando quaisquer outras pilhas de software que possam estar em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="2b867-112">The TBS feature solves this problem by enabling each software stack that communicates with TBS to use TPM resources checking for any other software stacks that may be running on the machine.</span></span>

<span data-ttu-id="2b867-113">A especificação do TPM e a especificação TSS (pilha de software TCG) estão disponíveis em [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/) .</span><span class="sxs-lookup"><span data-stu-id="2b867-113">The TPM specification and TCG Software Stack (TSS) specification are available at [https://www.trustedcomputinggroup.org](https://www.trustedcomputinggroup.org/).</span></span>

<span data-ttu-id="2b867-114">O TBS é implementado como um serviço fora do processo que aceita comandos que usam um serviço RPC.</span><span class="sxs-lookup"><span data-stu-id="2b867-114">TBS is implemented as an out-of-process service that accepts commands that use an RPC service.</span></span> <span data-ttu-id="2b867-115">Uma biblioteca vinculada dinamicamente apresenta a interface de linguagem C e se comunica com o serviço TBS.</span><span class="sxs-lookup"><span data-stu-id="2b867-115">A dynamically linked library presents the C language interface and communicates with the TBS service.</span></span>

> [!Note]  
> <span data-ttu-id="2b867-116">O serviço TBS aceita apenas solicitações RPC do computador local.</span><span class="sxs-lookup"><span data-stu-id="2b867-116">The TBS service only accepts RPC requests from the local machine.</span></span>

 

<span data-ttu-id="2b867-117">Os principais objetivos do TBS são:</span><span class="sxs-lookup"><span data-stu-id="2b867-117">The primary goals of the TBS are to:</span></span>

-   <span data-ttu-id="2b867-118">Fornecer compartilhamento eficiente de recursos limitados do TPM, como slots de chave, slots de sessões de autorização e slots de transporte.</span><span class="sxs-lookup"><span data-stu-id="2b867-118">Provide efficient sharing of limited TPM resources, such as key slots, authorization sessions slots, and transport slots.</span></span>
-   <span data-ttu-id="2b867-119">Fornecer acesso priorizado e sincronizado aos recursos do TPM entre várias instâncias de pilhas de software do TPM.</span><span class="sxs-lookup"><span data-stu-id="2b867-119">Provide prioritized and synchronized access to TPM resources between multiple instances of TPM software stacks.</span></span>
-   <span data-ttu-id="2b867-120">Forneça o gerenciamento apropriado de recursos do TPM em todos os Estados de energia.</span><span class="sxs-lookup"><span data-stu-id="2b867-120">Provide appropriate management of TPM resources across power states.</span></span>
-   <span data-ttu-id="2b867-121">Impedir que as pilhas de software do TPM acessem comandos do TPM que devem ser restritos, devido a limitações de plataforma ou requisitos administrativos.</span><span class="sxs-lookup"><span data-stu-id="2b867-121">Prevent TPM software stacks from accessing TPM commands that should be restricted, either because of platform limitations or administrative requirements.</span></span>

<span data-ttu-id="2b867-122">A ilustração a seguir mostra a relação entre o TBS e o TPM.</span><span class="sxs-lookup"><span data-stu-id="2b867-122">The following illustration shows the relationship of the TBS to the TPM.</span></span>

![relação entre TBS no modo de usuário e o TPM no modo kernel](images/tbs-block-diagram-as11601.png)

 

 




