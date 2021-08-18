---
title: Método Think
description: Método Think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c535912962a51961ae3f88f5cca412a55ecfa27506442aa78274fe697f2d7a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975506"
---
# <a name="think-method"></a>Método Think

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Exibe o texto especificado para o caractere especificado em um balão de palavra "thought".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). Pensar_ *  \[ *em texto*\]



| Parte   | Descrição                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | Opcional. Uma cadeia de caracteres que especifica a saída de pensamento do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Assim como [**o método Speak,**](speak-method.md) o método **Think** é uma solicitação na  fila que exibe texto em um balão de palavra, exceto pelo fato de que o balão Pensar palavra difere visualmente. Além disso, o balão dá suporte apenas à marca de controle de fala Indicador (**\\ Mrk**) e ignora qualquer outra marca de controle de fala. Ao **contrário de Speak**, o método **Think** não altera o estado de animação do caractere.

As [**propriedades**](/windows/desktop/lwef/the-balloon-object) do objeto Balão afetam a saída dos métodos [**Speak**](speak-method.md) e **Think.** Por exemplo, a propriedade [**Enabled**](enabled-property.md) do objeto **Balloon** deve ser **True** para que o texto seja exibido.

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um [**objeto Request.**](/windows/desktop/lwef/the-request-object) Além disso, se o arquivo não tiver  sido carregado, o servidor define a propriedade [**Status**](status-property.md) do objeto Request como "failed" com um número de código de erro apropriado.

A quebra automática de palavras do agente na palavra balão quebra palavras usando caracteres de espaço em branco (por exemplo, Espaço ou Guia). No entanto, se não puder, ele poderá quebrar uma palavra para se ajustar ao balão. Em idiomas como japonês, chinês e tailandês em que espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> De definir a ID de idioma do caractere antes de usar o [**método Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro do balão de palavras.

 

 

 