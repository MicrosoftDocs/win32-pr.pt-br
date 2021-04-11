---
title: Grupos em servidores membros e no Windows 2000 Professional
description: Em servidores membros e computadores em execução no Windows 2000 Professional, há um banco de dados de segurança local.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Grupos em servidores membros e AD do Windows 2000 Professional
- grupos de anúncios, grupos em servidores membros e Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291810"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="30179-105">Grupos em servidores membros e no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="30179-105">Groups on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="30179-106">Em servidores membros e computadores em execução no Windows 2000 Professional, há um banco de dados de segurança local.</span><span class="sxs-lookup"><span data-stu-id="30179-106">On member servers and computers running on Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="30179-107">Esse banco de dados de segurança local pode conter seu próprio usuário local e grupos locais cujo escopo é apenas o computador em que eles são criados.</span><span class="sxs-lookup"><span data-stu-id="30179-107">This local security database can contain its own local user and local groups whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="30179-108">Ao gerenciar esses tipos de usuários e grupos em servidores membros e computadores em execução no Windows NT Workstation ou no Windows 2000 Professional, use o provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="30179-108">When managing these types of users and groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="30179-109">Quando um servidor membro ou um computador que executa o Windows 2000 Professional ou o Windows 2000 Professional é membro de um domínio do Windows 2000, os grupos ou usuários no domínio podem ser usados no banco de dados de segurança local para conceder direitos a esse grupo nesse computador específico.</span><span class="sxs-lookup"><span data-stu-id="30179-109">When a member server or a computer running on Windows 2000 Professional or Windows 2000 Professional is a member of a Windows 2000 domain, the groups or users in the domain can be used in the local security database to grant rights to that group on that particular computer.</span></span>

<span data-ttu-id="30179-110">Ao gerenciar grupos em um domínio do Windows 2000 usando ADSI, use o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="30179-110">When managing groups on a Windows 2000 domain using ADSI, use the LDAP provider.</span></span> <span data-ttu-id="30179-111">Ao gerenciar grupos em servidores membros e computadores em execução no Windows NT Workstation ou no Windows 2000 Professional, use o provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="30179-111">When managing groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="30179-112">Você deve associar, pelo menos uma instância, a cada provedor: 1) associar ao provedor LDAP para recuperar o ADsPath para o grupo ou usuário que você deseja adicionar a um grupo no banco de dados local e 2) associar ao provedor WinNT para adicionar esse usuário ou grupo a um grupo local.</span><span class="sxs-lookup"><span data-stu-id="30179-112">You must bind, at least one instance, to each provider: 1) Bind to the LDAP provider to retrieve the ADsPath to the group or user you want to add to a group in the local database and 2) Bind to the WinNT provider to add that user or group to a local group.</span></span>

 

 




