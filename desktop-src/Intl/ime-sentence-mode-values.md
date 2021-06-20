---
description: Examine a lista de valores do modo de sentença do IME (editor de método de entrada). Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores do modo de frase do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 285636ab097bd536e5bd0e4e1869f12c648c3cbb
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406759"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="e5f61-104">Valores do modo de frase do IME</span><span class="sxs-lookup"><span data-stu-id="e5f61-104">IME Sentence Mode Values</span></span>

<span data-ttu-id="e5f61-105">Esses valores são usados com as funções [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="e5f61-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="e5f61-106">Constante</span><span class="sxs-lookup"><span data-stu-id="e5f61-106">Constant</span></span>                  | <span data-ttu-id="e5f61-107">Definição</span><span class="sxs-lookup"><span data-stu-id="e5f61-107">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e5f61-108">SMODE de IME \_ \_ automático</span><span class="sxs-lookup"><span data-stu-id="e5f61-108">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="e5f61-109">O IME executa o processamento de conversão no modo automático.</span><span class="sxs-lookup"><span data-stu-id="e5f61-109">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="e5f61-110">\_SMODE IME \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="e5f61-110">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="e5f61-111">Nenhuma informação para frase.</span><span class="sxs-lookup"><span data-stu-id="e5f61-111">No information for sentence.</span></span>                                               |
| <span data-ttu-id="e5f61-112">\_SMODE IME \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="e5f61-112">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="e5f61-113">O IME usa informações de frase para prever o próximo caractere.</span><span class="sxs-lookup"><span data-stu-id="e5f61-113">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="e5f61-114">\_SMODE IME \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="e5f61-114">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="e5f61-115">O IME usa as informações de cláusula plural para executar o processamento de conversão.</span><span class="sxs-lookup"><span data-stu-id="e5f61-115">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="e5f61-116">\_SMODE IME \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="e5f61-116">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="e5f61-117">O IME executa o processamento de conversão no modo de caractere único.</span><span class="sxs-lookup"><span data-stu-id="e5f61-117">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="e5f61-118">\_conversa de SMODE do IME \_</span><span class="sxs-lookup"><span data-stu-id="e5f61-118">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="e5f61-119">O IME usa o modo de conversa.</span><span class="sxs-lookup"><span data-stu-id="e5f61-119">The IME uses conversation mode.</span></span> <span data-ttu-id="e5f61-120">Isso é útil para aplicativos de chat.</span><span class="sxs-lookup"><span data-stu-id="e5f61-120">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="e5f61-121">Os bits 16 a 31 são reservados para uso do IME.</span><span class="sxs-lookup"><span data-stu-id="e5f61-121">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



