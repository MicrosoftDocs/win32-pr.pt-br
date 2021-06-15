---
title: Propriedade FontSize (objeto Balloon)
description: Saiba mais sobre a propriedade de objeto de balão FontSize. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 36d5526a-1ae9-4ef2-94f6-0ad63ce86882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a2c13708d3066faaf396a3a451c9be01d177
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068213"
---
# <a name="fontsize-property-balloon-object"></a>Propriedade FontSize (objeto Balloon)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define o tamanho da fonte com suporte para o balão de palavras para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*Agent. * * * caracteres* *  **("**_Characterid_*_"). Pontos de balão. FontSize_* \[  =  \]



| Parte     | Descrição                                              |
|----------|----------------------------------------------------------|
| *Faixas* | Um valor inteiro longo que especifica o tamanho da fonte em pontos. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade [**FontSize**](fontsize-property.md) retorna um valor inteiro longo especificando o tamanho da fonte atual em pontos. O valor máximo para **FontSize** é de 2160 pontos.

O valor padrão das configurações de fonte do balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent. Além disso, o usuário pode substituir as configurações de fonte para todos os caracteres na folha de propriedades do Microsoft Agent.

 

 




