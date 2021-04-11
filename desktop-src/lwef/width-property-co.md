---
title: Propriedade Width (objeto characters)
description: Propriedade Width
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a37a29bd8f50231bd44b6529a0c1ce13c0256d3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008718"
---
# <a name="width-property-characters-object"></a>Propriedade Width (objeto characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a largura do quadro para o caractere especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_")._ *  \[ =  *Valor* de largura\]



| Parte    | Descrição                                                |
|---------|------------------------------------------------------------|
| *value* | Um inteiro longo que especifica a largura do quadro do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade [**Width**](width-property.md) é sempre expressa em pixels. A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.

 

 




