---
title: Configurando a loja online inicial
description: Configurando a loja online inicial
ms.assetid: 86d98936-8f20-4395-be5f-37800162aa89
keywords:
- Lojas online do Windows Media Player, configurando lojas online iniciais
- lojas online, configurando lojas online iniciais
- Digite 1 lojas online, configurando lojas online iniciais
- tipo 2 lojas online, configurando lojas online iniciais
- Lojas online do Windows Media Player, primeira loja online exibida
- lojas online, primeira loja online exibida
- Digite 1 lojas online, primeira loja online exibida
- Digite 2 lojas online, primeira loja online exibida
- primeira loja online exibida
- Configurando lojas online iniciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fff7dc9b2df43f4b18c257b9b9c36998cbc1334
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822856"
---
# <a name="setting-the-initial-online-store"></a><span data-ttu-id="49a71-113">Configurando a loja online inicial</span><span class="sxs-lookup"><span data-stu-id="49a71-113">Setting the Initial Online Store</span></span>

<span data-ttu-id="49a71-114">Para obter detalhes sobre como redistribuir o software do Windows Media Player com seu aplicativo, consulte [redistribuindo o software do Windows Media Player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="49a71-114">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="49a71-115">Quando um usuário instala o Windows Media Player pela primeira vez, o aplicativo de instalação define o repositório online ativo inicial como um padrão escolhido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="49a71-115">When a user first installs Windows Media Player, the setup application sets the initial active online store to a default chosen by Microsoft.</span></span> <span data-ttu-id="49a71-116">Os OEMs (fabricantes de equipamentos originais) do computador pessoal podem optar por alterar essa configuração.</span><span class="sxs-lookup"><span data-stu-id="49a71-116">Personal computer original equipment manufacturers (OEMs) can choose to change this setting.</span></span>

<span data-ttu-id="49a71-117">Para especificar e configurar a primeira loja online que o usuário vê quando instala o Windows Media Player, você deve:</span><span class="sxs-lookup"><span data-stu-id="49a71-117">To specify and configure the first online store that the user sees when he or she installs Windows Media Player, you must:</span></span>

-   <span data-ttu-id="49a71-118">Crie um documento do serviceInfo que você instale no disco rígido do usuário.</span><span class="sxs-lookup"><span data-stu-id="49a71-118">Create a ServiceInfo document that you install on the user's hard disk.</span></span> <span data-ttu-id="49a71-119">Este documento contém as informações sobre como configurar o repositório online ativo inicial.</span><span class="sxs-lookup"><span data-stu-id="49a71-119">This document contains the information about how to configure the initial active online store.</span></span>
-   <span data-ttu-id="49a71-120">Acrescente um conjunto de parâmetros de linha de comando ao executar o aplicativo de instalação.</span><span class="sxs-lookup"><span data-stu-id="49a71-120">Append a set of command-line parameters when running the setup application.</span></span>

<span data-ttu-id="49a71-121">Há três cenários para instalar o Windows Media Player e configurar o repositório online inicial.</span><span class="sxs-lookup"><span data-stu-id="49a71-121">There are three scenarios for installing Windows Media Player and setting the initial online store.</span></span> <span data-ttu-id="49a71-122">As seções a seguir fornecem mais detalhes sobre cada cenário:</span><span class="sxs-lookup"><span data-stu-id="49a71-122">The following sections provide more details about each scenario:</span></span>

-   [<span data-ttu-id="49a71-123">Instalando enquanto estiver offline</span><span class="sxs-lookup"><span data-stu-id="49a71-123">Installing While Offline</span></span>](installing-while-offline.md)
-   [<span data-ttu-id="49a71-124">Instalando de um CD enquanto estiver online</span><span class="sxs-lookup"><span data-stu-id="49a71-124">Installing from a CD While Online</span></span>](installing-from-a-cd-while-online.md)
-   [<span data-ttu-id="49a71-125">Instalando a partir da Web enquanto estiver online</span><span class="sxs-lookup"><span data-stu-id="49a71-125">Installing from the Web While Online</span></span>](installing-from-the-web-while-online.md)

## <a name="related-topics"></a><span data-ttu-id="49a71-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49a71-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49a71-127">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="49a71-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="49a71-128">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="49a71-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="49a71-129">**Parâmetros de linha de comando de instalação para lojas online**</span><span class="sxs-lookup"><span data-stu-id="49a71-129">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




