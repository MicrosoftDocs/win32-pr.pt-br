---
title: Propriedade Left (objeto characters)
description: Propriedade Left
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105756790"
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

 

 




