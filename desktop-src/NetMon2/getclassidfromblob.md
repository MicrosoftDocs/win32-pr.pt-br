---
description: A função GetClassIDFromBlob recupera um valor de identificador de classe nomeado de um BLOB.
ms.assetid: fef29a42-ccd3-4655-958c-d150e5bcd0d7
title: Função GetClassIDFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetClassIDFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70122422c47a986058322ca8d17082093e02a4b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089968"
---
# <a name="getclassidfromblob-function"></a>Função GetClassIDFromBlob

A função **GetClassIDFromBlob** recupera um valor de identificador de classe nomeado de um blob.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetClassIDFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       CLSID *pClsID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para um BLOB.

</dd> <dt>

*pOwnerName* \[ no\]
</dt> <dd>

Ponteiro para o nome do proprietário do BLOB.

</dd> <dt>

*pCategoryName* \[ no\]
</dt> <dd>

Ponteiro para o nome da categoria de BLOB.

</dd> <dt>

*pTagName* \[ no\]
</dt> <dd>

Ponteiro para o nome da marca de BLOB.

</dd> <dt>

*pCLSID* \[ fora\]
</dt> <dd>

Ponteiro para o identificador de classe de BLOB.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




