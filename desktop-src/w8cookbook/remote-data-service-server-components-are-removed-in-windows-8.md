---
title: Serviço de dados remoto removido
description: Os componentes do servidor do serviço de dados remoto são removidos do Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Servidor RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103917746"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="774cf-104">Os componentes do servidor do serviço de dados remoto são removidos do Windows 8</span><span class="sxs-lookup"><span data-stu-id="774cf-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="774cf-105">Plataformas</span><span class="sxs-lookup"><span data-stu-id="774cf-105">Platforms</span></span>

 <span data-ttu-id="774cf-106">**Clientes** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="774cf-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="774cf-107">**Servidores** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="774cf-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="774cf-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="774cf-108">Description</span></span>

<span data-ttu-id="774cf-109">O servidor RDS (serviço de dados remotos) não está disponível no Windows 8:</span><span class="sxs-lookup"><span data-stu-id="774cf-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="774cf-110">O arquivo msadcf.dll, que hospeda o "objeto comercial" padrão RDSServer. datafactory, é removido e seus arquivos associados (msadcfr.dll, msadcfr.dll. mui, Handler. reg e handsafe. reg) são removidos</span><span class="sxs-lookup"><span data-stu-id="774cf-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="774cf-111">O arquivo msdfmap.dll, que é o manipulador padrão, é removido e o msdfmap.ini de arquivo é removido</span><span class="sxs-lookup"><span data-stu-id="774cf-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="774cf-112">O arquivo msadcs.dll, ISAPI, é removido</span><span class="sxs-lookup"><span data-stu-id="774cf-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="774cf-113">Manifestação</span><span class="sxs-lookup"><span data-stu-id="774cf-113">Manifestation</span></span>

<span data-ttu-id="774cf-114">Os clientes não podem hospedar um servidor RDS no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="774cf-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="774cf-115">Atenuação</span><span class="sxs-lookup"><span data-stu-id="774cf-115">Mitigation</span></span>

<span data-ttu-id="774cf-116">Os clientes podem manter seu servidor RDS em um computador com o Windows 7 ou outros sistemas operacionais de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="774cf-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="774cf-117">Solução</span><span class="sxs-lookup"><span data-stu-id="774cf-117">Solution</span></span>

<span data-ttu-id="774cf-118">Os clientes podem manter seu servidor RDS em um computador com o Windows 7 ou outros sistemas operacionais de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="774cf-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="774cf-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="774cf-119">Resources</span></span>

[<span data-ttu-id="774cf-120">Roteiro de tecnologias de acesso a dados</span><span class="sxs-lookup"><span data-stu-id="774cf-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 