---
description: Se o valor dessa política do sistema por máquina estiver definido como &\# 0034; 2&\# 0034; o instalador estará sempre desabilitado para todos os aplicativos. Se esse valor de política for definido como &\# 0034; 1&\# 0034;, o instalador será desabilitado para aplicativos não gerenciados, mas ainda estará habilitado para aplicativos gerenciados.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011155"
---
# <a name="disablemsi"></a><span data-ttu-id="bb34f-104">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="bb34f-104">DisableMSI</span></span>

<span data-ttu-id="bb34f-105">Se o valor dessa [política do sistema](system-policy.md) por máquina estiver definido como "2", o instalador estará sempre desabilitado para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bb34f-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="bb34f-106">Se esse valor de política for definido como "1", o instalador será desabilitado para aplicativos não gerenciados, mas ainda estará habilitado para aplicativos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="bb34f-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="bb34f-107">A tabela a seguir lista as possíveis configurações.</span><span class="sxs-lookup"><span data-stu-id="bb34f-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="bb34f-108">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="bb34f-108">DisableMSI</span></span> | <span data-ttu-id="bb34f-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb34f-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb34f-110">*Default*</span><span class="sxs-lookup"><span data-stu-id="bb34f-110">*Default*</span></span>  | <span data-ttu-id="bb34f-111">No Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 e Windows Server 2008 R2, se o valor da política for nulo, ausente ou qualquer número diferente de 1 ou 2, o Windows Installer será habilitado para aplicativos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="bb34f-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="bb34f-112">As instalações de aplicativos não gerenciados são bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="bb34f-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="bb34f-113">No Windows XP, no Windows Vista e no Windows 7, a Windows Installer está habilitada para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bb34f-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="bb34f-114">Todas as operações de instalação são permitidas.</span><span class="sxs-lookup"><span data-stu-id="bb34f-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="bb34f-115">0</span><span class="sxs-lookup"><span data-stu-id="bb34f-115">0</span></span>          | <span data-ttu-id="bb34f-116">O Windows Installer está habilitado para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bb34f-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="bb34f-117">Todas as operações de instalação são permitidas.</span><span class="sxs-lookup"><span data-stu-id="bb34f-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="bb34f-118">1</span><span class="sxs-lookup"><span data-stu-id="bb34f-118">1</span></span>          | <span data-ttu-id="bb34f-119">O Windows Installer está desabilitado para aplicativos não gerenciados, mas ainda está habilitado para aplicativos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="bb34f-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="bb34f-120">As instalações não elevadas por usuário são bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="bb34f-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="bb34f-121">Instalações elevadas por usuário e por máquina são permitidas.</span><span class="sxs-lookup"><span data-stu-id="bb34f-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="bb34f-122">2</span><span class="sxs-lookup"><span data-stu-id="bb34f-122">2</span></span>          | <span data-ttu-id="bb34f-123">O Windows Installer está sempre desabilitado para todos os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="bb34f-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="bb34f-124">Nenhuma instalação é permitida, incluindo reparos, reinstalação ou instalações sob demanda.</span><span class="sxs-lookup"><span data-stu-id="bb34f-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="bb34f-125">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="bb34f-125">Registry Key</span></span>

<span data-ttu-id="bb34f-126">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="bb34f-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="bb34f-127">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="bb34f-127">Data Type</span></span>

<span data-ttu-id="bb34f-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb34f-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb34f-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bb34f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb34f-130">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="bb34f-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




