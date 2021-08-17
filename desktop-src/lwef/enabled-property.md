---
title: Propriedade Enabled (objeto Balloon)
description: Saiba mais sobre a propriedade de objeto Balão Habilitado. O Microsoft Agent foi preterido a partir Windows 7.
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d4eaa09e173d847e9dead1bbd559b59e2d12a2d40b5f1d1f989d3cf70263ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751998"
---
# <a name="enabled-property-balloon-object"></a>Propriedade Enabled (objeto Balloon)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna se a palavra balão está habilitada para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Balloon.Enabled_*



| Valor     | Descrição              |
|-----------|--------------------------|
| **Verdadeiro**  | O balão está habilitado.  |
| **Falso** | O balão está desabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A **propriedade Enabled** retorna um valor booliana que especifica se o balão está habilitado. O estado padrão do balão de palavra é definido como parte da definição de um caractere quando o caractere é compilado no Editor de Caracteres do Microsoft Agent. Se um caractere for definido para não dar suporte ao balão de palavra, essa propriedade sempre será **False** para o caractere.

 

 




