---
description: Um IME implementa um recurso chamado &\# 0034; reconversão&\# 0034;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Usando a reconversão com um IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768590"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="b5945-103">Usando a reconversão com um IME</span><span class="sxs-lookup"><span data-stu-id="b5945-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="b5945-104">Um IME implementa um recurso chamado "reconversão".</span><span class="sxs-lookup"><span data-stu-id="b5945-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="b5945-105">Normalmente, o IMM determina as listas de candidatos com base apenas nas entradas digitadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b5945-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="b5945-106">A reconversão permite que o IMM determine um ou mais candidatos com base na frase que a contém (o contexto).</span><span class="sxs-lookup"><span data-stu-id="b5945-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="b5945-107">Os tipos de reconversão definidos são simples, normais e aprimorados.</span><span class="sxs-lookup"><span data-stu-id="b5945-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="b5945-108">A reconversão é útil quando um usuário observa um erro de composição em um documento.</span><span class="sxs-lookup"><span data-stu-id="b5945-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="b5945-109">O usuário pode selecionar o erro e escolher reconversão em um menu.</span><span class="sxs-lookup"><span data-stu-id="b5945-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="b5945-110">O IME usa o contexto para determinar a melhor substituição.</span><span class="sxs-lookup"><span data-stu-id="b5945-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="b5945-111">O aplicativo pode usar [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) para dar suporte à reconversão.</span><span class="sxs-lookup"><span data-stu-id="b5945-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5945-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5945-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5945-113">Usando o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="b5945-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



