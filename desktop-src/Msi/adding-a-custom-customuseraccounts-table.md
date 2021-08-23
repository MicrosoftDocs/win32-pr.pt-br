---
description: Uma especificação do exemplo é que as informações da conta de usuário sejam lidas de uma tabela personalizada no banco de dados de instalação e não codificadas na ação personalizada.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Adicionando uma tabela CustomUserAccounts personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede08ad733e2870e970416da3de345bfc89b7e63147bc848f3d36ffe66721585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066456"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Adicionando uma tabela CustomUserAccounts personalizada

Uma especificação do exemplo é que as informações da conta de usuário sejam lidas de uma tabela personalizada no banco de dados de instalação e não codificadas na ação personalizada.

Adicione uma tabela personalizada ao banco de dados de instalação de exemplo chamado CustomUserAccounts para manter informações de conta de usuário. Consulte [Exemplos de consultas de banco](examples-of-database-queries-using-sql-and-script.md) de dados usando SQL script e para ver um exemplo de como adicionar uma tabela personalizada. Use o esquema a seguir para a tabela CustomUserAccounts. Consulte [Formato de definição de](column-definition-format.md) coluna para ver uma explicação dos tipos de coluna.



| Coluna     | Tipo | Chave | Nullable | Descrição                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | s72  | Y   | N        | Nome da conta de usuário que está sendo criada.                                                                                                                                                                                                                                                                        |
| Senha   | s72  |     | N        | Nome da propriedade que contém a senha da conta. Essa é uma [propriedade pública](public-properties.md) definida na linha de comando ou por meio de um controle [de edição](edit-control.md) na interface do usuário. Esse controle de edição deve ter o [Atributo de Controle de Senha](password-control-attribute.md). |
| Atributos | i4   |     | Y        | Atributos para conta. Eles são definidos como os **valores DWORD** para o membro de sinalizadores usri1 \_ da estrutura USER INFO \_ \_ 1.                                                                                                                                                                              |



 

Depois que a tabela CustomUserAccounts tiver sido adicionada ao banco de dados, você poderá editar essa tabela usando o Orca, um editor de tabela fornecido com o SDK do instalador do Windows ou outro editor. Insira o registro a seguir na tabela CustomUserAccounts para criar uma conta de usuário protegida por senha para um usuário chamado TestUser. Observe que 512 é o valor numérico para a CONTA \_ NORMAL DA \_ UNIVERSIDADE.

Tabela CustomUserAccounts



| UserName | Senha         | Atributos |
|----------|------------------|------------|
| Testuser | TESTUSERPASSWORD | 512        |



 

Adicione os seguintes registros à tabela \_ Validação da tabela personalizada.

[\_Tabela de validação](-validation-table.md)



| Tabela              | Coluna     | Nullable | Minvalue | MaxValue   | Keytable | KeyColumn | Categoria                     | Definir | Descrição |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | Senha   | N        |          |            |          |           | [Identificador](identifier.md) |     |             |
| CustomUserAccounts | Atributos | Y        | 0        | 2147483647 |          |           | nulo                         |     |             |



 

Continue a [autor das tabelas ActionText e Error](authoring-the-actiontext-and-error-tables.md).

 

 



