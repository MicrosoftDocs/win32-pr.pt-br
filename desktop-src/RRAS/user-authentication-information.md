---
title: Informações de autenticação do usuário
description: O serviço do Gerenciador de conexões de acesso remoto no computador cliente envia um nome de usuário e senha para o servidor RAS no computador remoto.
ms.assetid: b27bf520-d871-4314-8ed9-3a6a9583ab52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0cb95d0e941c47deb398c03277013e0e0a35f9d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823804"
---
# <a name="user-authentication-information"></a><span data-ttu-id="c1843-103">Informações de autenticação do usuário</span><span class="sxs-lookup"><span data-stu-id="c1843-103">User Authentication Information</span></span>

<span data-ttu-id="c1843-104">O serviço do Gerenciador de conexões de acesso remoto no computador cliente envia um nome de usuário e senha para o servidor RAS no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="c1843-104">The Remote Access Connection Manager service on the client computer sends a user name and password to the RAS server on the remote computer.</span></span> <span data-ttu-id="c1843-105">Antes de estabelecer uma conexão, o servidor remoto usa essas informações para autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="c1843-105">Before it establishes a connection, the remote server uses this information to authenticate the user.</span></span> <span data-ttu-id="c1843-106">Por padrão, o Gerenciador de conexões de acesso remoto envia o nome de usuário e a senha do usuário conectado no momento.</span><span class="sxs-lookup"><span data-stu-id="c1843-106">By default, the Remote Access Connection Manager sends the user name and password of the currently logged-on user.</span></span> <span data-ttu-id="c1843-107">O cliente RAS pode usar a estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) especificada na chamada [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para especificar um nome de usuário e uma senha diferentes.</span><span class="sxs-lookup"><span data-stu-id="c1843-107">The RAS client can use the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure specified in the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call to specify a different user name and password.</span></span>

<span data-ttu-id="c1843-108">Se o servidor remoto não puder autenticar o usuário com as informações especificadas, ele poderá permitir que a operação de conexão entre em um [estado de pausa](paused-states.md) para permitir que o cliente RAS colete dados de autenticação diferentes do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1843-108">If the remote server cannot authenticate the user with the specified information, it can allow the connection operation to enter a [paused state](paused-states.md) to enable the RAS client to collect different authentication data from the user.</span></span>

 

 