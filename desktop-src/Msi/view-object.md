---
description: O objeto View representa um conjunto de resultados obtido ao processar uma consulta usando o método OpenView do objeto Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Exibir objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790030"
---
# <a name="view-object"></a>Exibir objeto

O objeto **View** representa um conjunto de resultados obtido ao processar uma consulta usando o método [**OpenView**](database-openview.md) do objeto [**Database**](database-object.md) . Antes que qualquer dado possa ser transferido, a consulta deve ser executada usando o método [**Execute**](view-execute.md) , passando para todos os parâmetros substituíveis designados na cadeia de caracteres de consulta SQL. A consulta pode ser executada novamente, com parâmetros diferentes, se necessário, mas somente depois de liberar o conjunto de resultados, seja buscando todos os registros ou chamando o método [**Close**](view-close.md) .

## <a name="members"></a>Membros

O objeto **View** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **View** tem esses métodos.



| Método                            | Descrição                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fechar**](view-close.md)       | Encerra a execução da consulta e libera recursos do banco de dados.<br/>                                                                                                          |
| [**Executados**](view-execute.md)   | Usa o token de ponto de interrogação para representar parâmetros em uma consulta SQL. Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.<br/> |
| [**Obtida**](view-fetch.md)       | Retorna um objeto [**Record**](record-object.md) contendo os dados de coluna solicitados se mais linhas estiverem disponíveis no conjunto de resultados, caso contrário, retornará NULL.<br/>      |
| [**GetError**](view-geterror.md) | Retorna o erro de validação e o nome da coluna para o qual o erro ocorreu.<br/>                                                                                           |
| [**Alterar**](view-modify.md)     | Modifica uma linha de banco de dados com um objeto de [**registro**](record-object.md) modificado obtido pelo método [**Fetch**](view-fetch.md) .<br/>                                   |



 

### <a name="properties"></a>Propriedades

O objeto **View** tem essas propriedades.



| Propriedade                                         | Descrição                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Retorna um objeto de [**registro**](record-object.md) que contém as informações solicitadas sobre cada coluna no conjunto de resultados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




