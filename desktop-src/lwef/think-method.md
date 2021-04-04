---
title: Método think
description: Método think
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823720"
---
# <a name="think-method"></a>Método think

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Exibe o texto especificado para o caractere especificado em um balão de palavras "pensamento".

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres ("*** characterid * * *"). Think* o *  \[ *texto*\]



| Parte   | Descrição                                                       |
|--------|-------------------------------------------------------------------|
| *Text* | Opcional. Uma cadeia de caracteres que especifica a saída de pensamento do caractere. |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Como o método [**Speak**](speak-method.md) , o método **Think** é uma solicitação em fila que exibe texto em um balão de palavras, exceto pelo fato de que o balão de palavras de **reflexão** difere visualmente. Além disso, o balão dá suporte apenas à marca de controle de fala de indicador (**\\ mrk**) e ignora quaisquer outras marcas de controle de fala. Ao contrário do que se **fala**, o método **Think** não altera o estado de animação do caractere.

As propriedades do objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) afetam a saída dos métodos [**Speak**](speak-method.md) e **Think** . Por exemplo, a propriedade [**Enabled**](enabled-property.md) do objeto **Balloon** deve ser **true** para que o texto seja exibido.

Se você declarar uma referência de objeto e defini-la para esse método, ela retornará um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) . Além disso, se o arquivo não tiver sido carregado, o servidor definirá a propriedade [**status**](status-property.md) do objeto de **solicitação** como "failed" com um número de código de erro apropriado.

A quebra automática de palavras do agente no balão de palavras quebra palavras usando caracteres de espaço em branco (por exemplo, espaço ou tabulação). No entanto, se não puder, ele poderá quebrar uma palavra para se ajustar ao balão. Em linguagens como japonês, chinês e tailandês em que os espaços não são usados para quebrar palavras, insira um caractere de espaço de largura zero Unicode (0x200B) entre caracteres para definir quebras de palavras lógicas.

> [!Note]  
> Defina a ID do idioma do caractere antes de usar o método [**Speak**](speak-method.md) para garantir a exibição de texto apropriada dentro do balão do Word.

 

 

 