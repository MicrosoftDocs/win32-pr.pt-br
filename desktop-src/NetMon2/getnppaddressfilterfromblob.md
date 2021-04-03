---
description: A função GetNPPAddressFilterFromBlob preenche o filtro de endereço fornecido com as informações armazenadas no BLOB.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: Função GetNPPAddressFilterFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922618"
---
# <a name="getnppaddressfilterfromblob-function"></a>Função GetNPPAddressFilterFromBlob

A função **GetNPPAddressFilterFromBlob** preenche o filtro de endereço fornecido com as informações armazenadas no BLOB.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para um BLOB.

</dd> <dt>

*pAddressTable* \[ entrada, saída\]
</dt> <dd>

Ponteiro para a tabela de endereços alocada pelo usuário.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro que especifica onde ocorreu o erro (se houver) no BLOB original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.

## <a name="remarks"></a>Comentários

As informações de endereço são armazenadas na seção de **configuração** da categoria blob NPP do **proprietário** .

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

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




