---
description: Ao conectar-se remotamente a um servidor Active Directory diferente daquele em seu domínio atual, você deve especificar o nome de um computador que já seja membro do domínio pertencente ao Active Directory desejado.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Descrevendo o namespace LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011506"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="effbb-103">Descrevendo o namespace LDAP</span><span class="sxs-lookup"><span data-stu-id="effbb-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="effbb-104">Ao conectar-se remotamente a um servidor Active Directory diferente daquele em seu domínio atual, você deve especificar o nome de um computador que já seja membro do domínio pertencente ao Active Directory desejado.</span><span class="sxs-lookup"><span data-stu-id="effbb-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="effbb-105">Para se conectar remotamente a um computador que já é membro do domínio pertencente ao servidor de Active Directory, digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="effbb-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="effbb-106">**\\\\\\ \\ LDAP do diretório raiz do computador_remoto \\**</span><span class="sxs-lookup"><span data-stu-id="effbb-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="effbb-107">Este exemplo mostra que há duas partes que compõem um nome de namespace totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="effbb-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="effbb-108">A primeira parte ( \\ \\ computador_remoto) representa o computador que já é membro do domínio pertencente ao servidor de Active Directory que você deseja.</span><span class="sxs-lookup"><span data-stu-id="effbb-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="effbb-109">A segunda parte ( \\ \\ LDAP do diretório raiz \\ ) representa o esquema de Active Directory no provedor de serviços de diretório.</span><span class="sxs-lookup"><span data-stu-id="effbb-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="effbb-110">Para obter mais informações sobre o suporte e a instalação desse componente em um sistema operacional específico, consulte [disponibilidade do sistema operacional de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="effbb-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



