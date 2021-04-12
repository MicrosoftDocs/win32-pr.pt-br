---
title: Propriedade ConfidenceText
description: Propriedade ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365938"
---
# <a name="confidencetext-property"></a><span data-ttu-id="30f8d-103">Propriedade ConfidenceText</span><span class="sxs-lookup"><span data-stu-id="30f8d-103">ConfidenceText Property</span></span>

<span data-ttu-id="30f8d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30f8d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="30f8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="30f8d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="30f8d-106">Retorna ou define o **ConfidenceText** do cliente que aparece na dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="30f8d-106">Returns or sets the client's **ConfidenceText** that appears in the Listening Tip.</span></span>

</dd> <dt>

<span data-ttu-id="30f8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="30f8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="30f8d-108">\* Agente ***. Caracteres ("*** characterid ***"). Comandos ("*** name \***")**.  \[ ConfidenceText  =  *cadeia de caracteres*\]</span><span class="sxs-lookup"><span data-stu-id="30f8d-108">\*agent ***.Characters ("*** CharacterID ***").Commands("*** name\***")**.**ConfidenceText**\[ = *string*\]</span></span>



| <span data-ttu-id="30f8d-109">Parte</span><span class="sxs-lookup"><span data-stu-id="30f8d-109">Part</span></span>     | <span data-ttu-id="30f8d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="30f8d-110">Description</span></span>                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30f8d-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="30f8d-111">*string*</span></span> | <span data-ttu-id="30f8d-112">Uma expressão de cadeia de caracteres que é avaliada como o texto do **ConfidenceText** para o [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="30f8d-112">A string expression that evaluates to the text for the **ConfidenceText** for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30f8d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="30f8d-113">Remarks</span></span>

<span data-ttu-id="30f8d-114">Quando o valor de confiança retornado da melhor correspondência (userinput. int) não excede a configuração de [**confiança**](confidence-property.md) , o servidor exibe o texto fornecido em **ConfidenceText** na dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="30f8d-114">When the returned confidence value of the best match (UserInput.Confidence) does not exceed the [**Confidence**](confidence-property.md) setting, the server displays the text supplied in **ConfidenceText** in the Listening Tip.</span></span>

 

 