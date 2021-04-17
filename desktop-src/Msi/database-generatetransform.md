---
description: O método GenerateTransform do objeto Database cria uma transformação que, quando aplicada ao banco de dados de objeto, resulta no banco de dados de referência. A transformação é armazenada no objeto de armazenamento.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Método Database. GenerateTransform
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.GenerateTransform
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5f7fca94c0765722dc2d0b21524c15265f99e7b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747773"
---
# <a name="databasegeneratetransform-method"></a>Método Database. GenerateTransform

O método **GenerateTransform** do objeto [**Database**](database-object.md) cria uma [*transformação*](t-gly.md) que, quando aplicada ao banco de dados de objeto, resulta no banco de dados de referência. A transformação é armazenada no objeto de armazenamento.

Se a transformação for ser aplicada durante uma instalação, você deverá usar o método [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) para popular o fluxo de informações de resumo.

## <a name="syntax"></a>Sintaxe


```JScript
Database.GenerateTransform(
  reference,
  storage
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*reference* 
</dt> <dd>

Banco de dados necessário que não inclui as alterações.

</dd> <dt>

*storage* 
</dt> <dd>

O nome do arquivo de transformação gerado. Isso é opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Uma transformação pode adicionar colunas de chave não primárias ao final de uma tabela. Não é possível criar uma transformação que adiciona colunas de chave primária a uma tabela. Não é possível criar uma transformação que altere a ordem, os nomes ou as definições de colunas.

Esse método retorna um valor booliano. Retornará TRUE se uma transformação for gerada. Retornará FALSE se uma transformação não for gerada porque não há diferenças entre os dois bancos de dados. Se o método falhar, ele gerará um erro.

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

[Transformações de banco de dados](database-transforms.md)
</dt> </dl>

 

 




