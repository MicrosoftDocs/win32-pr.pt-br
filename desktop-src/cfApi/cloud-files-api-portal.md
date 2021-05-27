---
description: A API de Filtro de Nuvem fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Mecanismos de sincronização de nuvem
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549591"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="634ce-103">Mecanismos de sincronização de nuvem</span><span class="sxs-lookup"><span data-stu-id="634ce-103">Cloud Sync Engines</span></span>

<span data-ttu-id="634ce-104">Consulte também [Exemplo de Espelhamento de Nuvem.](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)</span><span class="sxs-lookup"><span data-stu-id="634ce-104">Also see [Cloud Mirror sample](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span></span>

<span data-ttu-id="634ce-105">A partir do Windows 10, versão 1709, o Windows fornece a *API de arquivos de nuvem*.</span><span class="sxs-lookup"><span data-stu-id="634ce-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="634ce-106">Essa API consiste em várias APIs win32 e WinRT nativas que formalizam o suporte para mecanismos de sincronização de nuvem e lidam com tarefas como criar e gerenciar arquivos e diretórios de espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="634ce-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="634ce-107">Os usuários dessa API normalmente são provedores de sincronização e, até certo ponto, aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="634ce-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="634ce-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="634ce-108">In this section</span></span>

| <span data-ttu-id="634ce-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="634ce-109">Topic</span></span>                                                                | <span data-ttu-id="634ce-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="634ce-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="634ce-111">Criar um Mecanismo de Sincronização de Nuvem que dá suporte a arquivos de espaço reservado</span><span class="sxs-lookup"><span data-stu-id="634ce-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="634ce-112">Saiba como usar a API de arquivos de nuvem para criar um mecanismo de sincronização de arquivos de nuvem que inclui arquivos de espaço reservado e Explorador de Arquivos integração.</span><span class="sxs-lookup"><span data-stu-id="634ce-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="634ce-113">Referência de filtro de nuvem</span><span class="sxs-lookup"><span data-stu-id="634ce-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="634ce-114">A API de filtro de nuvem é uma API nativa do Win32 que faz parte da API de arquivos de nuvem mais ampla.</span><span class="sxs-lookup"><span data-stu-id="634ce-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="634ce-115">A API de filtro de nuvem fornece funcionalidade no limite entre o modo de usuário e o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="634ce-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="634ce-116">Essa API lida com a criação e o gerenciamento de arquivos e diretórios de espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="634ce-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |