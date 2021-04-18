---
description: Os terminais conectáveis são classificados em superclasses de terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entradas do registro (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810997"
---
# <a name="registry-entries-telephony-api"></a><span data-ttu-id="cb69f-103">Entradas do registro (API de telefonia)</span><span class="sxs-lookup"><span data-stu-id="cb69f-103">Registry Entries (Telephony API)</span></span>

<span data-ttu-id="cb69f-104">Os terminais conectáveis são classificados em superclasses de terminal.</span><span class="sxs-lookup"><span data-stu-id="cb69f-104">The pluggable terminals are classified into Terminal Superclasses.</span></span> <span data-ttu-id="cb69f-105">Cada superclasse de terminal tem uma entrada no registro sob a seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="cb69f-105">Each Terminal Superclass has an entry in the registry under the following key:</span></span>

<span data-ttu-id="cb69f-106">**HKEY \_ \_Computador local** \\ **software** \\  \\  \\  \\  \\ **terminalmanager** de telefonia do Microsoft Windows CurrentVersion</span><span class="sxs-lookup"><span data-stu-id="cb69f-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Telephony**\\**TerminalManager**</span></span>

<span data-ttu-id="cb69f-107">Abaixo da chave de superclasse de terminal estão entradas para cada terminal conectável na superclasse do terminal.</span><span class="sxs-lookup"><span data-stu-id="cb69f-107">Below the Terminal Superclass key are entries for each pluggable terminal within the Terminal Superclass.</span></span>

<span data-ttu-id="cb69f-108">A entrada para cada superclasse de terminal é identificada por um CLSID de superclasse de terminal.</span><span class="sxs-lookup"><span data-stu-id="cb69f-108">The entry for each Terminal Superclass is identified by a Terminal Superclass CLSID.</span></span> <span data-ttu-id="cb69f-109">Este é um identificador exclusivo para uma classe de terminal.</span><span class="sxs-lookup"><span data-stu-id="cb69f-109">This is a unique identifier for a terminal class.</span></span> <span data-ttu-id="cb69f-110">A classe terminal tem um atributo opcional: Name, que é um nome amigável para a classe terminal.</span><span class="sxs-lookup"><span data-stu-id="cb69f-110">The terminal class has an optional attribute: name, which is a friendly name for the terminal class.</span></span> <span data-ttu-id="cb69f-111">Cada terminal conectável é identificado por uma classe de terminal de CLSID; ou seja, um GUID.</span><span class="sxs-lookup"><span data-stu-id="cb69f-111">Each pluggable terminal is identified by a CLSID Terminal class; that is, a GUID.</span></span> <span data-ttu-id="cb69f-112">Os atributos para terminal conectável são armazenados em valores de chave de terminal conectáveis.</span><span class="sxs-lookup"><span data-stu-id="cb69f-112">The attributes for pluggable terminal are stored into pluggable terminal key values.</span></span> <span data-ttu-id="cb69f-113">Os atributos para um terminal conectável são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="cb69f-113">The attributes for a pluggable terminal are the following.</span></span>



| <span data-ttu-id="cb69f-114">Classe terminal</span><span class="sxs-lookup"><span data-stu-id="cb69f-114">Terminal class</span></span> | <span data-ttu-id="cb69f-115">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="cb69f-115">Key name</span></span> | <span data-ttu-id="cb69f-116">Identificador público</span><span class="sxs-lookup"><span data-stu-id="cb69f-116">Public identifier</span></span>                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cb69f-117">Nome</span><span class="sxs-lookup"><span data-stu-id="cb69f-117">Name</span></span>           | <span data-ttu-id="cb69f-118">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="cb69f-118">REG\_SZ</span></span>  | <span data-ttu-id="cb69f-119">Nome amigável do terminal</span><span class="sxs-lookup"><span data-stu-id="cb69f-119">Terminal friendly name</span></span>                                                            |
| <span data-ttu-id="cb69f-120">Empresa</span><span class="sxs-lookup"><span data-stu-id="cb69f-120">Company</span></span>        | <span data-ttu-id="cb69f-121">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="cb69f-121">REG\_SZ</span></span>  | <span data-ttu-id="cb69f-122">Nome da empresa</span><span class="sxs-lookup"><span data-stu-id="cb69f-122">Company name</span></span>                                                                      |
| <span data-ttu-id="cb69f-123">Versão</span><span class="sxs-lookup"><span data-stu-id="cb69f-123">Version</span></span>        | <span data-ttu-id="cb69f-124">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="cb69f-124">REG\_SZ</span></span>  | <span data-ttu-id="cb69f-125">Informações da versão</span><span class="sxs-lookup"><span data-stu-id="cb69f-125">Version information</span></span>                                                               |
| <span data-ttu-id="cb69f-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb69f-126">CLSID</span></span>          | <span data-ttu-id="cb69f-127">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="cb69f-127">REG\_SZ</span></span>  | <span data-ttu-id="cb69f-128">CLSID de terminal (usado no método COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) )</span><span class="sxs-lookup"><span data-stu-id="cb69f-128">Terminal CLSID (used in COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method)</span></span> |
| <span data-ttu-id="cb69f-129">Instruções</span><span class="sxs-lookup"><span data-stu-id="cb69f-129">Directions</span></span>     | <span data-ttu-id="cb69f-130">DWORD</span><span class="sxs-lookup"><span data-stu-id="cb69f-130">DWORD</span></span>    | <span data-ttu-id="cb69f-131">Direção do terminal</span><span class="sxs-lookup"><span data-stu-id="cb69f-131">Terminal direction</span></span>                                                                |
| <span data-ttu-id="cb69f-132">MediaTypes</span><span class="sxs-lookup"><span data-stu-id="cb69f-132">MediaTypes</span></span>     | <span data-ttu-id="cb69f-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="cb69f-133">DWORD</span></span>    | <span data-ttu-id="cb69f-134">Tipos de mídia de terminal com suporte</span><span class="sxs-lookup"><span data-stu-id="cb69f-134">Terminal media types supported</span></span>                                                    |



 

<span data-ttu-id="cb69f-135">Para uma classe terminal, os atributos são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="cb69f-135">For a terminal class the attributes are the following.</span></span>



| <span data-ttu-id="cb69f-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="cb69f-136">CLSID</span></span> | <span data-ttu-id="cb69f-137">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="cb69f-137">Key name</span></span> | <span data-ttu-id="cb69f-138">Identificador público</span><span class="sxs-lookup"><span data-stu-id="cb69f-138">Public identifier</span></span>            |
|-------|----------|------------------------------|
| <span data-ttu-id="cb69f-139">Nome</span><span class="sxs-lookup"><span data-stu-id="cb69f-139">Name</span></span>  | <span data-ttu-id="cb69f-140">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="cb69f-140">REG\_SZ</span></span>  | <span data-ttu-id="cb69f-141">Nome amigável da classe de terminal</span><span class="sxs-lookup"><span data-stu-id="cb69f-141">Terminal class friendly name</span></span> |



 

 

 
