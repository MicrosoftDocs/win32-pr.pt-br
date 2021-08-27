---
description: O método GenerateTransform do objeto Database cria uma transformação que, quando aplicada ao banco de dados de objeto, resulta no banco de dados de referência. A transformação é armazenada no objeto de armazenamento.
ms.assetid: 51cd70a0-6eda-4ca6-b468-9cb36ad942f8
title: Método Database.GenerateTransform
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
ms.openlocfilehash: 5c07e7483a43ea4f69eac473c76747447932fba57e53e22f79fa0663d4babc86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129646"
---
# <a name="databasegeneratetransform-method"></a>Método Database.GenerateTransform

O **método GenerateTransform** do objeto [**Database**](database-object.md) cria uma [*transformação*](t-gly.md) que, quando aplicada ao banco de dados de objeto, resulta no banco de dados de referência. A transformação é armazenada no objeto de armazenamento.

Se a transformação deve ser aplicada durante uma instalação, você deve usar o método [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) para preencher o fluxo de informações de resumo.

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Uma transformação pode adicionar colunas de chave não primária ao final de uma tabela. Não é possível criar uma transformação que adiciona colunas de chave primária a uma tabela. Não é possível criar uma transformação que altera a ordem, os nomes ou as definições das colunas.

Esse método retorna um valor booliana. Ele retornará TRUE se uma transformação for gerada. Ele retornará FALSE se uma transformação não for gerada porque não há diferenças entre os dois bancos de dados. Se o método falhar, ele gerará um erro.

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

[Transformações de banco de dados](database-transforms.md)
</dt> </dl>

 

 




