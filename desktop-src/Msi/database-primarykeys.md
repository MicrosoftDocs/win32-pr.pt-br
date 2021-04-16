---
description: A propriedade PrimaryKeys do objeto Database retorna um objeto Record contendo o nome da tabela no campo 0 e os nomes de coluna (que compreendem as chaves primárias) em campos com sucesso correspondentes aos seus números de coluna.
ms.assetid: 9aeafda4-65b8-4469-a391-eb25ca72459d
title: Propriedade Database. PrimaryKeys
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.PrimaryKeys
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dc266bc2e563e6f32b7ff9b8c7c8cb0df69b723d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758961"
---
# <a name="databaseprimarykeys-property"></a>Propriedade Database. PrimaryKeys

A propriedade **primarykeys** do objeto [**Database**](database-object.md) retorna um objeto [**Record**](record-object.md) contendo o nome da tabela no campo 0 e os nomes de coluna (que compreendem as chaves primárias) em campos com sucesso correspondentes aos seus números de coluna. A contagem de campos do registro é a contagem de colunas de chave primária.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Database.PrimaryKeys
```



## <a name="property-value"></a>Valor da propriedade

Nome necessário de uma tabela existente. Um erro será gerado se a tabela não existir.

## <a name="remarks"></a>Comentários

A propriedade **primarykeys** não pode ser usada com a [ \_ tabela tabelas](-tables-table.md) ou com a [ \_ tabela Columns](-columns-table.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




