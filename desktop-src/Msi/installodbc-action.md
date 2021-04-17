---
description: A ação InstallODBC instala os drivers, os tradutores e as fontes de dados na tabela ODBCDriver, na tabela ODBCTranslator e na tabela ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Ação InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812918"
---
# <a name="installodbc-action"></a>Ação InstallODBC

A ação InstallODBC instala os drivers, os tradutores e as fontes de dados na tabela [ODBCDriver](odbcdriver-table.md), na tabela [ODBCTranslator](odbctranslator-table.md)e na [tabela ODBCDataSource](odbcdatasource-table.md). Se um driver ou tradutor já existir, a ação InstallODBC fará as chamadas SQL necessárias para a instalação.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallODBC não copia nem remove arquivos e deve ser posterior a ações que copiam ou removem arquivos.

## <a name="actiondata-messages"></a>Mensagens ActionData

A tabela a seguir identifica as mensagens ActionData para cada driver instalado.



| Campo       | Descrição                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrição do driver. A chave do driver ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Pasta.                                                                  |
| \[4, 5,...\] | Pares de atributo e valor de [odbcattribute](odbcattribute-table.md). |



 

A tabela a seguir identifica as mensagens ActionData para cada tradutor instalado.



| Campo       | Descrição                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrição do driver. A chave do driver ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Pasta.                                                                  |
| \[4, 5,...\] | Pares de atributo e valor de [odbcattribute](odbcattribute-table.md). |



 

A tabela a seguir identifica as mensagens ActionData para cada fonte de dados instalada.



| Campo       | Descrição                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrição do driver. A chave do driver ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Registro: ODBC \_ Add \_ DSN ou ODBC \_ Add \_ Sys \_ DSN.                     |
| \[4, 5,...\] | Pares de atributo e valor de [odbcattribute](odbcattribute-table.md). |



 

## <a name="remarks"></a>Comentários

O Gerenciador de driver ODBC deve ser criado no pacote do Microsoft Installer e um componente chamado ODBCDriverManager deve ser incluído. O Gerenciador é instalado, se necessário.

Para renomear o componente, defina uma propriedade chamada ODBCDriverManager como o novo nome do componente. Se um Gerenciador de driver ODBC de 64 bits for instalado, o componente que o transporta deve ser nomeado ODBCDriverManager64.

-   A ação InstallODBC consulta a [tabela ODBCDataSource](odbcdatasource-table.md) e a [tabela ODBCSourceAttribute](odbcsourceattribute-table.md) para cada fonte de dados a ser instalada e os atributos da fonte de dados.
-   A ação InstallODBC consulta a [tabela ODBCDriver](odbcdriver-table.md) e a [tabela ODBCTranslator](odbctranslator-table.md) para cada driver e tradutor selecionado para instalação.
-   A ação InstallODBC consulta a [tabela odbcattribute](odbcattribute-table.md) para obter os atributos dos drivers e tradutores.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de Windows Installer](windows-installer-examples.md)
</dt> </dl>

 

 



