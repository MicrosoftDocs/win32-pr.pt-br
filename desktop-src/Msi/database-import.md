---
description: O método de importação do objeto de banco de dados importa uma tabela de banco de dados de arquivos mortos de texto, descartando qualquer tabela existente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Método Database. Import
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Import
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b931b77e6cf736bc291079532d20d9c6b48dd243
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756733"
---
# <a name="databaseimport-method"></a>Método Database. Import

O método de **importação** do objeto de [**banco de dados**](database-object.md) importa uma tabela de banco de dados de [arquivos mortos de texto](text-archive-files.md), descartando qualquer tabela existente.

## <a name="syntax"></a>Sintaxe


```JScript
Database.Import(
  path,
  file
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*path* 
</dt> <dd>

Pasta necessária onde o arquivo de texto está presente.

</dd> <dt>

*file* 
</dt> <dd>

Nome necessário do arquivo a ser importado. Isso não inclui a pasta, pois ela deve ser definida no objeto Path. O nome da tabela é especificado dentro do arquivo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Backup de banco de dados**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




