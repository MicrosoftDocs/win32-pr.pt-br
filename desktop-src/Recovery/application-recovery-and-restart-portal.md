---
title: Reinicialização e recuperação de aplicativos
description: Escreva instaladores personalizados para reiniciar automaticamente um aplicativo que foi desligado para concluir uma atualização. Salve os dados e configure a recuperação do aplicativo antes de sair dos programas.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recuperação
- confiabilidade
- confiabilidade do software
- recuperação de aplicativo
- reinicialização do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822961"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="11fbb-111">Reinicialização e recuperação de aplicativos</span><span class="sxs-lookup"><span data-stu-id="11fbb-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="11fbb-112">Finalidade</span><span class="sxs-lookup"><span data-stu-id="11fbb-112">Purpose</span></span>

<span data-ttu-id="11fbb-113">Um aplicativo pode usar a recuperação e reinicialização do aplicativo (ARR) para salvar dados e informações de estado antes que o aplicativo seja encerrado devido a uma exceção sem tratamento ou quando o aplicativo para de responder.</span><span class="sxs-lookup"><span data-stu-id="11fbb-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="11fbb-114">O aplicativo também será reiniciado, se solicitado.</span><span class="sxs-lookup"><span data-stu-id="11fbb-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="11fbb-115">Um aplicativo também pode ser reiniciado se um instalador atualizar um componente do aplicativo ou se o computador precisar ser reiniciado como resultado de uma atualização.</span><span class="sxs-lookup"><span data-stu-id="11fbb-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="11fbb-116">Observe que para dar suporte à reinicialização automática do aplicativo depois que um instalador atualiza um aplicativo, o aplicativo e o instalador precisam ser criados adequadamente.</span><span class="sxs-lookup"><span data-stu-id="11fbb-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="11fbb-117">Para obter detalhes, consulte [registrando para reinicialização do aplicativo](registering-for-application-restart.md).</span><span class="sxs-lookup"><span data-stu-id="11fbb-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="11fbb-118">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="11fbb-118">Developer audience</span></span>

<span data-ttu-id="11fbb-119">O ARR foi projetado para desenvolvedores de C e C++.</span><span class="sxs-lookup"><span data-stu-id="11fbb-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="11fbb-120">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="11fbb-120">Run-time requirements</span></span>

<span data-ttu-id="11fbb-121">O ARR está disponível a partir do sistema operacional Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="11fbb-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="11fbb-122">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="11fbb-122">In this section</span></span>



| <span data-ttu-id="11fbb-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="11fbb-123">Topic</span></span>                                                                                                   | <span data-ttu-id="11fbb-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="11fbb-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="11fbb-125">Usando a recuperação e reinicialização do aplicativo</span><span class="sxs-lookup"><span data-stu-id="11fbb-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="11fbb-126">Guia de procedimentos para o registro para recuperação e reinicialização.</span><span class="sxs-lookup"><span data-stu-id="11fbb-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="11fbb-127">Recuperação de aplicativo e referência de reinicialização</span><span class="sxs-lookup"><span data-stu-id="11fbb-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="11fbb-128">Informações de referência para a API ARR.</span><span class="sxs-lookup"><span data-stu-id="11fbb-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





