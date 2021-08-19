---
title: Propriedade Visible (objeto De balão)
description: Saiba mais sobre a Propriedade Visível do objeto Balão, que retorna ou define a configuração visível para a palavra balão para o caractere especificado.
ms.assetid: cbda7f69-889a-45a0-9549-d27eddfcec57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101d454f90e01ebcf31619b935d1b90512648baf33a11883b6b971c3178fb871
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975476"
---
# <a name="visible-property-balloon-object"></a>Propriedade Visible (objeto De balão)

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Retorna ou define a configuração visível para o balão de palavra para o caractere especificado.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Sintaxe** 
</dt> <dd>

*agent***. Characters(**"* CharacterID *"**). Booliana Balloon.Visible* *  \[  =  \]



| Parte      | Descrição                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *booleano* | Uma expressão booliana que especifica se a palavra balão está visível.<br/> **True** O balão está visível.<br/> **False** O balão está oculto.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você seguir [](think-method.md) uma chamada Fale ou Pensar com uma instrução para tentar alterar [**a**](speak-method.md) propriedade  do  balão, ela poderá não afetar o estado Visível do balão porque a chamada Fale ou Pensar será ensuada, mas a definição de chamada do estado visível do balão não afetará. Portanto, de definir esse valor somente **quando nenhuma chamada Falar** ou **Pensar** estiver na fila do caractere.

Se você tentar definir essa propriedade enquanto o caractere estiver falando, movendo ou sendo arrastado, a configuração de propriedade não funcionará até que a operação anterior seja concluída.

Chamar os [**métodos Speak**](speak-method.md) and [**Think**](think-method.md) torna automaticamente o balão visível, definindo a [**propriedade Visible**](visible-property.md) como **True.** Se a propriedade AutoHide de balão do caractere estiver habilitada, o balão será ocultado automaticamente depois que o texto de saída for falado. Clicar ou arrastar um caractere que não está falando no momento também oculta automaticamente o balão, mesmo que sua configuração autoHide seja desabilitada. Você pode alterar a configuração autoHide do caractere usando a propriedade [**Style do**](style-property.md) balão.

### <a name="see-also"></a>Consulte Também

[**Propriedade Style**](style-property.md)


 

 





