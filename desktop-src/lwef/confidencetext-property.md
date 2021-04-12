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
# <a name="confidencetext-property"></a>Propriedade ConfidenceText

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o **ConfidenceText** do cliente que aparece na dica de escuta.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

* Agente ***. Caracteres ("*** characterid ***"). Comandos ("*** name ***")**.  \[ ConfidenceText  =  *cadeia de caracteres*\]



| Parte     | Descrição                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *cadeia de caracteres* | Uma expressão de cadeia de caracteres que é avaliada como o texto do **ConfidenceText** para o [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando o valor de confiança retornado da melhor correspondência (userinput. int) não excede a configuração de [**confiança**](confidence-property.md) , o servidor exibe o texto fornecido em **ConfidenceText** na dica de escuta.

 

 