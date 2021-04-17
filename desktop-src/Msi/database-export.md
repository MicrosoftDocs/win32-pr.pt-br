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
ms.openlocfilehash: e9fbd5be6523db54be5f71b806bf278861f14709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748780"
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



 

 




