---
title: Parâmetros de linha de comando de instalação para lojas online
description: Parâmetros de linha de comando de instalação para lojas online
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Armazenamentos online do Windows Media Player, parâmetros de linha de comando de instalação
- lojas online, parâmetros de linha de comando de instalação
- Digite 1 lojas online, parâmetros de linha de comando de instalação
- Digite 2 lojas online, parâmetros de linha de comando de instalação
- parâmetros de linha de comando da instalação
- Lojas online do Windows Media Player, parâmetros de linha de comando
- lojas online, parâmetros de linha de comando
- tipo 1 lojas online, parâmetros de linha de comando
- tipo 2 lojas online, parâmetros de linha de comando
- parâmetros de linha de comando
- Armazenamentos online do Windows Media Player, parâmetros
- lojas online, parâmetros
- tipo 1 lojas online, parâmetros
- tipo 2 lojas online, parâmetros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005451"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="6a3d7-117">Parâmetros de linha de comando de instalação para lojas online</span><span class="sxs-lookup"><span data-stu-id="6a3d7-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="6a3d7-118">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6a3d7-119">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6a3d7-120">Ao instalar o Windows Media Player 10 ou o Windows Media Player 11 no Windows XP, você pode acrescentar parâmetros de linha de comando para especificar a primeira loja online que o usuário vê.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="6a3d7-121">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a3d7-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="6a3d7-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a3d7-122">Parameters</span></span>

<span data-ttu-id="6a3d7-123">Defaultservice (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="6a3d7-123">DefaultService (required)</span></span>

<span data-ttu-id="6a3d7-124">O nome da chave para a loja online.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-124">The key name for the online store.</span></span> <span data-ttu-id="6a3d7-125">Esse valor deve corresponder ao nome da chave no atributo de **chave** do elemento **serviceInfo** do documento serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="6a3d7-126">ServiceInfo (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="6a3d7-126">ServiceInfo (required)</span></span>

<span data-ttu-id="6a3d7-127">O caminho totalmente qualificado para um documento do serviceInfo instalado no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="6a3d7-128">Userextra (opcional)</span><span class="sxs-lookup"><span data-stu-id="6a3d7-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="6a3d7-129">Uma cadeia de caracteres de consulta que o Windows Media Player 10 acrescentará à URL do documento do serviceInfo quando recuperar o documento online.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a3d7-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a3d7-130">Remarks</span></span>

<span data-ttu-id="6a3d7-131">Para obter detalhes sobre como redistribuir o software do Windows Media Player com seu aplicativo, consulte [redistribuindo o software do Windows Media Player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="6a3d7-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="6a3d7-132">Quando o computador do usuário não está conectado à Internet, as informações contidas no documento local de informações são usadas para configurar o Windows Media Player para o serviço ativo inicial.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="6a3d7-133">Os parâmetros de linha de comando diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6a3d7-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a3d7-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a3d7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a3d7-135">**Lojas online de co-identidade visual**</span><span class="sxs-lookup"><span data-stu-id="6a3d7-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6a3d7-136">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6a3d7-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6a3d7-137">**Elemento de instalação**</span><span class="sxs-lookup"><span data-stu-id="6a3d7-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="6a3d7-138">**Configurando a loja online inicial**</span><span class="sxs-lookup"><span data-stu-id="6a3d7-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




