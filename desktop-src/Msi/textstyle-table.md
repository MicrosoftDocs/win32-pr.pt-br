---
description: A tabela TextStyle lista diferentes estilos de fonte usados em controles com texto.
ms.assetid: a351e67a-8f51-41bf-9202-56488b870fa7
title: Tabela TextStyle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9993362228e37f01c0e53683755f7bd1310eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921053"
---
# <a name="textstyle-table"></a>Tabela TextStyle

A tabela TextStyle lista diferentes estilos de fonte usados em controles com texto.

A tabela TextStyle tem as colunas a seguir.



| Coluna    | Tipo                               | Chave | Nullable |
|-----------|------------------------------------|-----|----------|
| Estilo] | [Identificador](identifier.md)       | S   | N        |
| FaceName  | [Text](text.md)                   | N   | N        |
| Tamanho      | [Inteiro](integer.md)             | N   | N        |
| Cor     | [DoubleInteger](doubleinteger.md) | N   | S        |
| StyleBits | [Inteiro](integer.md)             | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="TextStyle"></span><span id="textstyle"></span><span id="TEXTSTYLE"></span>Estilo]
</dt> <dd>

Esta coluna é o nome do estilo da fonte. Esse nome pode ser inserido na cadeia de texto para indicar uma alteração de estilo. Observe que o nome do estilo da fonte usado neste campo não deve terminar com os caracteres: \_ UL. Consulte [adicionando controles e texto](adding-controls-and-text.md).

</dd> <dt>

<span id="FaceName"></span><span id="facename"></span><span id="FACENAME"></span>FaceName
</dt> <dd>

Uma cadeia de caracteres que indica o nome da fonte. A cadeia de caracteres não deve ter mais de 31 caracteres.

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>Tamanho
</dt> <dd>

O tamanho da fonte medido em pontos. Este deve ser um número não negativo.

</dd> <dt>

<span id="Color"></span><span id="color"></span><span id="COLOR"></span>Cor
</dt> <dd>

Esta coluna especifica a cor do texto exibida por um [controle de texto](text-control.md). Todos os outros tipos de controles sempre usam a cor de texto padrão. O valor colocado nessa coluna deve ser calculado usando a seguinte fórmula: 65536 \* azul + 256 \* verde + vermelho, em que vermelho, verde e azul estão cada um no intervalo de 0-255. O valor não deve exceder 16777215, que é o valor de branco. O valor é 0 para preto, 255 para vermelho, 65280 para verde, 16711680 para azul e 8421504 para cinza. Deixar o campo vazio especifica a cor padrão.

Não coloque controles de [texto](text-control.md) transparentes na parte superior dos bitmaps coloridos. O texto pode não estar visível se o usuário alterar o esquema de cores de exibição. Por exemplo, o texto pode se tornar invisível se o usuário definir o parâmetro de alto contraste para acessibilidade.

</dd> <dt>

<span id="StyleBits"></span><span id="stylebits"></span><span id="STYLEBITS"></span>StyleBits
</dt> <dd>

Uma combinação de bits que indica a formatação do texto.

Os bits de estilo individuais têm os valores a seguir.



| Constante                             | Hexadecimal | Decimal | Estilo      |
|--------------------------------------|-------------|---------|------------|
| **msidbTextStyleStyleBitsBold**      | 0x001       | 1       | Negrito       |
| **msidbTextStyleStyleBitsItalic**    | 0x002       | 2       | Itálico     |
| **msidbTextStyleStyleBitsUnderline** | 0x004       | 4       | Underline  |
| **msidbTextStyleStyleBitsStrike**    | 0x008       | 8       | Riscar |



 

</dd> </dl>

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE31](ice31.md)  
[ICE45](ice45.md)  
</dl>

 

 



