---
title: Controlando intervalos modificados de um arquivo
description: Controlando intervalos modificados de um arquivo
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664e7a5c0a9148471d2a1a28f2881e1c375089c1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105773100"
---
# <a name="tracking-modified-ranges-of-a-file"></a><span data-ttu-id="c4200-103">Controlando intervalos modificados de um arquivo</span><span class="sxs-lookup"><span data-stu-id="c4200-103">Tracking modified ranges of a file</span></span>

## <a name="platforms"></a><span data-ttu-id="c4200-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="c4200-104">Platforms</span></span>

<span data-ttu-id="c4200-105">**Clientes-** Windows 8.1 (todas as SKUs)</span><span class="sxs-lookup"><span data-stu-id="c4200-105">**Clients -** Windows 8.1 (all SKUs)</span></span>  
<span data-ttu-id="c4200-106">**Servidores-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c4200-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="c4200-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4200-107">Description</span></span>

<span data-ttu-id="c4200-108">A equipe do sistema de arquivos NT (NTFS) adicionou um novo recurso ao Windows.</span><span class="sxs-lookup"><span data-stu-id="c4200-108">The NT File System (NTFS) team has added a new feature to Windows.</span></span> <span data-ttu-id="c4200-109">O diário de USN produzirá um registro USN (número de sequência de atualização) contendo intervalos modificados para um arquivo após o fechamento.</span><span class="sxs-lookup"><span data-stu-id="c4200-109">USN Journal will output an update sequence number (USN) record containing modified ranges for a file upon close.</span></span> <span data-ttu-id="c4200-110">Um novo tipo de registro, \_ registro USN \_ v4, foi introduzido para registrar esses intervalos alterados de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4200-110">A new record type, USN\_RECORD\_V4 has been introduced to record these changed ranges of a file.</span></span>

<span data-ttu-id="c4200-111">O recurso não está habilitado por padrão; os usuários devem invocar um comando de controle do sistema de arquivos (FSCTL) para habilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="c4200-111">The feature is not enabled by default; users must invoke a file system control (FSCTL) command to enable it.</span></span> <span data-ttu-id="c4200-112">No entanto, como outros componentes do Windows podem ativar o controle de intervalo, os usuários e desenvolvedores podem perceber que o recurso está sempre habilitado.</span><span class="sxs-lookup"><span data-stu-id="c4200-112">However, because other Windows components may turn on range tracking, users and developers may perceive that the feature is always enabled.</span></span> <span data-ttu-id="c4200-113">O Windows permitirá que os desenvolvedores consultem o diário de USN para descobrir se o rastreamento de intervalo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="c4200-113">Windows will allow developers to query USN journal to find out if range tracking is enabled.</span></span>

<span data-ttu-id="c4200-114">A documentação do MSDN será fornecida em uma data posterior para instruir os desenvolvedores em como \_ acessar \_ registros v4 de registro USN.</span><span class="sxs-lookup"><span data-stu-id="c4200-114">MSDN documentation will be provided at a later date to instruct developers in how to access USN\_RECORD\_V4 records.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c4200-115">Manifestação</span><span class="sxs-lookup"><span data-stu-id="c4200-115">Manifestation</span></span>

<span data-ttu-id="c4200-116">Todos os aplicativos existentes que usam o diário de USN continuarão funcionando bem sem problemas de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="c4200-116">All existing applications that use USN Journal will continue to work well without any compatibility issues.</span></span>

 

 




