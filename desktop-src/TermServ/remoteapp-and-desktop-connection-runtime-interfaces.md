---
title: Conexão de RemoteApp e Área de Trabalho interfaces de tempo de execução
description: Dá suporte a interfaces que permitem o desenvolvimento de clientes personalizados no Conexão de RemoteApp e Área de Trabalho.
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, Conexão de RemoteApp e Área de Trabalho referência da API de tempo de execução
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084193"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="ccc57-104">Conexão de RemoteApp e Área de Trabalho interfaces de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="ccc57-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="ccc57-105">A API de tempo de execução Conexão de RemoteApp e Área de Trabalho dá suporte a interfaces que permitem o desenvolvimento de clientes personalizados no Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccc57-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ccc57-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="ccc57-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ccc57-107">**IWorkspace**</span><span class="sxs-lookup"><span data-stu-id="ccc57-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="ccc57-108">Expõe métodos que fornecem informações sobre uma conexão no Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccc57-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="ccc57-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="ccc57-110">Expõe métodos adicionais que fornecem informações sobre uma conexão no Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccc57-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="ccc57-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="ccc57-112">Expõe métodos que fornecem informações sobre uma conexão em Conexão de RemoteApp e Área de Trabalho e adiciona a capacidade de recuperar ou definir um token de declarações.</span><span class="sxs-lookup"><span data-stu-id="ccc57-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-113">**IWorkspaceClientExt**</span><span class="sxs-lookup"><span data-stu-id="ccc57-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="ccc57-114">Expõe métodos que permitem ao tempo de execução desconectar um cliente personalizado no Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccc57-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-115">**IWorkspaceRegistration**</span><span class="sxs-lookup"><span data-stu-id="ccc57-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="ccc57-116">Expõe métodos que adicionam e removem referências a clientes personalizados no Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccc57-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="ccc57-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="ccc57-118">Expõe métodos que adicionam e removem referências a clientes personalizados no Conexão de RemoteApp e Área de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="ccc57-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-119">**IWorkspaceReportMessage**</span><span class="sxs-lookup"><span data-stu-id="ccc57-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="ccc57-120">Expõe métodos que dão suporte ao tratamento de mensagens de erro para espaços de trabalho remotos.</span><span class="sxs-lookup"><span data-stu-id="ccc57-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-121">**IWorkspaceResTypeRegistry**</span><span class="sxs-lookup"><span data-stu-id="ccc57-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="ccc57-122">Expõe métodos que permitem que um plug-in gerencie extensões de nome de arquivo de terceiros no Conexão de RemoteApp e Área de Trabalho Runtime.</span><span class="sxs-lookup"><span data-stu-id="ccc57-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-123">**IWorkspaceScriptable**</span><span class="sxs-lookup"><span data-stu-id="ccc57-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="ccc57-124">Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões.</span><span class="sxs-lookup"><span data-stu-id="ccc57-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="ccc57-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="ccc57-126">Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões.</span><span class="sxs-lookup"><span data-stu-id="ccc57-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="ccc57-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ccc57-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="ccc57-128">Expõe métodos que gerenciam credenciais de Conexão de RemoteApp e Área de Trabalho e conexões.</span><span class="sxs-lookup"><span data-stu-id="ccc57-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




