---
description: A tabela BBControl lista os controles a serem exibidos em cada visor.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Tabela BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70198167c866195204ec6cbcf644b92f3489a4ff44e14e719efbf5c6647e30c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754366"
---
# <a name="bbcontrol-table"></a>Tabela BBControl

A tabela BBControl lista os controles a serem exibidos em cada visor.

A tabela BBControl tem as seguintes colunas.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| Outdoor\_ | [Identificador](identifier.md)       | Y   | N        |
| BBControl   | [Identificador](identifier.md)       | Y   | N        |
| Tipo        | [Identificador](identifier.md)       | N   | N        |
| X           | [Inteiro](integer.md)             | N   | N        |
| Y           | [Inteiro](integer.md)             | N   | N        |
| Largura       | [Inteiro](integer.md)             | N   | N        |
| Altura      | [Inteiro](integer.md)             | N   | N        |
| Atributos  | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Texto        | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Outdoor\_
</dt> <dd>

Nome do mamão.

Chave externa para a coluna um da [tabela Dolei.](billboard-table.md)

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nome do controle. Esse nome deve ser exclusivo dentro de um cartaz, mas pode ser repetido em diferentes remos. Essa coluna combinada com a coluna \_ Demão forma a chave primária para a tabela.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

O tipo do controle. Somente controles estáticos, como [um texto,](text-control.md) [bitmap,](bitmap-control.md) [ícone](icon-control.md)ou controle personalizado podem ser colocados em um menu. Para ver uma lista completa de controles, consulte a [seção Controles.](controls.md)

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

Coordenada horizontal do canto superior esquerdo do limite retangular do controle. As unidades são [unidades do instalador](installer-units.md). Essa coordenada é medida em relação ao controle de ano e não em relação à caixa de diálogo. Use apenas números não negativos.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

Coordenada vertical do canto superior esquerdo do limite retangular do controle. As unidades são [unidades do instalador](installer-units.md). Essa coordenada é medida em relação ao controle de ano e não em relação à caixa de diálogo. Esse número deve ser não negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largura
</dt> <dd>

Largura do limite retangular do controle. As unidades são [unidades do instalador](installer-units.md). Esse número deve ser não negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altura
</dt> <dd>

Altura do limite retangular do controle. As unidades são [unidades do instalador](installer-units.md). Esse número deve ser não negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Uma palavra de 32 bits que especifica os sinalizadores de atributo a serem aplicados a esse controle. Esse número deve ser não negativo e especificar um atributo para um controle estático que é válido para posicionamento em um mercado. Para obter informações sobre os valores numéricos a inserir nesse campo, consulte o atributo específico em [Atributos de controle](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Essa coluna contém uma cadeia de caracteres localizável usada para definir o texto inicial no controle se o controle exibir texto. A cadeia de caracteres será truncada se o texto for muito longo para caber no controle. Essa coluna conterá [](binary-table.md) uma chave na tabela Binário se o controle for um botão de push ou uma caixa de seleção contendo um ícone ou bitmap. Não é possível mostrar texto e uma imagem no mesmo botão. Essa coluna pode ser deixada em branco.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores inteiros para x, y, largura e altura estão nas unidades [do instalador](installer-units.md), não em unidades de diálogo. Uma unidade do instalador é igual a um décimo segundo da altura do tamanho da fonte MS Sans Serif de 10 pontos. As coordenadas para os controles são relativas ao controle de mamão, não à caixa de diálogo.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



