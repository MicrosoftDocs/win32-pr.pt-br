---
description: O objeto de banco de dados acessa um banco de dados do instalador.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Objeto de banco de dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769323"
---
# <a name="database-object"></a>Objeto de banco de dados

O objeto de **banco de dados** acessa um banco de dados do instalador.

O objeto de **banco de dados** é liberado quando ele é retirado do escopo ou quando a variável de objeto associada a ele é definida como NULL. O método [**Commit**](database-commit.md) deve ser chamado antes que o objeto de **banco de dados** seja liberado para gravar todas as alterações persistentes. Se o método **Commit** não for chamado, o instalador executará uma reversão implícita após a destruição do objeto.

O cliente pode usar o procedimento a seguir para acesso a dados.

**Para consultar o sequenciamento de API**

1.  Obtenha um objeto de **banco de dados** chamando o objeto [**OpenDatabase**](installer-opendatabase.md) ou [**instalador**](installer-object.md) .
2.  Inicie uma consulta usando uma cadeia de caracteres SQL chamando o método [**OpenView**](database-openview.md) do objeto **Database** .
3.  Defina os parâmetros de consulta em um objeto de [**registro**](record-object.md) e execute a consulta de banco de dados chamando o método [**Execute**](view-execute.md) do objeto [**View**](view-object.md) . Isso produz um resultado que pode ser buscado ou atualizado.
4.  Chame o método [**Fetch**](view-fetch.md) do objeto [**View**](view-object.md) repetidamente para retornar objetos [**Record**](record-object.md) .
5.  Atualize as linhas de banco de dados de um objeto de [**registro**](record-object.md) obtido pelo método [**Fetch**](view-fetch.md) usando o método [**Modify**](view-modify.md) do objeto [**View**](view-object.md) .
6.  Libere a consulta e todos os registros não buscados chamando o método [**Close**](view-close.md) do objeto [**View**](view-object.md) .
7.  Mantenha todas as atualizações de banco de dados chamando o método [**Commit**](database-commit.md) do objeto **Database** .

## <a name="members"></a>Membros

O objeto de **banco de dados** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto de **banco de dados** tem esses métodos.



| Método                                                                    | Descrição                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Aplica a transformação a este banco de dados.<br/>                                                                                                                        |
| [**Compromisso**](database-commit.md)                                         | Finaliza a forma persistente do banco de dados.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Cria e popula o fluxo de informações resumidas de um arquivo de transformação existente.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Facilita a criação de caixas de diálogo e de mural, fornecendo o suporte necessário para exibir caixas de diálogo da interface do usuário armazenadas no banco de dados do instalador.<br/> |
| [**Exportação**](database-export.md)                                         | Copia a estrutura e os dados de uma tabela especificada para um arquivo morto de texto.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Cria uma transformação.<br/>                                                                                                                                           |
| [**Importar**](database-import.md)                                         | Importa uma tabela de banco de dados de um arquivo morto de texto.<br/>                                                                                                             |
| [**Mescle**](database-merge.md)                                           | Mescla o banco de dados de referência com o banco de dados base.<br/>                                                                                                          |
| [**AbrirModoDeExibição**](database-openview.md)                                     | Retorna um objeto [**View**](view-object.md) que representa a consulta especificada por uma cadeia de caracteres SQL.<br/>                                                                 |



 

### <a name="properties"></a>Propriedades

O objeto de **banco de dados** tem essas propriedades.



| Propriedade                                                                               | Descrição                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Banco de dados**](database-databasestate.md)<br/>                             | Retorna o estado de persistência do banco de dados.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Retorna um objeto de [**registro**](record-object.md) que contém o nome da tabela e os nomes de coluna (que abrangem as chaves primárias).<br/>                        |
| [**SummaryInformation (objeto de banco de dados)**](database-summaryinformation.md)<br/> | Retorna um objeto [**SummaryInfo**](summaryinfo-object.md) que pode ser usado para examinar, atualizar e adicionar propriedades ao fluxo de informações de resumo.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Retorna o estado de persistência da tabela.<br/>                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




