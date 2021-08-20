---
description: O método OpenLog do objeto Merge abre um arquivo de log que recebe mensagens de progresso e erro. Se o arquivo de log já existir, o instalador anexa novas mensagens. Se o arquivo de log não existir, o instalador criará um arquivo de log.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Método Merge.OpenLog (Mergemod.h)
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
ms.openlocfilehash: c69ecf0c7a4a629b2f6ebc303d34619ae9d4cc396c79e09ea37e2d4b27db5c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804608"
---
# <a name="mergeopenlog-method"></a>Método Merge.OpenLog

O **método OpenLog** do objeto [**Merge**](merge-object.md) abre um arquivo de log que recebe mensagens de progresso e erro. Se o arquivo de log já existir, o instalador anexa novas mensagens. Se o arquivo de log não existir, o instalador criará um arquivo de log.

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

Nome de arquivo totalmente qualificado apontando para um arquivo a ser aberto ou criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os clientes podem enviar suas próprias mensagens para esse arquivo de log por meio do [**método Log.**](merge-log.md)

### <a name="c"></a>C++

Consulte [**Função OpenLog.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
