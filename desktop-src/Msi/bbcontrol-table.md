---
description: A tabela BBControl lista os controles a serem exibidos em cada mural.
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: Tabela BBControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfebbdbc474ef88cbf26f34555deb4874840d005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778733"
---
# <a name="bbcontrol-table"></a>Tabela BBControl

A tabela BBControl lista os controles a serem exibidos em cada mural.

A tabela BBControl tem as colunas a seguir.



| Coluna      | Tipo                               | Chave | Nullable |
|-------------|------------------------------------|-----|----------|
| Mensagem\_ | [Identificador](identifier.md)       | S   | N        |
| BBControl   | [Identificador](identifier.md)       | S   | N        |
| Tipo        | [Identificador](identifier.md)       | N   | N        |
| X           | [Inteiro](integer.md)             | N   | N        |
| S           | [Inteiro](integer.md)             | N   | N        |
| Largura       | [Inteiro](integer.md)             | N   | N        |
| Altura      | [Inteiro](integer.md)             | N   | N        |
| Atributos  | [DoubleInteger](doubleinteger.md) | N   | S        |
| Texto        | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>Mensagem\_
</dt> <dd>

Nome do mural.

Chave externa para a coluna um da [tabela de mural](billboard-table.md).

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

Nome do controle. Esse nome deve ser exclusivo em um mural, mas pode ser repetido em diferentes murals. Essa coluna combinada com a coluna do mural \_ forma a chave primária para a tabela.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

O tipo do controle. Somente controles estáticos, como [texto](text-control.md), [bitmap](bitmap-control.md), [ícone](icon-control.md)ou controle personalizado, podem ser colocados em um mural. Para obter uma lista completa de controles, consulte a seção [controles](controls.md) .

</dd> <dt>

<span id="X"></span><span id="x"></span>W.x.y.
</dt> <dd>

Coordenada horizontal do canto superior esquerdo do limite retangular do controle. As unidades são [unidades de instalador](installer-units.md). Essa coordenada é medida relativa ao controle de mural e não relativa à caixa de diálogo. Use apenas números não negativos.

</dd> <dt>

<span id="Y"></span><span id="y"></span>Iar
</dt> <dd>

Coordenada vertical do canto superior esquerdo do limite retangular do controle. As unidades são [unidades de instalador](installer-units.md). Essa coordenada é medida relativa ao controle de mural e não relativa à caixa de diálogo. Esse número deve ser não negativo.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largura
</dt> <dd>

Largura do limite retangular do controle. As unidades são [unidades de instalador](installer-units.md). Esse número deve ser não negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Tamanho
</dt> <dd>

Altura do limite retangular do controle. As unidades são [unidades de instalador](installer-units.md). Esse número deve ser não negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Uma palavra de 32 bits que especifica os sinalizadores de atributo a serem aplicados a este controle. Esse número deve ser não negativo e especificar um atributo para um controle estático que seja válido para posicionamento em um mural. Para obter informações sobre os valores numéricos a serem inseridos nesse campo, consulte o atributo específico em [atributos de controle](control-attributes.md).

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Esta coluna contém uma cadeia de caracteres localizável usada para definir o texto inicial no controle se o controle exibir texto. A cadeia de caracteres será truncada se o texto for muito longo para caber no controle. Essa coluna contém uma chave para a [tabela binária](binary-table.md) se o controle for um botão de ação ou uma caixa de seleção contendo um ícone ou bitmap. Não é possível mostrar o texto e uma imagem no mesmo botão. Esta coluna pode ser deixada em branco.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores inteiros de x, y, Width e Height estão nas unidades de [instalação](installer-units.md), não nas unidades de caixa de diálogo. Uma unidade de instalador é igual a um décimo da altura do tamanho de fonte MS Sans Serif de 10 pontos. As coordenadas para os controles são relativas ao controle de mural, não à caixa de diálogo.

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

 

 



