---
description: O método OpenLog do objeto Merge abre um arquivo de log que recebe o progresso e as mensagens de erro. Se o arquivo de log já existir, o instalador acrescentará novas mensagens. Se o arquivo de log não existir, o instalador criará um arquivo de log.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Método Merge. OpenLog (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752846"
---
# <a name="mergeopenlog-method"></a>Método Merge. OpenLog

O método **OpenLog** do objeto [**Merge**](merge-object.md) abre um arquivo de log que recebe o progresso e as mensagens de erro. Se o arquivo de log já existir, o instalador acrescentará novas mensagens. Se o arquivo de log não existir, o instalador criará um arquivo de log.

## <a name="syntax"></a>Sintaxe


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Filename* 
</dt> <dd>

Nome de arquivo totalmente qualificado que aponta para um arquivo a ser aberto ou criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os clientes podem enviar suas próprias mensagens para esse arquivo de log por meio do método [**log**](merge-log.md) .

### <a name="c"></a>C++

Consulte a função [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
