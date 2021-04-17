---
description: O método Execute do objeto View usa o token de ponto de interrogação para representar parâmetros em uma instrução SQL. Para obter mais informações, consulte sintaxe SQL. Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.
ms.assetid: 4f2b2cb8-8f59-4e4a-ba09-6cb092ef81d6
title: View.Exemétodo graciosos
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
ms.openlocfilehash: 939d1aa5216085d701fb728ad5e5e9aa9e07e702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748752"
---
# <a name="viewexecute-method"></a>View.Exemétodo graciosos

O método **Execute** do objeto [**View**](view-object.md) usa o token de ponto de interrogação para representar parâmetros em uma instrução SQL. Para obter mais informações, consulte [sintaxe SQL](sql-syntax.md). Os valores desses parâmetros são passados como os campos correspondentes de um registro de parâmetro.

## <a name="syntax"></a>Sintaxe


```JScript
View.Execute(
  record
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*gravável* 
</dt> <dd>

Objetos de [**registro**](record-object.md) opcionais que contêm os valores que substituem os tokens de parâmetro (?) na consulta SQL.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método deve ser chamado antes de qualquer chamada para o método [**Fetch**](view-fetch.md) .

Se a consulta SQL especificar valores com marcadores de parâmetro (?), um registro deve ser fornecido contendo todos os valores de substituição, que devem estar na mesma ordem e no mesmo tipo de dados que os marcadores de parâmetro. Quando esse método é usado com consultas INSERT e UPDATE, os tokens de ponto de interrogação devem preceder todos os valores não parametrizados.

Por exemplo, essas consultas são válidas:

ATUALIZAR {Table-List} conjunto {Column} =? , {coluna} = {constante}

INSERT em {Table} ({Column-List}) valores (?, {Constant-List})

No entanto, essas consultas são inválidas:

ATUALIZAR {Table-List} conjunto {Column} = {constante}, {Column} =?

INSERIR em valores de {Table} ({Column-List}) ({lista de constantes},? )

Se o método falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView é definido como 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




