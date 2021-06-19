---
title: Propriedade Width (objeto Characters)
description: Saiba mais sobre a Propriedade width do objeto Characters, que retorna ou define a largura do quadro para o caractere especificado.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395122"
---
# <a name="width-property-characters-object"></a>Propriedade Width (objeto Characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a largura do quadro para o caractere especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Valor_ *  \[ =  *de largura*\]



| Parte    | Descrição                                                |
|---------|------------------------------------------------------------|
| *value* | Um inteiro Longo que especifica a largura do quadro do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A [**propriedade Width**](width-property.md) é sempre expressa em pixels. A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com forma irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o Editor de Caracteres do Microsoft Agent.

 

 




