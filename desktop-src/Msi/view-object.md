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
ms.openlocfilehash: f5025df952ce6e3c5ce43bf3dcb93748a241702b8c4e2f52cd9d0fd00103dc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145269"
---
# <a name="view-object"></a>Exibir objeto

O **objeto View** representa um conjunto de resultados obtido ao processar uma consulta usando o método [**OpenView**](database-openview.md) do [**objeto Database.**](database-object.md) Antes que qualquer dado possa ser transferido, a consulta deve ser executada usando o método [**Execute,**](view-execute.md) passando para ele todos os parâmetros substituíveis designados dentro da cadeia de caracteres SQL consulta. A consulta pode ser executada novamente, com parâmetros diferentes, se necessário, mas somente depois de liberar o conjunto de resultados buscando todos os registros ou chamando o [**método Close.**](view-close.md)

## <a name="members"></a>Membros

O **objeto View** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto View** tem esses métodos.



| Método                            | Descrição                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Perto**](view-close.md)       | Encerra a execução da consulta e libera recursos de banco de dados.<br/>                                                                                                          |
| [**Executar**](view-execute.md)   | Usa o token de ponto de interrogação para representar parâmetros em uma SQL consulta. Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.<br/> |
| [**Buscar**](view-fetch.md)       | Retorna um [**objeto Record**](record-object.md) que contém os dados de coluna solicitados se mais linhas estão disponíveis no conjunto de resultados; caso contrário, ele retorna nulo.<br/>      |
| [**Geterror**](view-geterror.md) | Retorna o erro validação e o nome da coluna para o qual o erro ocorreu.<br/>                                                                                           |
| [**Modificar**](view-modify.md)     | Modifica uma linha de banco de dados com um [**objeto Record**](record-object.md) modificado obtido pelo [**método Fetch.**](view-fetch.md)<br/>                                   |



 

### <a name="properties"></a>Propriedades

O **objeto View** tem essas propriedades.



| Propriedade                                         | Descrição                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**Columninfo**](view-columninfo.md)<br/> | Retorna um [**objeto Record**](record-object.md) que contém as informações solicitadas sobre cada coluna no conjunto de resultados.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView é definido como \_ 000C109C-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




