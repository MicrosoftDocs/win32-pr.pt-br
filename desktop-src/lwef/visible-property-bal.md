---
title: Propriedade Visible (objeto Balloon)
description: Saiba mais sobre a propriedade Visible do objeto Balloon, que retorna ou define a configuração visível para o balão de palavras do caractere especificado.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac587fa649f2a8ccb5ea83ddc077050a8548d2
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396321"
---
# <a name="visible-property-balloon-object"></a>Propriedade Visible (objeto Balloon)

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Retorna ou define a configuração visível para o balão de palavra do caractere especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*Agente ***. Caracteres (**"* characterid *" * *). Balão.* *  \[  =  *booliano* visível\]



| Parte      | Descrição                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se o balão de palavra está visível.<br/> **Verdadeiro** O balão está visível.<br/> **Falso** O balão está oculto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você seguir uma chamada [**Speak**](speak-method.md) ou [**Think**](think-method.md) com uma instrução para tentar alterar a propriedade do balão, ela não poderá afetar o estado visível do balão, pois a chamada **Speak** ou **Think** será enfileirada, mas a chamada definindo o estado visível do balão não. Portanto, defina esse valor somente quando nenhuma chamada de **fala** ou **Think** estiver na fila do caractere.

Se você tentar definir essa propriedade enquanto o caractere estiver falando, movendo ou sendo arrastado, a configuração de propriedade não entrará em vigor até que a operação anterior seja concluída.

Chamar os métodos [**Speak**](speak-method.md) e [**Think**](think-method.md) automaticamente torna o balão visível, definindo a propriedade [**Visible**](visible-property.md) como **true**. Se a propriedade AutoOcultar do balão do caractere estiver habilitada, o balão será ocultado automaticamente depois que o texto de saída for falado. Clicar ou arrastar um caractere que não esteja falando no momento também ocultará automaticamente o balão mesmo se sua configuração de AutoOcultar estiver desabilitada. Você pode alterar a configuração de AutoOcultar do caractere usando a propriedade [**Style**](style-property.md) do balão.

### <a name="see-also"></a>Consulte Também

[**Propriedade de estilo**](style-property.md)


 

 





