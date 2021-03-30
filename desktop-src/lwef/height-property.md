---
title: Propriedade Height (objeto characters)
description: Propriedade Height
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e504dcbbfd470c62b4102d86f25a1d2b3c4c25e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644105"
---
# <a name="height-property-characters-object"></a>Propriedade Height (objeto characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a altura do quadro do caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agente ***. Caracteres ("**_characterid_*_")._ *  \[ =  *Valor* da altura\]



| Parte    | Descrição                                                 |
|---------|-------------------------------------------------------------|
| *value* | Um inteiro longo que especifica a altura do quadro do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **Height** é sempre expressa em pixels, em relação às coordenadas da tela (superior esquerda). A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com formato irregular, a altura do caractere é baseada nas dimensões externas do quadro de animação retangular usado quando o caractere foi compilado com o editor de caracteres do Microsoft Agent.

 

 




