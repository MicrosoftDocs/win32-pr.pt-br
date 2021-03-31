---
title: Inicialização Medida
description: Inicialização Medida
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccbba6e5f96fd91c00c295c4b15cab8849f11dc
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103641959"
---
# <a name="measured-boot"></a><span data-ttu-id="a79e6-103">Inicialização Medida</span><span class="sxs-lookup"><span data-stu-id="a79e6-103">Measured Boot</span></span>

## <a name="platforms"></a><span data-ttu-id="a79e6-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="a79e6-104">Platforms</span></span>

 <span data-ttu-id="a79e6-105">**Clientes** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="a79e6-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="a79e6-106">**Servidores** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a79e6-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="a79e6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a79e6-107">Description</span></span>

<span data-ttu-id="a79e6-108">Como o software antimalware (AM) se tornou melhor e melhor na detecção de malware de tempo de execução, os invasores também estão se tornando melhores na criação de rootkits que podem se esconder da detecção.</span><span class="sxs-lookup"><span data-stu-id="a79e6-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="a79e6-109">Detectar malwares que iniciam no início do ciclo de inicialização é um desafio que a maioria dos fornecedores nos atendem de maneira programada.</span><span class="sxs-lookup"><span data-stu-id="a79e6-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="a79e6-110">Normalmente, eles criam hackers do sistema que não têm suporte no sistema operacional do host e podem realmente resultar na colocação do computador em um estado instável.</span><span class="sxs-lookup"><span data-stu-id="a79e6-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="a79e6-111">Até este ponto, o Windows não forneceu uma boa maneira para que eu detecte e resolva essas ameaças de inicialização antecipada.</span><span class="sxs-lookup"><span data-stu-id="a79e6-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span> <span data-ttu-id="a79e6-112">O Windows 8 apresenta um novo recurso chamado inicialização medida, que mede cada componente, do firmware até os drivers de inicialização, armazena essas medidas no Trusted Platform Module (TPM) no computador e disponibiliza um log que pode ser testado remotamente para verificar o estado de inicialização do cliente.</span><span class="sxs-lookup"><span data-stu-id="a79e6-112">Windows 8 introduces a new feature called Measured Boot, which measures each component, from firmware up through the boot start drivers, stores those measurements in the Trusted Platform Module (TPM) on the machine, and then makes available a log that can be tested remotely to verify the boot state of the client.</span></span>

## <a name="manifestation"></a><span data-ttu-id="a79e6-113">Manifestação</span><span class="sxs-lookup"><span data-stu-id="a79e6-113">Manifestation</span></span>

<span data-ttu-id="a79e6-114">O recurso de inicialização medido fornece software com um log confiável (resistente à falsificação e violação) de todos os componentes de inicialização que começaram antes do software.</span><span class="sxs-lookup"><span data-stu-id="a79e6-114">The Measured Boot feature provides AM software with a trusted (resistant to spoofing and tampering) log of all boot components that started before AM software.</span></span> <span data-ttu-id="a79e6-115">O software AM pode usar o log para determinar se os componentes que foram executados antes de serem confiáveis ou se estão infectados com malware.</span><span class="sxs-lookup"><span data-stu-id="a79e6-115">AM software can use the log to determine whether components that ran before it are trustworthy or if they are infected with malware.</span></span> <span data-ttu-id="a79e6-116">O software AM no computador local pode enviar o log para um servidor remoto para avaliação.</span><span class="sxs-lookup"><span data-stu-id="a79e6-116">The AM software on the local machine can send the log to a remote sever for evaluation.</span></span> <span data-ttu-id="a79e6-117">O servidor remoto pode iniciar ações de correção interagindo com software no cliente ou por meio de mecanismos fora de banda, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="a79e6-117">The remote server may initiate remediation actions either by interacting with software on the client or through out-of-band mechanisms, as appropriate.</span></span>

## <a name="mitigation"></a><span data-ttu-id="a79e6-118">Atenuação</span><span class="sxs-lookup"><span data-stu-id="a79e6-118">Mitigation</span></span>

<span data-ttu-id="a79e6-119">Em cenários empresariais, o administrador do sistema tem o controle de como as informações de inicialização são usadas.</span><span class="sxs-lookup"><span data-stu-id="a79e6-119">In enterprise scenarios, the system administrator has control of how Measured Boot info is used.</span></span> <span data-ttu-id="a79e6-120">Em cenários de usuário final, por exemplo, o banco online, o consumidor deve optar por usar a inicialização medida para o serviço específico.</span><span class="sxs-lookup"><span data-stu-id="a79e6-120">In end-user scenarios for example, online banking), the consumer must opt in to use Measured Boot for the specific service.</span></span>

## <a name="solution"></a><span data-ttu-id="a79e6-121">Solução</span><span class="sxs-lookup"><span data-stu-id="a79e6-121">Solution</span></span>

<span data-ttu-id="a79e6-122">Um white paper está sendo preparado para detalhar as APIs e as chamadas de função que devem ser feitas para vários cenários de inicialização medidos.</span><span class="sxs-lookup"><span data-stu-id="a79e6-122">A white paper is being prepared that details the APIs and function calls that must be made for various Measured Boot scenarios.</span></span>

 

 




