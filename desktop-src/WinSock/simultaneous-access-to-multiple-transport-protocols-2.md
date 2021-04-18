---
description: Um protocolo de transporte deve ser instalado corretamente no sistema e registrado com o Windows Sockets para ser acessível a um aplicativo.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Acesso simultâneo a vários protocolos de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781460"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="ea190-103">Acesso simultâneo a vários protocolos de transporte</span><span class="sxs-lookup"><span data-stu-id="ea190-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="ea190-104">Um protocolo de transporte deve ser instalado corretamente no sistema e registrado com o Windows Sockets para ser acessível a um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea190-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="ea190-105">A \_ biblioteca de32.dll Ws2 exporta um conjunto de funções para facilitar o processo de registro.</span><span class="sxs-lookup"><span data-stu-id="ea190-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="ea190-106">Isso inclui a criação de um novo registro e a remoção de um existente.</span><span class="sxs-lookup"><span data-stu-id="ea190-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="ea190-107">Quando novos registros são criados, o chamador (ou seja, o script de instalação do fornecedor da pilha) fornece uma ou mais estruturas [**de \_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) preenchidas contendo um conjunto completo de informações sobre o protocolo.</span><span class="sxs-lookup"><span data-stu-id="ea190-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="ea190-108">Para obter mais informações, consulte [SPI do Windows Sockets 2](about-the-winsock-spi.md).</span><span class="sxs-lookup"><span data-stu-id="ea190-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="ea190-109">Qualquer pilha de transporte instalada dessa maneira é conhecida como um provedor de serviços do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="ea190-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="ea190-110">No Windows XP com Service Pack 2 (SP2), Windows Server 2003 com Service Pack 1 (SP1) e Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="ea190-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="ea190-111">o catálogo Winsock que contém uma lista de provedores de transporte e de namespace instalados pode ser exibido em um prompt de comando com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ea190-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="ea190-112">**netsh winsock mostrar catálogo**</span><span class="sxs-lookup"><span data-stu-id="ea190-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="ea190-113">O SDK (Software Development Kit) do Microsoft Windows inclui *Sporder.exe*, que permite ao usuário exibir e modificar a ordem em que os provedores de serviço são enumerados.</span><span class="sxs-lookup"><span data-stu-id="ea190-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="ea190-114">Usando *Sporder.exe*, um usuário pode estabelecer manualmente uma pilha de protocolo TCP/IP específica como o provedor TCP/IP padrão se mais de uma dessas pilhas estiver presente.</span><span class="sxs-lookup"><span data-stu-id="ea190-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="ea190-115">O aplicativo *Sporder.exe* usa funções exportadas de *Sporder.dll* para reordenar os provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="ea190-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="ea190-116">Como resultado, os aplicativos de instalação podem usar a interface fornecida pelo *Sporder.dll* para reordenar programaticamente os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="ea190-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="ea190-117">Protocolos em camadas e cadeias de protocolos</span><span class="sxs-lookup"><span data-stu-id="ea190-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="ea190-118">Usando vários protocolos</span><span class="sxs-lookup"><span data-stu-id="ea190-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="ea190-119">Restrições de vários provedores em Select</span><span class="sxs-lookup"><span data-stu-id="ea190-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 
