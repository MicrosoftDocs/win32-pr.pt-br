---
description: A tabela TextStyle lista diferentes estilos de fonte usados em controles que têm texto.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabela TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f8a5b3141314722bc5b92e34ea214fa8e1505babfbc8b7f942899e6c6779c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623483"
---
# <a name="textstyle-table"></a>Tabela TextStyle

A tabela TextStyle lista diferentes estilos de fonte usados em controles que têm texto.

A tabela TextStyle tem as seguintes colunas.



| Coluna    | Tipo                               | Chave | Nullable |
|-----------|------------------------------------|-----|----------|
| Textstyle | [Identificador](identifier.md)       | Y   | N        |
| FaceName  | [Text](text.md)                   | N   | N        |
| Tamanho      | [Inteiro](integer.md)             | N   | N        |
| Color     | [DoubleInteger](doubleinteger.md) | N   | Y        |
| StyleBits | [Inteiro](integer.md)             | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Textstyle
</dt> <dd>

Essa coluna é o nome do estilo da fonte. Esse nome pode ser inserido na cadeia de caracteres de texto para indicar uma alteração de estilo. Observe que o nome de estilo da fonte usado neste campo não deve terminar com os caracteres: \_ UL. Consulte [Adicionando controles e texto.](adding-controls-and-text.md)

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

Uma cadeia de caracteres que indica o nome da fonte. A cadeia de caracteres não deve ter mais de 31 caracteres.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Tamanho
</dt> <dd>

O tamanho da fonte medido em pontos. Esse deve ser um número não negativo.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Cor
</dt> <dd>

Essa coluna especifica a cor do texto exibida por um [Controle de Texto](text-control.md). Todos os outros tipos de controles sempre usam a cor de texto padrão. O valor colocado nesta coluna deve ser calculado usando a seguinte fórmula: azul 65536 + 256 verde + vermelho, em que vermelho, verde e azul estão cada um no intervalo de \* \* 0 a 255. O valor não deve exceder 16777215, que é o valor para branco. O valor é 0 para preto, 255 para vermelho, 65280 para verde, 16711680 azul e 8421504 cinza. Deixar o campo vazio especifica a cor padrão.

Não coloque controles [de Texto transparentes](text-control.md) sobre bitmaps coloridos. O texto poderá não ficar visível se o usuário mudar o esquema de cores de exibição. Por exemplo, o texto pode se tornar invisível se o usuário define o parâmetro de alto contraste para acessibilidade.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Uma combinação de bits que indica a formatação do texto.

Os bits de estilo individuais têm os seguintes valores.



| Constante                             | Hexadecimal | Decimal | Estilo      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Negrito       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Itálico     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Underline  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Fazer o strike out |



 

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



