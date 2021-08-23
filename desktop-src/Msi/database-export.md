---
description: O método Export do objeto Database copia a estrutura e os dados de uma tabela especificada para um arquivo morto de texto.
ms.assetid: b724595f-ef28-456e-bf0b-5df65c659d17
title: Método Database. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Export
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: faa5e2459eb0fe4ba04fd548bc478c9a0e2c85267e1df8e3d318f4a3f6a082ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745606"
---
# <a name="databaseexport-method"></a>Método Database. Export

O método **Export** do objeto [**Database**](database-object.md) copia a estrutura e os dados de uma tabela especificada para um [arquivo morto de texto](text-archive-files.md).

## <a name="syntax"></a>Sintaxe


```JScript
Database.Export(
  table,
  path,
  file
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*table* 
</dt> <dd>

Nome necessário da tabela de banco de dados. Diferenciar maiúsculas de minúsculas se usar o banco de dados do instalador.

</dd> <dt>

*path* 
</dt> <dd>

Cadeia de caracteres necessária que é o caminho para a pasta onde o arquivo de texto é colocado.

</dd> <dt>

*file* 
</dt> <dd>

Nome necessário do arquivo a ser criado. Isso não inclui a pasta, pois ela deve ser definida no objeto Path.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




