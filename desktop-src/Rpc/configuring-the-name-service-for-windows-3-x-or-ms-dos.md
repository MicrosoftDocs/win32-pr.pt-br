---
title: Configurando o serviço de nome para Windows 3. x ou MS-DOS
description: RPC (chamada de procedimento remoto) e configuração do serviço de nome para Windows 3. x ou MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005674"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="1b3fe-103">Configurando o serviço de nome para Windows 3. x ou MS-DOS</span><span class="sxs-lookup"><span data-stu-id="1b3fe-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="1b3fe-104">Quando você executa Setup.exe para instalar a biblioteca de tempo de execução RPC de 16 bits, ele solicita que você selecione um provedor de serviços de nome:</span><span class="sxs-lookup"><span data-stu-id="1b3fe-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="1b3fe-105">Se você escolher **instalar provedor de serviço de nome padrão**, o NSP padrão, Microsoft Locator, será instalado.</span><span class="sxs-lookup"><span data-stu-id="1b3fe-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="1b3fe-106">Se você escolher **instalar provedor de serviço de nome personalizado**, conclua a caixa de diálogo **Definir endereço de rede** para instalar o serviço de diretório de célula do DCE como seu NSP.</span><span class="sxs-lookup"><span data-stu-id="1b3fe-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="1b3fe-107">O serviço de diretório de célula do DCE é o NSP usado com servidores DCE.</span><span class="sxs-lookup"><span data-stu-id="1b3fe-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="1b3fe-108">O endereço de rede é o nome do computador host que executa o daemon de NSI (nsid).</span><span class="sxs-lookup"><span data-stu-id="1b3fe-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="1b3fe-109">Esse computador atua como um gateway para o serviço de diretório de célula do DCE, passando chamadas de função de NSI entre computadores que executam sistemas operacionais Microsoft e computadores DCE.</span><span class="sxs-lookup"><span data-stu-id="1b3fe-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="1b3fe-110">O endereço de rede pode ter de 80 caracteres ou menos — por exemplo, 11.1.9.169 é um endereço válido.</span><span class="sxs-lookup"><span data-stu-id="1b3fe-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




