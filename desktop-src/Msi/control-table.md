---
description: A tabela de controle define os controles que aparecem em cada caixa de diálogo.
ms.assetid: cbe7acd6-b916-45f3-b694-d2345c5a892a
title: Tabela de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e1832a2cb600e8d7a27b43bc28c94836396d74a50a90b44d0e5013bde973c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638528"
---
# <a name="control-table"></a>Tabela de controle

A tabela de controle define os controles que aparecem em cada caixa de diálogo.

A tabela de controle tem as colunas a seguir.



| Coluna        | Tipo                               | Chave | Nullable |
|---------------|------------------------------------|-----|----------|
| caixa de diálogo\_      | [Identificador](identifier.md)       | Y   | N        |
| Control       | [Identificador](identifier.md)       | Y   | N        |
| Digite          | [Identificador](identifier.md)       | N   | N        |
| X             | [Inteiro](integer.md)             | N   | N        |
| Y             | [Inteiro](integer.md)             | N   | N        |
| Largura         | [Inteiro](integer.md)             | N   | N        |
| Altura        | [Inteiro](integer.md)             | N   | N        |
| Atributos    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Propriedade      | [Identificador](identifier.md)       | N   | Y        |
| Texto          | [Binário](formatted.md)         | N   | Y        |
| \_Próximo controle | [Identificador](identifier.md)       | N   | Y        |
| Ajuda          | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>'\_
</dt> <dd>

Chave externa para a primeira coluna da [tabela de diálogo](dialog-table.md), o nome da caixa de diálogo.

</dd> <dt>

<span id="Control"></span><span id="control"></span><span id="CONTROL"></span>Controlo
</dt> <dd>

Nome do controle. Esse nome deve ser exclusivo dentro de uma caixa de diálogo, mas pode ser repetido em caixas de diálogo diferentes. A coluna de controle combinada com a \_ coluna da caixa de diálogo formam a chave primária para esta tabela.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

O tipo do controle. Para obter uma lista de tipos de controle, consulte [controles](controls.md).

</dd> <dt>

<span id="X"></span><span id="x"></span>W.x.y.
</dt> <dd>

Coordenada horizontal do canto superior esquerdo do limite retangular do controle. Este deve ser um número não negativo. Consulte [atributo de controle de posição](position-control-attribute.md).

</dd> <dt>

<span id="Y"></span><span id="y"></span>Iar
</dt> <dd>

Coordenada vertical do canto superior esquerdo do limite retangular do controle. Este deve ser um número não negativo. Consulte [atributo de controle de posição](position-control-attribute.md).

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largura
</dt> <dd>

Largura do limite retangular do controle. Este deve ser um número não negativo. Consulte [atributo de controle de posição](position-control-attribute.md).

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Tamanho
</dt> <dd>

Altura do limite retangular do controle. Este deve ser um número não negativo. Consulte [atributo de controle de posição](position-control-attribute.md).

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Uma palavra de 32 bits que especifica os sinalizadores de bits a serem aplicados a este controle. Ele deve ser um número não negativo e os valores permitidos dependem do tipo de controle. Para obter uma lista de todos os atributos de controle e o valor a ser inserido neste campo, consulte [atributos de controle](control-attributes.md).

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

O nome de uma propriedade definida a ser vinculada a este controle. Os valores de botão de opção, caixa de listagem e caixa de combinação são vinculados a um grupo vinculando-se à mesma propriedade. Essa coluna é necessária para controles ativos.

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto
</dt> <dd>

Uma cadeia de caracteres localizável usada para definir o texto inicial contido em um controle. A cadeia de caracteres também pode conter Propriedades inseridas. Para obter a sintaxe de uma cadeia de caracteres formatada contendo propriedades, consulte a função [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) . Especifique o tamanho, a fonte e a cor do texto prefixando a cadeia de texto com { \\ Style}, em que Style é um estilo de texto criado na coluna TextStyle da [tabela TextStyle](textstyle-table.md). A cadeia de texto será truncada se for muito longa para caber no controle. A cadeia de texto pode estar em branco.

A criação especial da cadeia de caracteres de texto [formatado](formatted.md) nesse campo será necessária se o texto for exibido por um [controle de texto](text-control.md) localizado em uma caixa de diálogo com o atributo TrackDiskpace. Esse é o caso especificado pelo [bit do estilo da caixa de diálogo TrackDiskSpace](trackdiskspace-dialog-style-bit.md) aparecendo nos atributos da tabela de [diálogo](dialog-table.md). Nesse caso, se a cadeia de caracteres Formatada na coluna Texto da tabela Controle começar com " " e terminar com " , você deverá adicionar um espaço no final da cadeia de \[ \] caracteres. Por exemplo, se DlgTextFont for uma propriedade que será definida como "{ DlgFontBold}", a cadeia de caracteres formatada \\ " \[ DlgTextFont \] MyText \[ ProductName " exigirá o espaço no final após o colchete de \] fechamento. Esse espaço extra é exigido pelo instalador para exibir corretamente o texto no controle Texto.

Você pode inserir uma cadeia de caracteres de texto descritivo curta para os controles [VolumeCostList,](volumecostlist-control.md) [ListView,](listview-control.md) [DirectoryList](directorylist-control.md)e [SelectionTree](selectiontree-control.md). Esse texto não é visto pelo usuário, mas pode ser lido por leitores de tela como a descrição do controle.

Consulte também [Acessibilidade](accessibility.md).

</dd> <dt>

<span id="Control_Next"></span><span id="control_next"></span><span id="CONTROL_NEXT"></span>Controlar \_ Próximo
</dt> <dd>

O nome de outro controle na mesma caixa de diálogo e uma chave externa para a segunda coluna da tabela Controle. Se o foco na caixa de diálogo estiver no controle na coluna Controle, a tecla Tab moverá o foco para o controle listado na coluna Controlar \_ Próximo. Portanto, essa coluna é usada para especificar a ordem de tabulação dos controles na caixa de diálogo. Os links entre os controles devem formar um ciclo fechado. Alguns controles, como controles de texto estáticos, podem ser deixados de fora do ciclo. Nesse caso, esse campo pode ser deixado em branco.

Consulte também [Acessibilidade](accessibility.md).

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>Ajuda
</dt> <dd>

Opcional, cadeias de caracteres de texto localizáveis que são usadas com o botão Ajuda. A cadeia de caracteres é dividida em duas partes por um caractere separador ( \| ). A primeira parte da cadeia de caracteres é usada como texto da Dica de Ferramenta. Esse texto é usado por leitores de tela para controles que contêm uma imagem. A segunda parte da cadeia de caracteres é reservada para uso futuro. O caractere separador será necessário mesmo se apenas um dos dois tipos de texto estiver presente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os valores inteiros para x, y, largura e altura estão nas unidades [do instalador](installer-units.md), não em unidades de diálogo. Uma unidade do instalador é igual a um décimo segundo da altura do tamanho da fonte MS Sans Serif de 10 pontos. As coordenadas para os controles são relativas ao ano.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE31](ice31.md)  
[ICE32](ice32.md)  
[ICE34](ice34.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
[ICE95](ice95.md)  
</dl>

 

 



