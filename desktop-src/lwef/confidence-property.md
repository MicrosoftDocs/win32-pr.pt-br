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
# <a name="confidence-property"></a>Propriedade de confiança

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define se a **confiança** do cliente aparece na dica de escuta.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid ***"). Comandos ("*** nome ***")**. * ** *  \[  =  *número* de confiança\]



| Parte     | Descrição                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Número* | Uma expressão numérica que é avaliada como um inteiro longo que identifica o valor de confiança para o [**comando**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o valor de confiança retornado da melhor correspondência (userinput. confiante) não exceder o valor definido para a propriedade **int** , o texto fornecido em [**ConfidenceText**](confidencetext-property.md) será exibido na dica de escuta.

 

 