---
description: Depois de criar o provedor de rede ou o Gerenciador de credenciais, você deve registrá-lo no sistema.
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: Registrando provedores de rede e gerenciadores de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169825"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="5bb48-103">Registrando provedores de rede e gerenciadores de credenciais</span><span class="sxs-lookup"><span data-stu-id="5bb48-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="5bb48-104">Depois de criar o provedor de rede ou o Gerenciador de credenciais, você deve registrá-lo no sistema.</span><span class="sxs-lookup"><span data-stu-id="5bb48-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="5bb48-105">Isso é necessário para que o MPR saiba quais provedores de rede estão instalados.</span><span class="sxs-lookup"><span data-stu-id="5bb48-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="5bb48-106">Quando o MPR é iniciado, ele verifica o registro e carrega os provedores de rede ou os gerenciadores de credenciais encontrados.</span><span class="sxs-lookup"><span data-stu-id="5bb48-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="5bb48-107">Como os provedores de rede e os gerenciadores de credenciais estão relacionados, eles são registrados nas mesmas subchaves do registro.</span><span class="sxs-lookup"><span data-stu-id="5bb48-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="5bb48-108">Na verdade, as DLLs do provedor de rede também podem ser gerenciadores de credenciais.</span><span class="sxs-lookup"><span data-stu-id="5bb48-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="5bb48-109">Para obter informações detalhadas sobre as chaves do registro que você deve criar para o provedor de rede ou o Gerenciador de credenciais, consulte [chaves do registro de autenticação](authentication-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="5bb48-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



