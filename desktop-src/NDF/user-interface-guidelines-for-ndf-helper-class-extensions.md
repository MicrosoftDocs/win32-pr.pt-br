---
title: Diretrizes da interface do usuário para extensões de classe auxiliar NDF
description: Ao criar sua classe auxiliar, você precisará criar um texto para ajudar o usuário a entender a causa de um incidente e as possíveis etapas de reparo que podem ser tomadas.
ms.assetid: f13f3621-ab82-4e22-9442-0a4d57c368fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e48357ba6561ab135e2c341409c22d1edf3fb7d
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104293541"
---
# <a name="ui-guidelines-for-ndf-helper-class-extensions"></a><span data-ttu-id="d7af4-103">Diretrizes da interface do usuário para extensões de classe auxiliar NDF</span><span class="sxs-lookup"><span data-stu-id="d7af4-103">UI guidelines for NDF helper class extensions</span></span>

<span data-ttu-id="d7af4-104">Ao criar sua classe auxiliar, você precisará criar um texto para ajudar o usuário a entender a causa de um incidente e as possíveis etapas de reparo que podem ser tomadas.</span><span class="sxs-lookup"><span data-stu-id="d7af4-104">When building your helper class, you will need to create text to help the user understand the cause of an incident and the possible repair steps which can be taken.</span></span>

## <a name="root-cause-and-repair"></a><span data-ttu-id="d7af4-105">Causa e reparo raiz</span><span class="sxs-lookup"><span data-stu-id="d7af4-105">Root Cause and Repair</span></span>

<span data-ttu-id="d7af4-106">Quando ocorrer um incidente, uma caixa de diálogo será exibida para informar o usuário sobre o que aconteceu.</span><span class="sxs-lookup"><span data-stu-id="d7af4-106">When an incident occurs, a dialog box will appear to inform the user about what has happened.</span></span> <span data-ttu-id="d7af4-107">O texto que você cria aparecerá em duas áreas separadas.</span><span class="sxs-lookup"><span data-stu-id="d7af4-107">The text that you create will appear in two separate areas.</span></span>

-   <span data-ttu-id="d7af4-108">**Causa raiz**: uma breve descrição da causa do problema.</span><span class="sxs-lookup"><span data-stu-id="d7af4-108">**Root Cause**: A brief description of the cause of the issue.</span></span> <span data-ttu-id="d7af4-109">Contém informações para ajudar um administrador ou usuário avançado a solucionar o problema.</span><span class="sxs-lookup"><span data-stu-id="d7af4-109">Contains information to help an administrator or advanced user troubleshoot the problem.</span></span>
-   <span data-ttu-id="d7af4-110">**Reparo**: expande a causa raiz para fornecer mais detalhes sobre as etapas que um usuário pode executar, sem ficar muito demorado.</span><span class="sxs-lookup"><span data-stu-id="d7af4-110">**Repair**: Expands on the root cause to provide more details about the steps that a user can take, without getting too lengthy.</span></span>

<span data-ttu-id="d7af4-111">Cada causa ou reparo raiz deve ter um título e uma descrição.</span><span class="sxs-lookup"><span data-stu-id="d7af4-111">Each root cause or repair should have a title and a description.</span></span> <span data-ttu-id="d7af4-112">Todo o texto antes do primeiro \\ caractere "n" será usado para o título.</span><span class="sxs-lookup"><span data-stu-id="d7af4-112">All text before the first "\\n" character will be used for the title.</span></span> <span data-ttu-id="d7af4-113">Todo o texto após o primeiro \\ caractere "n" (incluindo todas as quebras de linha subsequentes) será usado para a descrição.</span><span class="sxs-lookup"><span data-stu-id="d7af4-113">All text following the first "\\n" character (including any subsequent line breaks) will be used for the description.</span></span>

## <a name="title-guidelines"></a><span data-ttu-id="d7af4-114">Diretrizes de título</span><span class="sxs-lookup"><span data-stu-id="d7af4-114">Title Guidelines</span></span>

<span data-ttu-id="d7af4-115">O título de uma causa raiz ou reparo deve seguir estas diretrizes:</span><span class="sxs-lookup"><span data-stu-id="d7af4-115">The title of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="d7af4-116">Deve ter de 128 caracteres ou menos.</span><span class="sxs-lookup"><span data-stu-id="d7af4-116">Must be 128 characters or fewer.</span></span> <span data-ttu-id="d7af4-117">(recomenda-se 40 caracteres ou menos).</span><span class="sxs-lookup"><span data-stu-id="d7af4-117">(40 characters or less is recommended.)</span></span>
-   <span data-ttu-id="d7af4-118">Não deve terminar com um ponto.</span><span class="sxs-lookup"><span data-stu-id="d7af4-118">Should not end with a period.</span></span>

## <a name="description-guidelines"></a><span data-ttu-id="d7af4-119">Diretrizes de descrição</span><span class="sxs-lookup"><span data-stu-id="d7af4-119">Description Guidelines</span></span>

<span data-ttu-id="d7af4-120">A descrição de uma causa raiz ou reparo deve seguir estas diretrizes:</span><span class="sxs-lookup"><span data-stu-id="d7af4-120">The description of a root cause or repair should follow these guidelines:</span></span>

-   <span data-ttu-id="d7af4-121">Deve ter de 512 caracteres ou menos.</span><span class="sxs-lookup"><span data-stu-id="d7af4-121">Must be 512 characters or fewer.</span></span>
-   <span data-ttu-id="d7af4-122">Cada frase deve terminar com um ponto.</span><span class="sxs-lookup"><span data-stu-id="d7af4-122">Each sentence should end with a period.</span></span>
-   <span data-ttu-id="d7af4-123">O \\ caractere "n" pode ser usado para criar uma quebra de linha na descrição.</span><span class="sxs-lookup"><span data-stu-id="d7af4-123">The "\\n" character may be used to create a line break in the description.</span></span>

 

 




