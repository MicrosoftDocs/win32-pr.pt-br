---
description: Esta é uma tabela temporária somente leitura usada para exibir transformações com o modo de exibição de transformação. Essa tabela nunca é persistida pelo instalador.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Tabela de _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505804"
---
# <a name="_transformview-table"></a>\_Tabela de transformview

Esta é uma tabela temporária somente leitura usada para exibir transformações com o modo de exibição de transformação. Essa tabela nunca é persistida pelo instalador.

Para invocar o modo de exibição de transformação, obtenha um identificador e abra o banco de dados de referência. Consulte [obtendo um identificador de banco de dados](obtaining-a-database-handle.md). Chame [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) com o \_ erro MSITRANSFORM \_ VIEWTRANSFORM. Isso interrompe a transformação de ser aplicada ao banco de dados e despeja o conteúdo da transformação na \_ tabela do transformview. Os dados na tabela podem ser acessados usando consultas SQL. Consulte [trabalhando com consultas](working-with-queries.md).

A \_ tabela transformview não é limpa quando outra transformação é aplicada. A tabela reflete o efeito cumulativo de aplicativos sucessivos. Para exibir as transformações separadamente, você deve liberar a tabela.

A \_ tabela transformview tem as colunas a seguir.



| Coluna  | Tipo                         | Chave | Nullable |
|---------|------------------------------|-----|----------|
| Tabela   | [Identificador](identifier.md) | S   | N        |
| Coluna  | [Text](text.md)             | S   | N        |
| Linha     | [Text](text.md)             | S   | S        |
| Dados    | [Text](text.md)             | N   | S        |
| Current | [Text](text.md)             | N   | S        |



 

## <a name="column"></a>Coluna

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela
</dt> <dd>

Nome de uma tabela de banco de dados alterada.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha
</dt> <dd>

Nome de uma coluna de tabela alterada ou inserir, excluir, criar ou descartar.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila
</dt> <dd>

Uma lista dos valores de chave primária separados por tabulações. Valores nulos de chave primária são representados por um único caractere de espaço. Um valor nulo nesta coluna indica uma alteração de esquema.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Dados, nome de um fluxo de dados ou uma definição de coluna.

</dd> <dt>

<span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Atualizados
</dt> <dd>

Valor atual do banco de dados de referência ou de um número de coluna.

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ transformview é mantido na memória por uma contagem de bloqueios, que pode ser lançada com o comando SQL a seguir.

"ALTER TABLE \_ Exformview Free".

Os dados na tabela podem ser acessados usando consultas SQL. A linguagem SQL tem duas divisões principais: DDL (linguagem de definição de dados) que é usada para definir todos os objetos em um banco de dados SQL e DML (linguagem de manipulação de dados) usada para selecionar, inserir, atualizar e excluir dados nos objetos definidos usando DDL.

As operações de transformação DML (linguagem de manipulação de dados) são indicadas a seguir. DML (linguagem de manipulação de dados) são as instruções no SQL que manipulam, em vez de definir, os dados.



| Operação de transformação | Resultado do SQL                                    |
|---------------------|-----------------------------------------------|
| Modificar dados         | tabela pilha fila dado {valor atual} |
| Inserir linha          | tabela "Inserir" {Row} nulo NULL              |
| Excluir linha          | tabela "Excluir" {Row} NULL NULL              |



 

As operações de transformação DDL (linguagem de definição de dados) são indicadas a seguir. O DDL (linguagem de definição de dados) são as instruções no SQL que definem, em vez de manipular, os dados.



| Operação de transformação | Resultado do SQL                                   |
|---------------------|----------------------------------------------|
| Adicionar coluna          | tabela pilha NULL {defn} {número da coluna} |
| Adicionar tabela           | tabela "CREATE" NULL NULL NULL              |
| Remover tabela          | tabela "REMOVER" NULL NULL NULO                |



 

Quando o aplicativo de uma transformação adiciona essa tabela, o campo de dados recebe texto que pode ser interpretado como um valor inteiro de 16 bits. O valor descreve a coluna denominada no campo coluna. Você pode comparar o valor inteiro com as constantes na tabela a seguir para determinar a definição da coluna alterada.



| bit                                                                                                       | Descrição                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7<br/>         | Hexadecimal: 0x0000 0x0100<br/> Decimal: 0 255<br/> Largura da Coluna<br/>                                                                                                                                                                                                                                  |
| <span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8<br/>                  | Hexadecimal: 0x0100<br/> Decimal: 256<br/> Uma coluna persistente. Zero significa uma coluna temporária. <br/>                                                                                                                                                                                                   |
| <span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9<br/>                  | Hexadecimal: 0x0200<br/> Decimal: 1023<br/> Uma coluna localizável. Zero significa que a coluna não pode ser localizada.<br/>                                                                                                                                                                                      |
| <span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11<br/> | Hexadecimal: 0x0000<br/> Decimal: 0<br/> Long integer<br/> Hexadecimal: 0x0400<br/> Decimal: 1024<br/> Inteiro curto<br/> Hexadecimal: 0x0800<br/> Decimal: 2048<br/> Objeto Binary<br/> Hexadecimal: 0x0C00<br/> Decimal: 3072<br/> String<br/> |
| <span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12<br/>              | Hexadecimal: 0x1000<br/> Decimal: 4096<br/> Coluna anulável. Zero significa que a coluna não permite valor nulo.<br/>                                                                                                                                                                                               |
| <span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13<br/>              | Hexadecimal: 0x2000<br/> Decimal: 8192<br/> Coluna de chave primária. Zero significa que esta coluna não é uma chave primária.<br/>                                                                                                                                                                                      |
| <span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15<br/> | Hexadecimal: 0x4000 0x8000<br/> Decimal: 16384 32768<br/> Reservado<br/>                                                                                                                                                                                                                                |



 

Para obter um exemplo de script que demonstre a \_ tabela transformview, consulte [exibir uma transformação](view-a-transform.md).

 

 




