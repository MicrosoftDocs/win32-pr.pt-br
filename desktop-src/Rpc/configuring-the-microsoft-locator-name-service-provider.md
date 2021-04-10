---
title: Configurando o provedor de serviços do Microsoft Locator Name
description: Você pode alterar o nome do provedor de serviços especificado editando o arquivo de configuração Rpcreg. dat, que contém os parâmetros NSP e as configurações do Protocolo RPC. Use um editor de texto para alterar as entradas NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292377"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a><span data-ttu-id="f3dbf-104">Configurando o provedor de serviços do Microsoft Locator Name</span><span class="sxs-lookup"><span data-stu-id="f3dbf-104">Configuring the Microsoft Locator Name Service Provider</span></span>

<span data-ttu-id="f3dbf-105">Você pode alterar o nome do provedor de serviços especificado editando o arquivo de configuração Rpcreg. dat, que contém os parâmetros NSP e as configurações do Protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-105">You can change the name service provider you specified by editing the Rpcreg.dat configuration file, which contains the NSP parameters and RPC protocol settings.</span></span> <span data-ttu-id="f3dbf-106">Use um editor de texto para alterar as entradas NSP.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-106">Use a text editor to change NSP entries.</span></span>

<span data-ttu-id="f3dbf-107">**Para reconfigurar o provedor de serviços do Microsoft Locator Name**</span><span class="sxs-lookup"><span data-stu-id="f3dbf-107">**To reconfigure the Microsoft Locator name service provider**</span></span>

1.  <span data-ttu-id="f3dbf-108">Abra o arquivo Rpcreg. dat usando um editor de texto.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-108">Open the Rpcreg.dat file using a text editor.</span></span>

    <span data-ttu-id="f3dbf-109">Rpcreg. dat está no diretório raiz, a menos que você tenha especificado um caminho diferente durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-109">Rpcreg.dat is in the root directory unless you specified a different path during setup.</span></span>

2.  <span data-ttu-id="f3dbf-110">Defina os valores a seguir para as entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-110">Set the following values for the registry entries.</span></span> 

    | <span data-ttu-id="f3dbf-111">Entrada de registro</span><span class="sxs-lookup"><span data-stu-id="f3dbf-111">Registry entry</span></span>                                         | <span data-ttu-id="f3dbf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f3dbf-112">Value</span></span>                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f3dbf-113">Protocolo de software \\ RPC da Microsoft \\ \\ NameService \\</span><span class="sxs-lookup"><span data-stu-id="f3dbf-113">Software\\Microsoft\\RPC \\NameService\\Protocol</span></span>       | <span data-ttu-id="f3dbf-114">A sequência de protocolo para o protocolo que você está usando.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-114">The protocol sequence for the protocol you are using.</span></span> <span data-ttu-id="f3dbf-115">O padrão é **ncacn \_ NP**.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-115">The default is **ncacn\_np**.</span></span>                                                                   |
    | <span data-ttu-id="f3dbf-116">Software \\ Microsoft \\ RPC \\ NameService \\ networkaddress</span><span class="sxs-lookup"><span data-stu-id="f3dbf-116">Software\\Microsoft\\RPC\\ NameService\\NetworkAddress</span></span> | <span data-ttu-id="f3dbf-117">O nome do computador que está executando o localizador que é usado por clientes durante operações de pesquisa de serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-117">The name of the computer running Locator that is used by clients during name service lookup operations.</span></span> <span data-ttu-id="f3dbf-118">O padrão é o controlador de domínio primário.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-118">The default is the primary domain controller.</span></span> |
    | <span data-ttu-id="f3dbf-119">Software \\ Microsoft \\ RPC \\ NameService \\ Endpoint</span><span class="sxs-lookup"><span data-stu-id="f3dbf-119">Software\\Microsoft\\RPC\\ NameService\\Endpoint</span></span>       | <span data-ttu-id="f3dbf-120">O nome do ponto de extremidade usado pelo serviço de nome.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-120">The name of the endpoint used by the name service.</span></span> <span data-ttu-id="f3dbf-121">O padrão é \\ \\ localizador de pipe.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-121">The default is \\pipe\\locator.</span></span>                                                                    |

    

     

3.  <span data-ttu-id="f3dbf-122">Salve e feche o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f3dbf-122">Save and close the file.</span></span>

 

 




