---
title: Fazendo backup e restaurando um servidor de Active Directory
description: Active Directory Domain Services fornecer funções para fazer backup e restaurar dados no banco de dados de diretório.
ms.assetid: d9b9db51-ed1b-4db4-a4de-b8798c9647ac
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services, usando, fazendo backup e restaurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a92d57c2ddf572db8806aca71282e6b4fd8799ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640437"
---
# <a name="backing-up-and-restoring-an-active-directory-server"></a><span data-ttu-id="037fc-104">Fazendo backup e restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="037fc-104">Backing Up and Restoring an Active Directory Server</span></span>

<span data-ttu-id="037fc-105">Active Directory Domain Services fornecer funções para fazer backup e restaurar dados no banco de dados de diretório.</span><span class="sxs-lookup"><span data-stu-id="037fc-105">Active Directory Domain Services provide functions for backing up and restoring data in the directory database.</span></span> <span data-ttu-id="037fc-106">Esta seção descreve como [fazer backup](backing-up-an-active-directory-server.md) e [restaurar](restoring-an-active-directory-server.md) um servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="037fc-106">This section describes how to [back up](backing-up-an-active-directory-server.md) and [restore](restoring-an-active-directory-server.md) an Active Directory server.</span></span> <span data-ttu-id="037fc-107">Para obter mais informações sobre como fazer backup de um servidor de Active Directory usando os utilitários fornecidos nos sistemas operacionais Windows 2000 e Windows Server 2003, consulte o Resource Kit aplicável, disponível no site do Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="037fc-107">For more information about backing up an Active Directory server using the utilities provided in Windows 2000 and Windows Server 2003 operating systems, see the applicable Resource Kit, available on the Microsoft TechNet website.</span></span>

<span data-ttu-id="037fc-108">O backup de um servidor de Active Directory deve ser executado online e deve ser executado quando o Active Directory Domain Services estiver instalado.</span><span class="sxs-lookup"><span data-stu-id="037fc-108">Backup of an Active Directory server must be performed online and must be performed when the Active Directory Domain Services are installed.</span></span> <span data-ttu-id="037fc-109">Os Active Directory Domain Services são criados em um banco de dados especial e exportam um conjunto de funções de backup que fornecem a interface de backup programática.</span><span class="sxs-lookup"><span data-stu-id="037fc-109">Active Directory Domain Services are built on a special database and export a set of backup functions that provide the programmatic backup interface.</span></span> <span data-ttu-id="037fc-110">O backup não oferece suporte a backups incrementais.</span><span class="sxs-lookup"><span data-stu-id="037fc-110">The backup does not support incremental backups.</span></span> <span data-ttu-id="037fc-111">Um aplicativo de backup é associado a uma DLL do lado do cliente local com pontos de entrada definidos em Ntdsbcli. h.</span><span class="sxs-lookup"><span data-stu-id="037fc-111">A backup application binds to a local client-side DLL with entry points defined in Ntdsbcli.h.</span></span>

<span data-ttu-id="037fc-112">A restauração de um servidor de Active Directory é sempre executada offline.</span><span class="sxs-lookup"><span data-stu-id="037fc-112">Restoration of an Active Directory server is always performed offline.</span></span>

<span data-ttu-id="037fc-113">Embora os tópicos nesta seção descrevam apenas como fazer backup e restaurar um servidor de Active Directory, lembre-se de que o Windows 2000 e os sistemas operacionais Windows Server 2003 têm vários componentes de "estado do sistema" que devem ser armazenados em backup e restaurados juntos.</span><span class="sxs-lookup"><span data-stu-id="037fc-113">Although the topics in this section describe only how to back up and restore an Active Directory server, be aware that Windows 2000 and the Windows Server 2003 operating systems have several "system state" components that must be backed up and restored together.</span></span> <span data-ttu-id="037fc-114">Esses componentes de estado do sistema consistem em:</span><span class="sxs-lookup"><span data-stu-id="037fc-114">These system state components consist of:</span></span>

