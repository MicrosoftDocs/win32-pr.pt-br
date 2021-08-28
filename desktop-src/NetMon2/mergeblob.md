---
description: A função MergeBlob copia todas as entradas do BLOB de origem em um BLOB de destino.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Função MergeBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5c0ce93235a0c46286b9bfbef0773a5584f3db774aa52991b4e0eaa9dd38352f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677186"
---
# <a name="mergeblob-function"></a>Função MergeBlob

A **função MergeBlob** copia todas as entradas do BLOB de origem em um BLOB de destino.

## <a name="syntax"></a>Sintaxe


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDstBlob* \[ in, out\]
</dt> <dd>

Lidar com o BLOB de destino. Na entrada, esse BLOB contém suas informações originais. Na saída, esse BLOB contém suas informações originais, além de todas as informações do BLOB de origem.

</dd> <dt>

*hSrcBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB de origem.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="remarks"></a>Comentários

Entradas comuns aos arquivos de origem e de destino serão substituídas por dados do BLOB de origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




