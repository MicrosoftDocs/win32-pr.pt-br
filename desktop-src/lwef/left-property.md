---
title: Propriedade Left (objeto Characters)
description: Saiba mais sobre a propriedade de objeto Left Characters. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e546dc662dc535889eb6c3a476a54b839c5d9577a7e2ff525eeadf79f727fbf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105012"
---
# <a name="left-property-characters-object"></a>Propriedade Left (objeto Characters)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a borda esquerda do quadro do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor_ *  \[  =  *esquerdo*\]



| Parte    | Descrição                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Um inteiro Longo que especifica a borda esquerda do quadro do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A **propriedade Left** sempre é expressa em pixels, em relação à origem da tela (superior esquerdo). A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com forma irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o Editor de Caracteres do Microsoft Agent.

 

 




