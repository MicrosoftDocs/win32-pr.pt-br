---
title: Entidades de segurança
description: No Windows 2000, uma entidade de segurança é um usuário, grupo ou computador \ 8212; uma entidade que o sistema de segurança reconhece.
ms.assetid: 213ee563-35cd-43d2-abb2-f66652df5be1
ms.tgt_platform: multiple
keywords:
- ANÚNCIO das entidades de segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877ed77b365fa4a61444e4936dbe859379ee397
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105762806"
---
# <a name="security-principals"></a><span data-ttu-id="39220-104">Entidades de segurança</span><span class="sxs-lookup"><span data-stu-id="39220-104">Security Principals</span></span>

<span data-ttu-id="39220-105">No Windows 2000, uma entidade de segurança é um usuário, um grupo ou um computador — uma pessoa que o sistema de segurança reconhece.</span><span class="sxs-lookup"><span data-stu-id="39220-105">In Windows 2000, a security principal is a user, group, or computer — an entity that the security system recognizes.</span></span> <span data-ttu-id="39220-106">Isso inclui usuários humanos, bem como processos autônomos.</span><span class="sxs-lookup"><span data-stu-id="39220-106">This includes human users as well as autonomous processes.</span></span> <span data-ttu-id="39220-107">Estritamente falando, o sistema de segurança não pode informar a diferença entre os usuários que estão conectados e os processos em execução no computador.</span><span class="sxs-lookup"><span data-stu-id="39220-107">Strictly speaking, the security system cannot tell the difference between users who are logged in and processes running on the computer.</span></span> <span data-ttu-id="39220-108">Ele vê tanto como entidades de segurança com nomes de entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="39220-108">It sees both as security principals with security principal names.</span></span>

<span data-ttu-id="39220-109">Usuários, grupos e computadores são criados e armazenados como objetos no Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="39220-109">Users, groups, and computers are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="39220-110">Também há entidades de segurança bem conhecidas que representam identidades especiais definidas pelo sistema de segurança do Windows 2000, como todos, sistema local, principal, usuário autenticado, proprietário criador e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="39220-110">There are also well-known security principals that represent special identities defined by the Windows 2000 security system, such as Everyone, Local System, Principal Self, Authenticated User, Creator Owner, and so on.</span></span> <span data-ttu-id="39220-111">Os objetos que representam as entidades de segurança conhecidas, como logon anônimo, são armazenados no contêiner de entidades de segurança do WellKnown sob o contêiner de configuração.</span><span class="sxs-lookup"><span data-stu-id="39220-111">Objects representing the well-known security principals, such as Anonymous Logon, are stored in the WellKnown Security Principals container beneath the Configuration container.</span></span>

 

 




