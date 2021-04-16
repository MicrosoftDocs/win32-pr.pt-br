---
description: Se não for possível localizar os avaliadores de consistência internos necessários entre as ações personalizadas de ICE existentes listadas na referência de ICE, você precisará preparar seu próprio ICE para validar seu pacote.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Criando uma ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768479"
---
# <a name="building-an-ice"></a><span data-ttu-id="3016a-103">Criando uma ICE</span><span class="sxs-lookup"><span data-stu-id="3016a-103">Building An ICE</span></span>

<span data-ttu-id="3016a-104">Se não for possível localizar os [avaliadores de consistência internos](internal-consistency-evaluators-ices.md) necessários entre as ações personalizadas de Ice existentes listadas na [referência de Ice](ice-reference.md), você precisará preparar seu próprio Ice para validar seu pacote.</span><span class="sxs-lookup"><span data-stu-id="3016a-104">If you are unable to find the [Internal Consistency Evaluators](internal-consistency-evaluators-ices.md) you need among the existing ICE custom actions listed in the [ICE Reference](ice-reference.md), you will need to prepare your own ICE to validate your package.</span></span>

<span data-ttu-id="3016a-105">Ao criar ações personalizadas do ICE, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3016a-105">When authoring ICE custom actions you should do the following:</span></span>

