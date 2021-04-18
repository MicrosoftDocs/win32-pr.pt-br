---
title: Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel
description: Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105765783"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a><span data-ttu-id="8c2db-103">Requisitos de assinatura de recursos de inicialização segura para drivers de modo kernel</span><span class="sxs-lookup"><span data-stu-id="8c2db-103">Secure boot feature signing requirements for kernel-mode drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="8c2db-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="8c2db-104">Platforms</span></span>

<span data-ttu-id="8c2db-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="8c2db-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="8c2db-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c2db-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="8c2db-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c2db-107">Description</span></span>

<span data-ttu-id="8c2db-108">No Windows 8 e no Windows Server 2012, incluindo o WinPE, o kernel foi bloqueado para evitar que malwares introduzidos por kits de inicialização ou raiz contornem os requisitos de segurança do sistema operacional Windows para drivers assinados.</span><span class="sxs-lookup"><span data-stu-id="8c2db-108">In Windows 8 and Windows Server 2012, including WinPE, the kernel has been locked down to prevent malware introduced by boot or root kits from circumventing Windows operating system security requirements for signed drivers.</span></span>

<span data-ttu-id="8c2db-109">Essa alteração afeta todos os drivers de modo kernel para dispositivos que dão suporte à inicialização segura da UEFI (Unified Extensible Firmware Interface); A inicialização segura de UEFI é necessária para a certificação do Windows 8 para computadores cliente e opcional para servidores.</span><span class="sxs-lookup"><span data-stu-id="8c2db-109">This change affects all kernel-mode drivers for devices that support unified extensible firmware interface (UEFI) Secure Boot; UEFI Secure Boot is required for Windows 8 certification for client machines, and optional for servers.</span></span> <span data-ttu-id="8c2db-110">Ele não afeta os drivers do modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="8c2db-110">It does not affect user-mode drivers.</span></span>

<span data-ttu-id="8c2db-111">O desenvolvimento padrão para drivers de modo kernel envolve o uso de depuração de modo kernel ou da configuração BCD (dados de configuração de inicialização) <testsigning> .</span><span class="sxs-lookup"><span data-stu-id="8c2db-111">Standard development for kernel-mode drivers involves either the use of kernel mode debugging or the boot configuration data (BCD) <testsigning> setting.</span></span> <span data-ttu-id="8c2db-112">Ambos são desabilitados quando a inicialização segura está ativada.</span><span class="sxs-lookup"><span data-stu-id="8c2db-112">Both of these are disabled when Secured Boot is on.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8c2db-113">Manifestação</span><span class="sxs-lookup"><span data-stu-id="8c2db-113">Manifestation</span></span>

<span data-ttu-id="8c2db-114">Os drivers do modo kernel não serão executados se não forem assinados corretamente por uma autoridade de certificação (CA) confiável.</span><span class="sxs-lookup"><span data-stu-id="8c2db-114">Kernel-mode drivers will not run if they are not properly signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="8c2db-115">O sistema operacional não permitirá que drivers não confiáveis sejam executados e mecanismos padrão, como depuração de kernel e testsigning, não sejam permitidos.</span><span class="sxs-lookup"><span data-stu-id="8c2db-115">The operating system will not allow untrusted drivers to run and standard mechanisms like kernel debugging and testsigning will not be permitted.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8c2db-116">Atenuação</span><span class="sxs-lookup"><span data-stu-id="8c2db-116">Mitigation</span></span>

<span data-ttu-id="8c2db-117">Para testar os drivers, você deve desabilitar a inicialização segura no BIOS, bem como atender aos outros requisitos de assinatura de teste (veja abaixo).</span><span class="sxs-lookup"><span data-stu-id="8c2db-117">To test drivers, you must disable Secure Boot in BIOS as well as meet the other test-signing requirements (see below).</span></span>

<span data-ttu-id="8c2db-118">Ao distribuir drivers mais amplamente eles devem ser assinados corretamente por uma AC confiável.</span><span class="sxs-lookup"><span data-stu-id="8c2db-118">When distributing drivers more widely they must be properly signed by a trusted CA.</span></span>

## <a name="resources"></a><span data-ttu-id="8c2db-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="8c2db-119">Resources</span></span>

-   <span data-ttu-id="8c2db-120">[Drivers de assinatura](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8c2db-120">[Signing Drivers](/previous-versions/windows/hardware/design/dn653563(v=vs.85))</span></span>

 

 