---
title: Propriedade Visible (objeto characters)
description: Propriedade Visible
ms.assetid: c06d623d-8997-413a-b4ab-24275eccfa10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a994fd59e5eaaebcaabbd9257b860fa4e27a09b4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105813305"
---
# <a name="visible-property-characters-object"></a>Propriedade Visible (objeto characters)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna um valor booleano que indica se o caractere está visível.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agente ***. Caracteres (**"* characterid *" * *). Visível**



| Valor | Descrição                            |
|-------|----------------------------------------|
| True  | O caractere é exibido.            |
| Falso | O caractere é oculto (não visível). |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta propriedade indica se o quadro do caractere está sendo exibido. Isso não significa necessariamente que há uma imagem na tela. Por exemplo, essa propriedade retorna **true** mesmo quando o caractere é posicionado fora da área de exibição visível ou quando o quadro de caracteres atual não contém nenhuma imagem. A configuração dessa propriedade se aplica a todos os clientes do caractere.

Esta propriedade é somente para leitura. Para tornar um caractere visível ou oculto, use os métodos [**show**](show-method.md) ou [**Hide**](https://www.bing.com/search?q=**Hide**) .

 

 




