---
description: Uma especificação do exemplo é que as informações da conta de usuário sejam lidas de uma tabela personalizada no banco de dados de instalação e não embutidas em código na ação personalizada.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Adicionando uma tabela CustomUserAccounts personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750258"
---
# <a name="adding-a-custom-customuseraccounts-table"></a>Adicionando uma tabela CustomUserAccounts personalizada

Uma especificação do exemplo é que as informações da conta de usuário sejam lidas de uma tabela personalizada no banco de dados de instalação e não embutidas em código na ação personalizada.

Adicione uma tabela personalizada ao banco de dados de instalação de exemplo chamado CustomUserAccounts para manter as informações da conta de usuário. Consulte [exemplos de consultas de banco de dados usando SQL e script](examples-of-database-queries-using-sql-and-script.md) para obter um exemplo de como adicionar uma tabela personalizada. Use o esquema a seguir para a tabela CustomUserAccounts. Consulte [formato de definição de coluna](column-definition-format.md) para obter uma explicação dos tipos de coluna.



| Coluna     | Tipo | Chave | Nullable | Descrição                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UserName   | s72  | S   | N        | Nome da conta de usuário que está sendo criada.                                                                                                                                                                                                                                                                        |
| Senha   | s72  |     | N        | Nome da propriedade que contém a senha da conta. Essa é uma [propriedade pública](public-properties.md) definida na linha de comando ou por meio de um [controle de edição](edit-control.md) na interface do usuário. Esse controle de edição deve ter o [atributo de controle de senha](password-control-attribute.md). |
| Atributos | i4   |     | S        | Atributos para a conta. Eles são definidos como os valores **DWORD** para o \_ membro flags usri1 da estrutura info do usuário \_ \_ 1.                                                                                                                                                                              |



 

Depois que a tabela CustomUserAccounts tiver sido adicionada ao banco de dados, você poderá editar essa tabela usando orca, um editor de tabela fornecido com o SDK do Windows Installer ou outro editor. Insira o registro a seguir na tabela CustomUserAccounts para criar uma conta de usuário protegida por senha para um usuário chamado TestUser. Observe que 512 é o valor numérico para a \_ conta normal da UF \_ .

Tabela CustomUserAccounts



| UserName | Senha         | Atributos |
|----------|------------------|------------|
| User | TESTUSERPASSWORD | 512        |



 

Adicione os seguintes registros à \_ tabela de validação para a tabela personalizada.

[\_Tabela de validação](-validation-table.md)



| Tabela              | Coluna     | Nullable | MinValue | MaxValue   | KeyTable | KeyColumn | Category                     | Definir | Descrição |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| CustomUserAccounts | UserName   | N        |          |            |          |           | [Text](text.md)             |     |             |
| CustomUserAccounts | Senha   | N        |          |            |          |           | [Identificador](identifier.md) |     |             |
| CustomUserAccounts | Atributos | S        | 0        | 2147483647 |          |           | nulo                         |     |             |



 

Continue a [criar as tabelas de erro e ActionText](authoring-the-actiontext-and-error-tables.md).

 

 