-   <span data-ttu-id="037fc-115">Arquivos de inicialização, como NTLDR, NTDETECT, todos os arquivos protegidos por SFP e configuração do contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="037fc-115">Boot files such as ntldr, ntdetect, all files protected by SFP, and performance counter configuration</span></span>
-   <span data-ttu-id="037fc-116">O controlador de Domínio do Active Directory</span><span class="sxs-lookup"><span data-stu-id="037fc-116">The Active Directory Domain Controller</span></span>
-   <span data-ttu-id="037fc-117">SysVol (somente controlador de domínio)</span><span class="sxs-lookup"><span data-stu-id="037fc-117">SysVol (domain controller only)</span></span>
-   <span data-ttu-id="037fc-118">Servidor de certificado (somente CA)</span><span class="sxs-lookup"><span data-stu-id="037fc-118">Certificate Server (CA only)</span></span>
-   <span data-ttu-id="037fc-119">Banco de dados do cluster (somente nó do cluster)</span><span class="sxs-lookup"><span data-stu-id="037fc-119">Cluster database (cluster node only)</span></span>
-   <span data-ttu-id="037fc-120">Registro</span><span class="sxs-lookup"><span data-stu-id="037fc-120">Registry</span></span>
-   <span data-ttu-id="037fc-121">Banco de dados de registro de classe COM+</span><span class="sxs-lookup"><span data-stu-id="037fc-121">COM+ class registration database</span></span>

<span data-ttu-id="037fc-122">O backup do estado do sistema pode ser feito em qualquer ordem, mas a restauração do estado do sistema deve ocorrer na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="037fc-122">The system state can be backed up in any order, but restoration of the system state must occur in the following order:</span></span>

1.  <span data-ttu-id="037fc-123">Restaure os arquivos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="037fc-123">Restore the boot files.</span></span>
2.  <span data-ttu-id="037fc-124">Restaure SysVol, servidor de certificado, banco de dados de cluster e banco de dados de registro de classe COM+, conforme aplicável.</span><span class="sxs-lookup"><span data-stu-id="037fc-124">Restore SysVol, Certificate Server, Cluster database and COM+ class registration database, as applicable.</span></span>
3.  <span data-ttu-id="037fc-125">Restaure o servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="037fc-125">Restore the Active Directory server.</span></span>
4.  <span data-ttu-id="037fc-126">Restaure o registro.</span><span class="sxs-lookup"><span data-stu-id="037fc-126">Restore the registry.</span></span>

<span data-ttu-id="037fc-127">Para obter mais informações sobre como fazer backup e restaurar os serviços de certificados, consulte [usando as funções de backup e restauração dos serviços de certificados](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span><span class="sxs-lookup"><span data-stu-id="037fc-127">For more information about backing up and restoring Certificate Services, see [Using the Certificate Services Backup and Restore Functions](/windows/desktop/SecCrypto/using-the-certificate-services-backup-and-restore-functions).</span></span>

<span data-ttu-id="037fc-128">Para obter mais informações sobre como fazer backup e restaurar Active Directory Domain Services, consulte:</span><span class="sxs-lookup"><span data-stu-id="037fc-128">For more information about backing up and restoring Active Directory Domain Services, see:</span></span>

-   [<span data-ttu-id="037fc-129">Considerações sobre o backup de Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="037fc-129">Considerations for Active Directory Domain Services Backup</span></span>](considerations-for-active-directory-domain-services-backup.md)
-   [<span data-ttu-id="037fc-130">Fazendo backup de um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="037fc-130">Backing Up an Active Directory Server</span></span>](backing-up-an-active-directory-server.md)
-   [<span data-ttu-id="037fc-131">Restaurando um servidor de Active Directory</span><span class="sxs-lookup"><span data-stu-id="037fc-131">Restoring an Active Directory Server</span></span>](restoring-an-active-directory-server.md)
-   [<span data-ttu-id="037fc-132">Funções de backup de diretório</span><span class="sxs-lookup"><span data-stu-id="037fc-132">Directory Backup Functions</span></span>](directory-backup-functions.md)

 

 