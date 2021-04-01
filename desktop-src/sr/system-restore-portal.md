---
title: Restauração do Sistema
description: Define pontos de restauração do sistema e monitora as principais alterações do sistema de um programa para permitir a reversão do sistema para um estado anterior. Grave código de recuperação automática ou script WMI para restaurar o estado do sistema para um ponto de restauração registrado.
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- Restauração do Sistema
- Restauração do sistema, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084690"
---
# <a name="system-restore"></a><span data-ttu-id="24f15-106">Restauração do Sistema</span><span class="sxs-lookup"><span data-stu-id="24f15-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="24f15-107">Finalidade</span><span class="sxs-lookup"><span data-stu-id="24f15-107">Purpose</span></span>

<span data-ttu-id="24f15-108">A restauração do sistema monitora e registra automaticamente as principais alterações do sistema no computador de um usuário.</span><span class="sxs-lookup"><span data-stu-id="24f15-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="24f15-109">Ele foi projetado para reduzir os custos de suporte e aumentar a satisfação do cliente, permitindo que um usuário desfaça uma alteração que possa ter causado um problema com o sistema ou reverta para um dia em que o sistema estava sendo executado de forma ideal.</span><span class="sxs-lookup"><span data-stu-id="24f15-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="24f15-110">A documentação a seguir destina-se a desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="24f15-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="24f15-111">Se você for um usuário final procurando informações sobre como usar a restauração do sistema, consulte [o que é a restauração do sistema?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="24f15-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="24f15-112">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="24f15-112">Developer audience</span></span>

<span data-ttu-id="24f15-113">A API de restauração do sistema foi projetada para uso por programadores C/C++.</span><span class="sxs-lookup"><span data-stu-id="24f15-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="24f15-114">Uma familiaridade com o Instrumentação de Gerenciamento do Windows (WMI) é necessária para usar a interface de script.</span><span class="sxs-lookup"><span data-stu-id="24f15-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="24f15-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="24f15-115">Run-time requirements</span></span>

<span data-ttu-id="24f15-116">A API de restauração do sistema tem suporte em sistemas operacionais cliente que começam com o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="24f15-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="24f15-117">Para obter informações sobre quais sistemas operacionais são necessários para usar um elemento de API específico, consulte a seção requisitos de sua documentação.</span><span class="sxs-lookup"><span data-stu-id="24f15-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24f15-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="24f15-118">In this section</span></span>



| <span data-ttu-id="24f15-119">Tópico</span><span class="sxs-lookup"><span data-stu-id="24f15-119">Topic</span></span>                                                | <span data-ttu-id="24f15-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="24f15-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="24f15-121">Visão geral</span><span class="sxs-lookup"><span data-stu-id="24f15-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="24f15-122">Uma visão geral de como funciona a restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="24f15-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="24f15-123">Referência</span><span class="sxs-lookup"><span data-stu-id="24f15-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="24f15-124">Documentação das funções, estruturas e classes de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="24f15-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="24f15-125">Amostras</span><span class="sxs-lookup"><span data-stu-id="24f15-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="24f15-126">Um programa de exemplo escrito em C.</span><span class="sxs-lookup"><span data-stu-id="24f15-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="24f15-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24f15-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24f15-128">WMI</span><span class="sxs-lookup"><span data-stu-id="24f15-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

