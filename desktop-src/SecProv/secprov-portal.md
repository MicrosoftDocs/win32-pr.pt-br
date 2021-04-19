---
description: Os provedores WMI de segurança podem ser usados para scripts WMI e para criar um provedor de segurança gerenciado.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Provedores WMI de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770248"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="36ff3-103">Provedores WMI de segurança</span><span class="sxs-lookup"><span data-stu-id="36ff3-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="36ff3-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="36ff3-104">Purpose</span></span>

<span data-ttu-id="36ff3-105">Os provedores de segurança WMI permitem que administradores e programadores configurem Criptografia de Unidade de Disco BitLocker (BDE) e o Trusted Platform Module (TPM) usando Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="36ff3-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="36ff3-106">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="36ff3-106">Developer audience</span></span>

<span data-ttu-id="36ff3-107">Este documento especifica a interface do provedor WMI para gerenciar e configurar Criptografia de Unidade de Disco BitLocker (BDE) e Trusted Platform Module (TPM) no Windows Server 2008 R2 e no Windows Server 2008 para servidores e no Windows 7 e no Windows Vista para computadores cliente.</span><span class="sxs-lookup"><span data-stu-id="36ff3-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="36ff3-108">Ele se destina a ser lido por esses scripts de escrita, elementos de interface do usuário ou outras ferramentas administrativas para o BDE ou o TPM.</span><span class="sxs-lookup"><span data-stu-id="36ff3-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="36ff3-109">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="36ff3-109">Run-time requirements</span></span>

<span data-ttu-id="36ff3-110">Os provedores de WMI de segurança exigem o arquivo. mof especificado com cada provedor e um sistema operacional com suporte.</span><span class="sxs-lookup"><span data-stu-id="36ff3-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="36ff3-111">O sistema operacional mínimo é o Windows Server 2008 ou o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36ff3-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="36ff3-112">Criptografia de Unidade de Disco BitLocker só está disponível para as versões Windows Vista Enterprise e Windows Vista Ultimate do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36ff3-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="36ff3-113">Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.</span><span class="sxs-lookup"><span data-stu-id="36ff3-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="36ff3-114">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="36ff3-114">In this section</span></span>



| <span data-ttu-id="36ff3-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="36ff3-115">Topic</span></span>                                                                               | <span data-ttu-id="36ff3-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="36ff3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="36ff3-117">Sobre provedores WMI de segurança</span><span class="sxs-lookup"><span data-stu-id="36ff3-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="36ff3-118">Breve visão geral dos provedores de WMI de segurança.</span><span class="sxs-lookup"><span data-stu-id="36ff3-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="36ff3-119">Referência de provedores WMI de segurança</span><span class="sxs-lookup"><span data-stu-id="36ff3-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="36ff3-120">Documentação de referência para os provedores de WMI de segurança.</span><span class="sxs-lookup"><span data-stu-id="36ff3-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="36ff3-121">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="36ff3-121">Additional resources</span></span>

<span data-ttu-id="36ff3-122">A seguir estão os recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="36ff3-122">The following are additional resources.</span></span>



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36ff3-123">Classes</span><span class="sxs-lookup"><span data-stu-id="36ff3-123">Classes</span></span><br/> | <span data-ttu-id="36ff3-124">Para obter mais informações sobre os provedores de WMI de segurança, consulte [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) e [**Win32 \_ TPM**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="36ff3-124">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span><br/> |



 

 

 




