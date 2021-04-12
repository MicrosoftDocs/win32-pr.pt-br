---
description: Um provedor de serviços de mídia deve implementar um subconjunto mínimo de interfaces MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Gravando um provedor de serviços de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297882"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="888ef-103">Gravando um provedor de serviços de mídia</span><span class="sxs-lookup"><span data-stu-id="888ef-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="888ef-104">Um provedor de serviços de mídia deve implementar um subconjunto mínimo de interfaces MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="888ef-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="888ef-105">O suporte a Subfluxo é opcional.</span><span class="sxs-lookup"><span data-stu-id="888ef-105">SubStream support is optional.</span></span> <span data-ttu-id="888ef-106">Além disso, um determinado MSP pode implementar métodos adicionais, como os controles necessários para hardware especializado.</span><span class="sxs-lookup"><span data-stu-id="888ef-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="888ef-107">Os seguintes documentos materiais:</span><span class="sxs-lookup"><span data-stu-id="888ef-107">The following material documents:</span></span>

-   <span data-ttu-id="888ef-108">As [classes base TAPI 3 MSP](tapi-3-msp-base-classes.md), que são um conjunto de classes C++ projetadas para simplificar a tarefa de criar um MSP baseado em DirectShow.</span><span class="sxs-lookup"><span data-stu-id="888ef-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="888ef-109">As classes base implementam todas as interfaces MSPI de maneira genérica.</span><span class="sxs-lookup"><span data-stu-id="888ef-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="888ef-110">Diferentes MSPs podem substituir funções específicas do MSP e fornecer suas próprias implementações.</span><span class="sxs-lookup"><span data-stu-id="888ef-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="888ef-111">O [Gerenciador de terminal TAPI 3](tapi-3-terminal-manager.md), que fornece interfaces e métodos usados por um msp para controlar os terminais.</span><span class="sxs-lookup"><span data-stu-id="888ef-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="888ef-112">[Terminais conectáveis](writing-a-pluggable-terminal.md), que permitem a um aplicativo em vez de um MSP criar terminais.</span><span class="sxs-lookup"><span data-stu-id="888ef-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="888ef-113">Os desenvolvedores que já tiverem experiência em escrever provedores de serviços serão os principais criadores de terminais conectáveis.</span><span class="sxs-lookup"><span data-stu-id="888ef-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="888ef-114">A versão inicial implementada para esta versão destina-se a aplicativos de servidor de conferência que precisam adicionar clientes que não são do Windows 2000 ou não multicast a conferências multifuncionais de antivírus/IP de terceiros da TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="888ef-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 
