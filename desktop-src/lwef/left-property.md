---
title: Propriedade Left (objeto characters)
description: Saiba mais sobre a propriedade de objeto caracteres à esquerda. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e2f860e6827a9c96c42014456e43b791ab70ed4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988932"
---
# <a name="left-property-characters-object"></a>Propriedade Left (objeto characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a borda esquerda do quadro do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_")._ *  \[  =  *Valor* esquerdo\]



| Parte    | Descrição                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Um inteiro longo que especifica a borda esquerda do quadro do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **Left** é sempre expressa em pixels, em relação à origem da tela (superior esquerda). A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.

 

 




