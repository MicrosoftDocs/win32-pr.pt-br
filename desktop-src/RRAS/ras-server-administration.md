---
title: Administração do servidor RAS
description: O Windows NT Server 4,0 fornece um conjunto de funções para administrar permissões e portas de usuário em servidores Windows NT/Windows 2000 RAS.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Administração do servidor, RAS
- Administração, servidor RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160263"
---
# <a name="ras-server-administration"></a><span data-ttu-id="8bf56-105">Administração do servidor RAS</span><span class="sxs-lookup"><span data-stu-id="8bf56-105">RAS Server Administration</span></span>

<span data-ttu-id="8bf56-106">O Windows NT Server 4,0 fornece um conjunto de funções para administrar permissões e portas de usuário em servidores Windows NT/Windows 2000 RAS.</span><span class="sxs-lookup"><span data-stu-id="8bf56-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="8bf56-107">O Windows 95 não oferece suporte a essas funções.</span><span class="sxs-lookup"><span data-stu-id="8bf56-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="8bf56-108">Usando essas funções, você pode desenvolver um aplicativo de administração de servidor RAS para executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="8bf56-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="8bf56-109">Enumerar os usuários que têm um conjunto especificado de permissões de RAS</span><span class="sxs-lookup"><span data-stu-id="8bf56-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="8bf56-110">Atribuir ou revogar permissões RAS para um usuário especificado</span><span class="sxs-lookup"><span data-stu-id="8bf56-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="8bf56-111">Enumerar as portas configuradas em um servidor RAS</span><span class="sxs-lookup"><span data-stu-id="8bf56-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="8bf56-112">Obter informações e estatísticas sobre uma porta especificada em um servidor RAS</span><span class="sxs-lookup"><span data-stu-id="8bf56-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="8bf56-113">Redefinir os contadores de estatísticas para uma porta especificada</span><span class="sxs-lookup"><span data-stu-id="8bf56-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="8bf56-114">Desconectar uma porta especificada</span><span class="sxs-lookup"><span data-stu-id="8bf56-114">Disconnect a specified port</span></span>

<span data-ttu-id="8bf56-115">Você também pode instalar uma DLL de administração de servidor RAS para auditar conexões de usuário e atribuir endereços IP a usuários de discagem.</span><span class="sxs-lookup"><span data-stu-id="8bf56-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="8bf56-116">A DLL exporta um conjunto de funções que o servidor RAS chama sempre que um usuário tenta se conectar ou se desconectar.</span><span class="sxs-lookup"><span data-stu-id="8bf56-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 




