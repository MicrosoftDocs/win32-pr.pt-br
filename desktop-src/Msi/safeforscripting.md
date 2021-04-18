---
description: Se essa política do sistema por máquina estiver definida como &\# 0034; 1&\# 0034;, o instalador não avisará os usuários quando os scripts em uma página da Web usarem a interface de automação do instalador.
ms.assetid: 1365996d-30a2-43f9-8e1b-7704d46a11c9
title: SafeForScripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2907c4b021101ff936bdddf98a5cc1e32a01b991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756891"
---
# <a name="safeforscripting"></a><span data-ttu-id="16170-103">SafeForScripting</span><span class="sxs-lookup"><span data-stu-id="16170-103">SafeForScripting</span></span>

<span data-ttu-id="16170-104">Se essa [política do sistema](system-policy.md) por máquina for definida como "1", o instalador não avisará os usuários quando os scripts em uma página da Web usarem a [interface de automação](automation-interface.md)do instalador.</span><span class="sxs-lookup"><span data-stu-id="16170-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer does not prompt users when scripts within a Web page use the installer's [automation interface](automation-interface.md).</span></span>

<span data-ttu-id="16170-105">Antes de definir essa política, você deve considerar se, antes do prompt do usuário, ele fornece um nível apropriado de segurança para seus usuários.</span><span class="sxs-lookup"><span data-stu-id="16170-105">Before setting this policy, you should consider whether foregoing the user prompt provides an appropriate level of security for your users.</span></span> <span data-ttu-id="16170-106">Se essa política não estiver definida, quando um script hospedado por um navegador da Internet tentar instalar um aplicativo, o sistema avisará o usuário e solicitará que eles aceitem ou recusem a instalação.</span><span class="sxs-lookup"><span data-stu-id="16170-106">If this policy is not set, when a script hosted by an Internet browser tries to install an application, the system warns the user and asks them to accept or refuse the installation.</span></span> <span data-ttu-id="16170-107">A definição de SafeForScripting suprime esse aviso e pode permitir a instalação de aplicativos no sistema sem o conhecimento do usuário.</span><span class="sxs-lookup"><span data-stu-id="16170-107">Setting SafeForScripting suppresses this warning and may allow the installation of applications on the system without the user's knowledge.</span></span> <span data-ttu-id="16170-108">Essa política pode ser útil para uma empresa que usa ferramentas baseadas na Web para distribuir programas.</span><span class="sxs-lookup"><span data-stu-id="16170-108">This policy may be useful for an enterprise that uses web-based tools to distribute programs.</span></span>

<span data-ttu-id="16170-109">Para obter mais informações, consulte [diretrizes para criar instalações seguras](guidelines-for-authoring-secure-installations.md) e [assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md) e [baixar uma instalação da Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="16170-109">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="16170-110">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="16170-110">Registry Key</span></span>

<span data-ttu-id="16170-111">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="16170-111">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="16170-112">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="16170-112">Data Type</span></span>

<span data-ttu-id="16170-113">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="16170-113">**REG\_DWORD**</span></span>

 

 



