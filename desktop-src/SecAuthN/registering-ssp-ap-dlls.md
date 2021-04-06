---
description: Depois de desenvolver uma biblioteca de vínculo dinâmico (SSP/PA DLL) do pacote de autenticação/provedor de suporte de segurança que contenha um ou mais pacotes de segurança personalizados, você deve registrá-lo.
ms.assetid: db0d899e-dbd4-40d3-98d8-4d9668c01453
title: Registrando DLLs SSP/AP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d279459b91633e0ef45e6e6d57b43489699a657
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662130"
---
# <a name="registering-sspap-dlls"></a><span data-ttu-id="d09c0-103">Registrando DLLs SSP/AP</span><span class="sxs-lookup"><span data-stu-id="d09c0-103">Registering SSP/AP DLLs</span></span>

<span data-ttu-id="d09c0-104">Depois de desenvolver uma biblioteca de vínculo dinâmico do pacote de autenticação do [*provedor de suporte de segurança*](../secgloss/s-gly.md) / [](../secgloss/a-gly.md) (SSP/AP dll) que contém um ou mais [*pacotes de segurança*](../secgloss/s-gly.md)personalizados, você deve registrá-lo.</span><span class="sxs-lookup"><span data-stu-id="d09c0-104">After developing a [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) dynamic-link library (SSP/AP DLL) containing one or more custom [*security packages*](../secgloss/s-gly.md), you must register it.</span></span> <span data-ttu-id="d09c0-105">Para fazer isso, adicione o nome de sua DLL de SSP/PA personalizada aos dados do seguinte valor de registro:</span><span class="sxs-lookup"><span data-stu-id="d09c0-105">To do so, add the name of your custom SSP/AP DLL to the data of the following registry value:</span></span>

<span data-ttu-id="d09c0-106">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **controlar** \\ pacotes de \\ **segurança** LSA</span><span class="sxs-lookup"><span data-stu-id="d09c0-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Security Packages**</span></span>

<span data-ttu-id="d09c0-107">Os dados para esse valor de registro são uma lista dos nomes de DLLs SSP/PA, sem a extensão ". dll".</span><span class="sxs-lookup"><span data-stu-id="d09c0-107">The data for this registry value is a list of the names of SSP/AP DLLs, without the ".dll" extension.</span></span> <span data-ttu-id="d09c0-108">O tipo de dados dessa lista é **reg \_ multi \_ sz** , portanto deve haver um caractere nulo (' \\ 0 ') entre cada nome de dll na lista.</span><span class="sxs-lookup"><span data-stu-id="d09c0-108">The data type for this list is **REG\_MULTI\_SZ** so there must be a null character ('\\0') between each DLL name in the list.</span></span>

<span data-ttu-id="d09c0-109">Normalmente, as DLLs do SSP/AP são armazenadas no diretório% SystemRoot%/system32</span><span class="sxs-lookup"><span data-stu-id="d09c0-109">Typically, SSP/AP DLLs are stored in the %systemroot%/system32 directory.</span></span> <span data-ttu-id="d09c0-110">Se esse for o caminho para sua DLL de SSP/PA personalizada, não inclua o caminho como parte do nome da DLL.</span><span class="sxs-lookup"><span data-stu-id="d09c0-110">If this is the path to your custom SSP/AP DLL then do not include the path as part of the DLL name.</span></span> <span data-ttu-id="d09c0-111">Se, no entanto, a DLL estiver em um caminho diferente, inclua o caminho completo para a DLL no nome.</span><span class="sxs-lookup"><span data-stu-id="d09c0-111">If, however, the DLL is in a different path, include the complete path to the DLL in the name.</span></span>

<span data-ttu-id="d09c0-112">Cada vez que o sistema é iniciado, o LSA carrega as DLLs SSP/AP nessa lista e executa a sequência de inicialização descrita em [inicialização no modo LSA](lsa-mode-initialization.md).</span><span class="sxs-lookup"><span data-stu-id="d09c0-112">Each time the system starts, the LSA loads the SSP/AP DLLs in this list and performs the initialization sequence described in [LSA-Mode Initialization](lsa-mode-initialization.md).</span></span>