-   <span data-ttu-id="3016a-106">Baseie o ICEs somente em ações personalizadas de tipos listados na tabela mostrada.</span><span class="sxs-lookup"><span data-stu-id="3016a-106">Base the ICEs only on custom actions of types listed in the table shown.</span></span>
-   <span data-ttu-id="3016a-107">Chame [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e poste um \_ tipo de mensagem de usuário do INSTALLMESSAGE.</span><span class="sxs-lookup"><span data-stu-id="3016a-107">Call [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) and post an INSTALLMESSAGE\_USER type of message.</span></span> <span data-ttu-id="3016a-108">Ao criar suas mensagens de ICE, siga o formato da mensagem nas [diretrizes de mensagem do Ice](ice-message-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="3016a-108">When authoring your ICE messages follow the message format in the [ICE Message Guidelines](ice-message-guidelines.md).</span></span>
-   <span data-ttu-id="3016a-109">Escreva seu ICE de modo que ele Capture quaisquer erros de API e sempre retorne o êxito do erro \_ .</span><span class="sxs-lookup"><span data-stu-id="3016a-109">Write your ICE such that it captures any API errors and always returns ERROR\_SUCCESS.</span></span> <span data-ttu-id="3016a-110">Isso é necessário para permitir que ações personalizadas subsequentes sejam executadas após a falha de um ICE.</span><span class="sxs-lookup"><span data-stu-id="3016a-110">This is necessary to allow subsequent custom actions to run following the failure of an ICE.</span></span>

<span data-ttu-id="3016a-111">As ações personalizadas do ICE são limitadas aos seguintes tipos de ação personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3016a-111">ICE custom actions are limited to the following custom action types.</span></span>



| <span data-ttu-id="3016a-112">Tipo de ação personalizada</span><span class="sxs-lookup"><span data-stu-id="3016a-112">Custom action type</span></span>                                 | <span data-ttu-id="3016a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3016a-113">Description</span></span>               |
|----------------------------------------------------|---------------------------|
| [<span data-ttu-id="3016a-114">Tipo de ação personalizada 1</span><span class="sxs-lookup"><span data-stu-id="3016a-114">Custom Action Type 1</span></span>](custom-action-type-1.md)   | <span data-ttu-id="3016a-115">DLL no fluxo binário</span><span class="sxs-lookup"><span data-stu-id="3016a-115">DLL in binary stream</span></span>      |
| [<span data-ttu-id="3016a-116">Tipo de ação personalizada 2</span><span class="sxs-lookup"><span data-stu-id="3016a-116">Custom Action Type 2</span></span>](custom-action-type-2.md)   | <span data-ttu-id="3016a-117">EXE no fluxo binário</span><span class="sxs-lookup"><span data-stu-id="3016a-117">EXE in binary stream</span></span>      |
| [<span data-ttu-id="3016a-118">Tipo de ação personalizada 5</span><span class="sxs-lookup"><span data-stu-id="3016a-118">Custom Action Type 5</span></span>](custom-action-type-5.md)   | <span data-ttu-id="3016a-119">JScript em fluxo binário</span><span class="sxs-lookup"><span data-stu-id="3016a-119">JScript in binary stream</span></span>  |
| [<span data-ttu-id="3016a-120">Tipo de ação personalizada 6</span><span class="sxs-lookup"><span data-stu-id="3016a-120">Custom Action Type 6</span></span>](custom-action-type-6.md)   | <span data-ttu-id="3016a-121">VBScript em fluxo binário</span><span class="sxs-lookup"><span data-stu-id="3016a-121">VBScript in binary stream</span></span> |
| [<span data-ttu-id="3016a-122">Tipo de ação personalizada 37</span><span class="sxs-lookup"><span data-stu-id="3016a-122">Custom Action Type 37</span></span>](custom-action-type-37.md) | <span data-ttu-id="3016a-123">Código JScript como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="3016a-123">JScript code as string</span></span>    |
| [<span data-ttu-id="3016a-124">Tipo de ação personalizada 38</span><span class="sxs-lookup"><span data-stu-id="3016a-124">Custom Action Type 38</span></span>](custom-action-type-38.md) | <span data-ttu-id="3016a-125">Código VBScript como cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="3016a-125">VBScript code as string</span></span>   |



 

<span data-ttu-id="3016a-126">Ao criar uma ação personalizada de ICE, não faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3016a-126">When authoring an ICE custom action, do not do the following:</span></span>

-   <span data-ttu-id="3016a-127">Não assuma que o identificador para o mecanismo que o ICE recebe é uma instância de instalação do banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="3016a-127">Do not assume that the handle to the engine that the ICE receives is an installation instance of the installer database.</span></span> <span data-ttu-id="3016a-128">Se não for uma instância de instalação, determinadas propriedades não serão definidas, os diretórios de origem e de destino não serão resolvidos, e os Estados de recursos atuais não serão definidos.</span><span class="sxs-lookup"><span data-stu-id="3016a-128">If it is not a installation instance, certain properties are not defined, the source and target directories are not resolved, and current feature states are not defined.</span></span>
-   <span data-ttu-id="3016a-129">Não confie na execução anterior, ou não na execução, de qualquer ação do instalador, ação personalizada ou outra ICE.</span><span class="sxs-lookup"><span data-stu-id="3016a-129">Do not rely on the prior execution, or non-execution, of any installer action, custom action, or another ICE.</span></span> <span data-ttu-id="3016a-130">Como uma ICE anterior pode ter criado colunas temporárias em qualquer tabela, os autores devem referenciar colunas por nome sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="3016a-130">Because a prior ICE may have created temporary columns in any table, authors should reference columns by name whenever possible.</span></span> <span data-ttu-id="3016a-131">ICEs deve limpar todas as colunas ou tabelas temporárias antes de sair.</span><span class="sxs-lookup"><span data-stu-id="3016a-131">ICEs should cleanup any temporary columns or tables before they exit.</span></span>
-   <span data-ttu-id="3016a-132">Não presuma que os autores tenham acesso a uma imagem do diretório de origem do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3016a-132">Do not assume that authors have access to an image of the source directory of the database.</span></span>
-   <span data-ttu-id="3016a-133">Não assuma que as alterações feitas no banco de dados não persistam.</span><span class="sxs-lookup"><span data-stu-id="3016a-133">Do not assume that changes made to the database do not persist.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3016a-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3016a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3016a-135">ICE de exemplo em C++</span><span class="sxs-lookup"><span data-stu-id="3016a-135">Sample ICE in C++</span></span>](sample-ice-in-c-.md)
</dt> <dt>

[<span data-ttu-id="3016a-136">ICE de exemplo em VBScript</span><span class="sxs-lookup"><span data-stu-id="3016a-136">Sample ICE in VBScript</span></span>](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



