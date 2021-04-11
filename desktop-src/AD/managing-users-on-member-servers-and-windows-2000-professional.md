---
title: Gerenciando usuários em servidores membros e no Windows 2000 Professional
description: Em servidores membros e no Windows 2000 Professional, há um banco de dados de segurança local.
ms.assetid: eb0b793b-b33f-4200-af1e-3b72e7478af2
ms.tgt_platform: multiple
keywords:
- AD de usuários, gerenciando um usuário em servidores membros e no Windows 2000 Professional
- Active Directory, usando, usuários, gerenciando um usuário em servidores membros e no Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450ee7ae5a3e4a9d0af08a54de5002f0f6043f5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159314"
---
# <a name="managing-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="2b719-105">Gerenciando usuários em servidores membros e no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2b719-105">Managing Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="2b719-106">Em servidores membros e no Windows 2000 Professional, há um banco de dados de segurança local.</span><span class="sxs-lookup"><span data-stu-id="2b719-106">On member servers and Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="2b719-107">Esse banco de dados de segurança local pode conter seus próprios usuários locais cujo escopo é apenas o computador em que eles são criados.</span><span class="sxs-lookup"><span data-stu-id="2b719-107">That local security database can contain its own local users whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="2b719-108">Ao gerenciar esses tipos de usuários em estações de trabalho e servidores membros, você usa o provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="2b719-108">When managing these types of users on member servers and workstations, you use the WinNT provider.</span></span>

<span data-ttu-id="2b719-109">Ao gerenciar usuários em um domínio do Windows 2000 usando ADSI, você usa o provedor LDAP.</span><span class="sxs-lookup"><span data-stu-id="2b719-109">When managing users on a Windows 2000 domain using ADSI, you use the LDAP provider.</span></span> <span data-ttu-id="2b719-110">Ao gerenciar usuários em estações de trabalho e servidores membros, você usa o provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="2b719-110">When managing users on member servers and workstations, you use the WinNT provider.</span></span>

 

 




