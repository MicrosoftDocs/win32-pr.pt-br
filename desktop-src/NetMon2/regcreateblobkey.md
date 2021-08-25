---
description: A função RegCreateBlobKey armazena um BLOB na chave do Registro determinada.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Função RegCreateBlobKey (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 3267fd0ba5e6fe56b99b5d465f69718fe5509a7ead58acf1d8dafb642397af5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889646"
---
# <a name="regcreateblobkey-function"></a>Função RegCreateBlobKey

A **função RegCreateBlobKey** armazena um BLOB na chave do Registro determinada.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hkey* \[ out\]
</dt> <dd>

Lidar com a chave do Registro em que o BLOB será armazenado.

</dd> <dt>

*szBlobName* \[ Em\]
</dt> <dd>

Nome (aplicativo definido) que representa o BLOB no Registro.

</dd> <dt>

*hBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB salvo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




