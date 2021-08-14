---
description: O método Execute do objeto View usa o token de ponto de interrogação para representar parâmetros em uma instrução SQL dados. Para obter mais informações, consulte Sintaxe SQL dados. Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemétodo cute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Execute
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9bfd1120382ea06f6046f4435d0143024422ff6345959099326ab4a5428d26d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804024"
---
# <a name="viewexecute-method"></a>View.Exemétodo cute

O **método** Execute do objeto [**View**](view-object.md) usa o token de ponto de interrogação para representar parâmetros em uma instrução SQL dados. Para obter mais informações, consulte [Sintaxe SQL .](sql-syntax.md) Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.

## <a name="syntax"></a>Sintaxe


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Registro* 
</dt> <dd>

Objetos [**de**](record-object.md) registro opcionais que contêm os valores que substituem os tokens de parâmetro (?) na SQL consulta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado antes de qualquer chamada para o [**método Fetch.**](view-fetch.md)

Se a SQL especifica valores com marcadores de parâmetro (?), será necessário fornecer um registro que contenha todos os valores de substituição, que devem estar na mesma ordem e no mesmo tipo de dados que os marcadores de parâmetro. Quando esse método é usado com consultas INSERT e UPDATE, os tokens de ponto de interrogação devem preceder todos os valores não parametrizados.

Por exemplo, essas consultas são válidas:

UPDATE {table-list} SET {column}= ? , {column}= {constant}

INSERT INTO {table} ({column-list}) VALUES (?, {constant-list})

No entanto, essas consultas são inválidas:

UPDATE {table-list} SET {column}= {constant}, {column}=?

INSERT INTO {table} ({column-list}) VALUES ({constant-list}, ? )

Se o método falhar, você poderá obter informações de erro estendidas usando o [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView é definido como \_ 000C109C-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



 

 




