---
description: A função IsRemoteNPP indica se o BLOB especificado especifica um NPP remoto.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Função IsRemoteNPP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661854"
---
# <a name="isremotenpp-function"></a>Função IsRemoteNPP

A função **IsRemoteNPP** indica se o blob especificado especifica um NPP remoto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para um BLOB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será **true**.

## <a name="remarks"></a>Comentários

Use essa função para testar se existe uma categoria remota.

Verifique se os nomes dos computadores remotos e locais são diferentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




