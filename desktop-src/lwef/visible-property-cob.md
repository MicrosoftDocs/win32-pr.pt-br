---
title: Propriedade Visible (objeto Characters)
description: Saiba mais sobre a Propriedade Visível do objeto Characters, que retorna um booliana que indica se o caractere está visível.
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7358cd87a7fb3232b22cef33cbee5f2609708875
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396301"
---
# <a name="visible-property-characters-object"></a>Propriedade Visible (objeto Characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna um booliana que indica se o caractere está visível.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Visível**



| Valor | Descrição                            |
|-------|----------------------------------------|
| True  | O caractere é exibido.            |
| Falso | O caractere está oculto (não visível). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa propriedade indica se o quadro do caractere está sendo exibido. Isso não significa necessariamente que há uma imagem na tela. Por exemplo, essa propriedade retorna **True** mesmo quando o caractere é posicionado fora da área de exibição visível ou quando o quadro de caracteres atual não contém imagens. A configuração dessa propriedade se aplica a todos os clientes do caractere.

Esta propriedade é somente para leitura. Para tornar um caractere visível ou oculto, use os [**métodos Show**](show-method.md) ou [**Hide.**](https://www.bing.com/search?q=**Hide**)

 

 




