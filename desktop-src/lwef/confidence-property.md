---
title: Propriedade de confiança
description: Propriedade de confiança
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365875"
---
# <a name="confidence-property"></a><span data-ttu-id="39294-103">Propriedade de confiança</span><span class="sxs-lookup"><span data-stu-id="39294-103">Confidence Property</span></span>

<span data-ttu-id="39294-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39294-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="39294-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="39294-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="39294-106">Retorna ou define se a **confiança** do cliente aparece na dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="39294-106">Returns or sets whether the client's **Confidence** appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="39294-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="39294-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="39294-108">\*agente do ***. Caracteres ("*** characterid ***"). Comandos ("*** nome \***")**. \* \*\* \*  \[  =  *número* de confiança\]</span><span class="sxs-lookup"><span data-stu-id="39294-108">*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.\*\*Confidence*\* \[ = *Number*\]</span></span>



| <span data-ttu-id="39294-109">Parte</span><span class="sxs-lookup"><span data-stu-id="39294-109">Part</span></span>     | <span data-ttu-id="39294-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="39294-110">Description</span></span>                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39294-111">*Número*</span><span class="sxs-lookup"><span data-stu-id="39294-111">*Number*</span></span> | <span data-ttu-id="39294-112">Uma expressão numérica que é avaliada como um inteiro longo que identifica o valor de confiança para o [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="39294-112">A numeric expression that evaluates to a Long integer that identifies confidence value for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39294-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="39294-113">Remarks</span></span>

<span data-ttu-id="39294-114">Se o valor de confiança retornado da melhor correspondência (userinput. confiante) não exceder o valor definido para a propriedade **int** , o texto fornecido em [**ConfidenceText**](confidencetext-property.md) será exibido na dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="39294-114">If the returned confidence value of the best match (UserInput.Confidence) does not exceed value you set for the **Confidence** property, the text supplied in [**ConfidenceText**](confidencetext-property.md) is displayed in the Listening Tip.</span></span>

 

 