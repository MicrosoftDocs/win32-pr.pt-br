---
description: o método Conexão do objeto de mesclagem conecta um módulo a um recurso adicional. O módulo já deve ter sido mesclado no banco de dados ou será mesclado no banco de dados. O recurso deve existir antes de chamar essa função.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Mescle. método de Conexão (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c28aafaac9f8224ea4f622b2e63f81d9dc458d72e98c6e22c348087794e9e7a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926666"
---
# <a name="mergeconnect-method"></a>Mescle. método de Conexão

o método **Conexão** do objeto de [**mesclagem**](merge-object.md) conecta um módulo a um recurso adicional. O módulo já deve ter sido mesclado no banco de dados ou será mesclado no banco de dados. O recurso deve existir antes de chamar essa função.

As alterações feitas no banco de dados não são salvas no disco, a menos que o método [**CloseDatabase**](merge-closedatabase.md) seja chamado com *BCommit* definido como **true**.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recurso* 
</dt> <dd>

O nome de um recurso já existente no banco de dados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os erros podem ser recuperados por meio da propriedade [**Errors**](merge-errors.md) . Erros e mensagens informativas são postados no arquivo de log atual.

### <a name="c"></a>C++

consulte [**Conexão**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
