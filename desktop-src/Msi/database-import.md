---
description: O método Import do objeto Database importa uma tabela de banco de dados de arquivos de texto, soltando qualquer tabela existente.
ms.assetid: 9ecc31d9-bccd-48cc-b205-9ce70aaf638a
title: Método Database.Import
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
ms.openlocfilehash: 31bd306475460b03e9b4b5137cbd8fe214128dbec0dac516d2d9557de137a82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075026"
---
# <a name="databaseimport-method"></a>Método Database.Import

O **método Import** do objeto [**Database**](database-object.md) importa uma tabela de banco de dados de arquivos de [texto,](text-archive-files.md)soltando qualquer tabela existente.

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

Pasta necessária em que o arquivo de texto está presente.

</dd> <dt>

*file* 
</dt> <dd>

Nome necessário do arquivo a ser importado. Isso não inclui a pasta , pois ela deve ser definida no objeto path. O nome da tabela é especificado dentro do arquivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método falhar, você poderá obter informações de erro estendidas usando o [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase é definido como \_ 000C109D-0000-0000-C000-00000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Banco de dados**](database-object.md)
</dt> <dt>

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)
</dt> </dl>

 

 




