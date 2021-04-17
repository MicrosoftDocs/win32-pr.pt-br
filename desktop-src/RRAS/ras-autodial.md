---
title: Discagem automática de RAS
description: Um recurso chamado \ 0034; conexão padrão \ 0034; foi adicionado ao sistema no Windows XP.
ms.assetid: 8ef832ed-97e4-4941-adb2-b35ce3a75fd1
keywords:
- Discagem automática, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc2da449b91dd34165038b8d9f07b73926a943a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105775659"
---
# <a name="ras-autodial"></a><span data-ttu-id="8746e-104">Discagem automática de RAS</span><span class="sxs-lookup"><span data-stu-id="8746e-104">RAS AutoDial</span></span>

<span data-ttu-id="8746e-105">Um recurso chamado "conexão padrão" foi adicionado ao sistema no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8746e-105">A feature called "default connection" was added to the system in Windows XP.</span></span> <span data-ttu-id="8746e-106">Se houver uma falha na tentativa de conexão, o sistema verificará se há uma correspondência explícita (para nome do Winsock ou nome do compartilhamento) no banco de dados, se não, ele discará a conexão padrão se houver uma.</span><span class="sxs-lookup"><span data-stu-id="8746e-106">If there is a failed connection attempt, the system checks for an explicit match (for Winsock name or share name) in the database if not, it dials the default connection if there is one.</span></span>

<span data-ttu-id="8746e-107">**Windows 2000:** Quando uma tentativa de conexão com um endereço de rede falha porque o host não pode ser acessado, o recurso de discagem automática pode iniciar automaticamente uma operação de conexão discada.</span><span class="sxs-lookup"><span data-stu-id="8746e-107">**Windows 2000:** When an attempt to connect to a network address fails because the host cannot be reached, the AutoDial feature can automatically start a dial-up connection operation.</span></span> <span data-ttu-id="8746e-108">Para fazer isso, a discagem automática pesquisa seu banco de dados de endereços de rede para localizar uma entrada de catálogo telefônico que pode ser usada para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="8746e-108">To do this, AutoDial searches its database of network addresses to find a phone-book entry that it can use to establish the connection.</span></span>

<span data-ttu-id="8746e-109">**Windows NT 4,0:  ** O RAS mantém um banco de dados dos nomes do Winsock e/ou dos nomes de compartilhamento que você atingiu com êxito enquanto uma conexão RAS/VPN estava ativa.</span><span class="sxs-lookup"><span data-stu-id="8746e-109">**Windows NT 4.0:  ** RAS keeps a database of the Winsock names and/or share names that you have successfully reached while a RAS/VPN connection was active.</span></span> <span data-ttu-id="8746e-110">Posteriormente, quando uma tentativa de conexão Winsock ou compartilhar falha, o sistema verifica esse banco de dados e oferece para discar a conexão armazenada para você.</span><span class="sxs-lookup"><span data-stu-id="8746e-110">Later, when a winsock or share connection attempt fails, the system checks this database and offers to dial the stored connection for you.</span></span>

 

 




