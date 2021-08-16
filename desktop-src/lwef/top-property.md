---
title: Propriedade Top (objeto characters)
description: Saiba mais sobre a propriedade Top (objeto characters). o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bdc753bc287e1289b2a75633081c7b325d698a7fbe92ba495cc93662485d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474474"
---
# <a name="top-property-characters-object"></a>Propriedade Top (objeto characters)

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a borda superior do quadro do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_")._ *  \[  =  *Valor* superior\]



| Parte    | Descrição                                             |
|---------|---------------------------------------------------------|
| *value* | Um inteiro longo que especifica a borda superior do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **Top** é sempre expressa em pixels, em relação à origem da tela (superior esquerda). A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.

Use o método [**MoveTo**](moveto-method.md) para alterar o local do caractere.

## <a name="see-also"></a>Consulte Também

[**Propriedade Left**](left-property.md), [ **método MoveTo**](moveto-method.md)


 

 




