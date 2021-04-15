---
description: Recupera o tipo de MAC da categoria NetworkInfo da seção NPP do BLOB e converte os dados de tipo em um número de tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Função GetNPPMacTypeAsNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501349"
---
# <a name="getnppmactypeasnumber-function"></a>Função GetNPPMacTypeAsNumber

A função **GetNPPMacTypeAsNumber** recupera o tipo de Mac da categoria NetworkInfo da seção NPP do blob e converte os dados de tipo em um número de tipo Mac.

## <a name="syntax"></a>Sintaxe


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Um identificador para o BLOB especificado.

</dd> <dt>

*lpMacType* \[ fora\]
</dt> <dd>

Um ponteiro para o tipo de MAC.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a marca não estiver disponível, o valor de retorno será \_ tipo de Mac \_ desconhecido.

## <a name="remarks"></a>Comentários

Essa função mapeia a marca, **NPP: NetworkInfo: MacType** para o **\_ \_ \* tipo de Mac** , conforme definido no arquivo Npptypes. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




