---
title: Propriedade FontName (objeto Commands)
description: Saiba mais sobre a propriedade de objeto FontName Commands. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068252"
---
# <a name="fontname-property-commands-object"></a>Propriedade FontName (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a fonte usada no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Fonte Commands.FontName_ *  \[  =  \]



| Parte   | Descrição                                      |
|--------|--------------------------------------------------|
| *Fonte* | Um valor de cadeia de caracteres correspondente ao nome da fonte. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A **propriedade FontName** define a fonte usada para exibir texto no menu pop-up do caractere. O valor padrão para a configuração de fonte é baseado na configuração de fonte de menu para a configuração **LanguageID** do caractere ou , se isso não estiver definido, a configuração de ID de idioma padrão do usuário.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

 

 




