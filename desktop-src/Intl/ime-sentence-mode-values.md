---
description: Esses valores são usados com as funções ImmGetConversionStatus e ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valores do modo de frase do IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2fb9d25b2c3b1828e8c36aca554468f6447af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169725"
---
# <a name="ime-sentence-mode-values"></a><span data-ttu-id="3dd9b-103">Valores do modo de frase do IME</span><span class="sxs-lookup"><span data-stu-id="3dd9b-103">IME Sentence Mode Values</span></span>

<span data-ttu-id="3dd9b-104">Esses valores são usados com as funções [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) e [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="3dd9b-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="3dd9b-105">Constante</span><span class="sxs-lookup"><span data-stu-id="3dd9b-105">Constant</span></span>                  | <span data-ttu-id="3dd9b-106">Definição</span><span class="sxs-lookup"><span data-stu-id="3dd9b-106">Definition</span></span>                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="3dd9b-107">SMODE de IME \_ \_ automático</span><span class="sxs-lookup"><span data-stu-id="3dd9b-107">IME\_SMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="3dd9b-108">O IME executa o processamento de conversão no modo automático.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-108">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="3dd9b-109">\_SMODE IME \_ nenhum</span><span class="sxs-lookup"><span data-stu-id="3dd9b-109">IME\_SMODE\_NONE</span></span>          | <span data-ttu-id="3dd9b-110">Nenhuma informação para frase.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-110">No information for sentence.</span></span>                                               |
| <span data-ttu-id="3dd9b-111">\_SMODE IME \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="3dd9b-111">IME\_SMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="3dd9b-112">O IME usa informações de frase para prever o próximo caractere.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-112">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="3dd9b-113">\_SMODE IME \_ PLURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="3dd9b-113">IME\_SMODE\_PLURALCLAUSE</span></span>  | <span data-ttu-id="3dd9b-114">O IME usa as informações de cláusula plural para executar o processamento de conversão.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-114">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="3dd9b-115">\_SMODE IME \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="3dd9b-115">IME\_SMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="3dd9b-116">O IME executa o processamento de conversão no modo de caractere único.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-116">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="3dd9b-117">\_conversa de SMODE do IME \_</span><span class="sxs-lookup"><span data-stu-id="3dd9b-117">IME\_SMODE\_CONVERSATION</span></span>  | <span data-ttu-id="3dd9b-118">O IME usa o modo de conversa.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-118">The IME uses conversation mode.</span></span> <span data-ttu-id="3dd9b-119">Isso é útil para aplicativos de chat.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-119">This is useful for chat applications.</span></span>      |



 

<span data-ttu-id="3dd9b-120">Os bits 16 a 31 são reservados para uso do IME.</span><span class="sxs-lookup"><span data-stu-id="3dd9b-120">Bits 16 through 31 are reserved for IME use.</span></span>

 

 