### <a name="registering-a-custom-security-package-as-the-default-tls-ssp"></a><span data-ttu-id="d09c0-113">Registrando um pacote de segurança personalizado como o SSP padrão do TLS</span><span class="sxs-lookup"><span data-stu-id="d09c0-113">Registering a custom security package as the default TLS SSP</span></span>

<span data-ttu-id="d09c0-114">Depois de desenvolver um provedor de suporte de segurança TLS personalizado e registrá-lo conforme descrito acima, você também deverá registrá-lo como o "SSP padrão do TLS".</span><span class="sxs-lookup"><span data-stu-id="d09c0-114">After developing a custom TLS security support provider and registering it as described above, you must also register it as the “default TLS SSP.”</span></span> <span data-ttu-id="d09c0-115">Para fazer isso, preencha o nome do pacote do seu SSP personalizado para os dados do seguinte valor de registro:</span><span class="sxs-lookup"><span data-stu-id="d09c0-115">To do so, populate the package name of your custom SSP to the data of the following registry value:</span></span>

<span data-ttu-id="d09c0-116">**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **controle** \\ **LSA** \\ **SSP TLS padrão**</span><span class="sxs-lookup"><span data-stu-id="d09c0-116">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Lsa**\\**Default TLS SSP**</span></span>

<span data-ttu-id="d09c0-117">Os dados para esse valor de registro são o nome do pacote do SSP, não o nome da dll.</span><span class="sxs-lookup"><span data-stu-id="d09c0-117">The data for this registry value is the package name of SSP, not the dll name.</span></span> <span data-ttu-id="d09c0-118">O tipo de dados para isso é **reg \_ sz**.</span><span class="sxs-lookup"><span data-stu-id="d09c0-118">The data type for this is **REG\_SZ**.</span></span>

<span data-ttu-id="d09c0-119">Os aplicativos de modo de usuário que usam "SSP do TLS padrão" usarão o padrão registrado aqui.</span><span class="sxs-lookup"><span data-stu-id="d09c0-119">User mode applications which use “default TLS SSP” will use the default registered here.</span></span> <span data-ttu-id="d09c0-120">Aplicativos de modo kernel ou aplicativos de modo de usuário que usam "provedor de protocolo de segurança unificada da Microsoft" ou outros nomes de SSP TLS específicos não serão afetados por essa alteração.</span><span class="sxs-lookup"><span data-stu-id="d09c0-120">Kernel mode applications or user mode applications which use “Microsoft Unified Security Protocol Provider” or other specific TLS SSP names will not be impacted by this change.</span></span>

> [!Note]  
> <span data-ttu-id="d09c0-121">Essas informações de registro pertencem apenas à DLL do SSP/PA.</span><span class="sxs-lookup"><span data-stu-id="d09c0-121">This registry information pertains to SSP/AP DLL's only.</span></span> <span data-ttu-id="d09c0-122">Para obter informações sobre como registrar os SSPs (provedores de suporte de segurança), consulte [gravando e instalando um provedor de suporte de segurança](writing-and-installing-a-security-support-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d09c0-122">For information about registering security support providers (SSPs), see [Writing and Installing a Security Support Provider](writing-and-installing-a-security-support-provider.md).</span></span> <span data-ttu-id="d09c0-123">Para obter informações sobre as diferenças entre o SSP/AP e as DLLs do SSP, consulte [SSP/APS vs. SSPs](ssp-aps-versus-ssps.md).</span><span class="sxs-lookup"><span data-stu-id="d09c0-123">For information about the differences between SSP/AP and SSP DLLs, see [SSP/APs vs. SSPs](ssp-aps-versus-ssps.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d09c0-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d09c0-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d09c0-125">Restrições sobre o registro e a instalação de um pacote de segurança</span><span class="sxs-lookup"><span data-stu-id="d09c0-125">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
