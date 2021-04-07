---
description: ICE90 posta um aviso se descobrir que o diretório de um atalho foi especificado como uma propriedade pública.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827942"
---
# <a name="ice90"></a><span data-ttu-id="77002-103">ICE90</span><span class="sxs-lookup"><span data-stu-id="77002-103">ICE90</span></span>

<span data-ttu-id="77002-104">ICE90 posta um aviso se descobrir que o diretório de um atalho foi especificado como uma propriedade pública.</span><span class="sxs-lookup"><span data-stu-id="77002-104">ICE90 posts a warning if it finds that a shortcut's directory has been specified as a public property.</span></span> <span data-ttu-id="77002-105">Os nomes das [Propriedades públicas](public-properties.md) são gravados em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="77002-105">The names of [Public Properties](public-properties.md) are written in uppercase letters.</span></span> <span data-ttu-id="77002-106">Um atalho especificado por uma propriedade pública pode não funcionar se o valor da propriedade [**AllUsers**](allusers.md) for alterado.</span><span class="sxs-lookup"><span data-stu-id="77002-106">A shortcut specified by a public property may not work if the value of the [**ALLUSERS**](allusers.md) property changes.</span></span>

<span data-ttu-id="77002-107">Essa ação personalizada de ICE valida a tabela de atalho e usa a tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="77002-107">This ICE custom action validates the Shortcut table and uses the Directory table.</span></span> <span data-ttu-id="77002-108">Se a tabela de diretório não estiver presente, ela será retornada sem validar a tabela de atalho e não lançará nenhum erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="77002-108">If the Directory table is not present, it returns without validating the Shortcut table and posts no errors or warnings.</span></span>

## <a name="result"></a><span data-ttu-id="77002-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="77002-109">Result</span></span>

<span data-ttu-id="77002-110">ICE90 posta o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="77002-110">ICE90 posts the following warning.</span></span>



| <span data-ttu-id="77002-111">Erro de ICE90</span><span class="sxs-lookup"><span data-stu-id="77002-111">ICE90 error</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="77002-112">Description</span><span class="sxs-lookup"><span data-stu-id="77002-112">Description</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="77002-113">O atalho ' \[ 1 \] ' tem um diretório que é uma propriedade pública (All Caps) e está no diretório de perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="77002-113">The shortcut '\[1\]' has a directory that is a public property (ALL CAPS) and is under user profile directory.</span></span> <span data-ttu-id="77002-114">Isso resultará em um problema se o valor da propriedade [**AllUsers**](allusers.md) for alterado na sequência da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="77002-114">This results in a problem if the value of the [**ALLUSERS**](allusers.md) property changes in the UI sequence.</span></span> | <span data-ttu-id="77002-115">O diretório de um atalho foi especificado como uma propriedade pública.</span><span class="sxs-lookup"><span data-stu-id="77002-115">A shortcut's directory has been specified as a public property.</span></span> |



 

## <a name="example"></a><span data-ttu-id="77002-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="77002-116">Example</span></span>

<span data-ttu-id="77002-117">ICE90 relata o seguinte aviso para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="77002-117">ICE90 reports the following warning for the example:</span></span>

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

<span data-ttu-id="77002-118">Neste exemplo, MYDIR está em um perfil de usuários.</span><span class="sxs-lookup"><span data-stu-id="77002-118">In this example, MYDIR is under a users profile.</span></span> <span data-ttu-id="77002-119">ICE90 posta um aviso porque o local do diretório de destino é especificado por uma propriedade pública, MYDIR.</span><span class="sxs-lookup"><span data-stu-id="77002-119">ICE90 posts a warning because the location of the target directory is specified by a public property, MYDIR.</span></span> <span data-ttu-id="77002-120">Um usuário pode alterar A propriedade MYDIR ou [**AllUsers**](allusers.md) .</span><span class="sxs-lookup"><span data-stu-id="77002-120">A user may change MYDIR or [**ALLUSERS**](allusers.md) property.</span></span> <span data-ttu-id="77002-121">Se **AllUsers** estiver definido para o [contexto de instalação](installation-context.md)por máquina e MYDIR estiver em um perfil de usuários, o arquivo de atalho em MYDIR será copiado no perfil "todos os usuários" e não em um perfil de usuário específico.</span><span class="sxs-lookup"><span data-stu-id="77002-121">If **ALLUSERS** is set for the per-machine [installation context](installation-context.md), and MYDIR is under a users profile, the shortcut file in MYDIR are copied under the "All Users" profile and not a particular user's profile.</span></span> <span data-ttu-id="77002-122">Se **AllUsers** estiver definido para o contexto de instalação por usuário, o arquivo de atalho em MYDIR será copiado para um perfil de usuário específico e não estará disponível para outros usuários.</span><span class="sxs-lookup"><span data-stu-id="77002-122">If **ALLUSERS** is set for the per-user installation context, the shortcut file in MYDIR is copied into a particular user's profile and is not available to other users.</span></span>

<span data-ttu-id="77002-123">[Tabela de atalho](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="77002-123">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="77002-124">Atalho</span><span class="sxs-lookup"><span data-stu-id="77002-124">Shortcut</span></span>  | <span data-ttu-id="77002-125">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="77002-125">Directory\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="77002-126">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="77002-126">Shortcut1</span></span> | <span data-ttu-id="77002-127">MYDIR</span><span class="sxs-lookup"><span data-stu-id="77002-127">MYDIR</span></span>       |



 

<span data-ttu-id="77002-128">[Tabela de diretórios](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="77002-128">[Directory Table](directory-table.md) (partial)</span></span>



| <span data-ttu-id="77002-129">Diretório</span><span class="sxs-lookup"><span data-stu-id="77002-129">Directory</span></span> | <span data-ttu-id="77002-130">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="77002-130">Directory\_Parent</span></span> |
|-----------|-------------------|
| <span data-ttu-id="77002-131">MYDIR</span><span class="sxs-lookup"><span data-stu-id="77002-131">MYDIR</span></span>     | <span data-ttu-id="77002-132">ProgramMenuFolder</span><span class="sxs-lookup"><span data-stu-id="77002-132">ProgramMenuFolder</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="77002-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77002-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77002-134">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="77002-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



