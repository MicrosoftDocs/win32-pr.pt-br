---
title: Propriedade Visible (objeto Commands)
description: Propriedade Visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369156"
---
# <a name="visible-property-commands-object"></a>Propriedade Visible (objeto Commands)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define um valor que determina se a legenda da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) é exibida no menu pop-up do caractere.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*Agente ***. Caracteres (**"* characterid *" * *). Comandos.* *  \[  =  *booliano* visível\]



| Parte      | Descrição                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) aparece no menu pop-up do caractere. <br/> **Verdadeiro** A legenda é exibida.<br/> **Falso** A legenda não aparece.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Para que a legenda apareça no menu pop-up do caractere quando seu aplicativo não for o cliente de entrada-ativo, essa propriedade deverá ser definida como **true** e a propriedade [**Caption**](caption-property.md) definida para a coleção de comandos. Além disso, essa propriedade deve ser definida como **true** para que os comandos em sua coleção sejam exibidos no menu pop-up quando seu aplicativo for Input-active.

 

