---
description: A função MergeBlob copia Todas as entradas do BLOB de origem em um BLOB de destino.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: Função MergeBlob (Netmon. h)
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
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921001"
---
# <a name="mergeblob-function"></a>Função MergeBlob

A função **MergeBlob** copia Todas as entradas do blob de origem em um blob de destino.

## <a name="syntax"></a>Sintaxe


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDstBlob* \[ entrada, saída\]
</dt> <dd>

Identificador para o BLOB de destino. Na entrada, esse BLOB contém suas informações originais. Na saída, esse BLOB contém suas informações originais e todas as informações do BLOB de origem.

</dd> <dt>

*hSrcBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB de origem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="remarks"></a>Comentários

As entradas comuns aos arquivos de origem e de destino serão substituídas pelos dados do BLOB de origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




