---
title: Propriedade Enabled (objeto Balloon)
description: Propriedade Enabled
ms.assetid: 4d73acda-6fcc-4912-a466-570849aeb807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07179390b183e98a5eaccb2dfdb4405525d7d26e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105781163"
---
# <a name="enabled-property-balloon-object"></a>Propriedade Enabled (objeto Balloon)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna se o balão de palavra está habilitado para o caractere especificado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente ***. Caracteres ("**_characterid_*_"). Balão. habilitado_*



| Valor     | Descrição              |
|-----------|--------------------------|
| **Verdadeiro**  | O balão está habilitado.  |
| **Falso** | O balão está desabilitado. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

A propriedade **Enabled** retorna um valor booliano que especifica se o balão está habilitado. O estado padrão do balão de palavras é definido como parte da definição de um caractere quando o caractere é compilado no editor de caracteres do Microsoft Agent. Se um caractere for definido para não oferecer suporte à palavra balão, essa propriedade será sempre **falsa** para o caractere.

 

 




