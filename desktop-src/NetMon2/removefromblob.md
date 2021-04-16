---
description: A função RemoveFromBlob exclui qualquer nível de entrada de BLOB (proprietário, categoria ou marca).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Função RemoveFromBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779598"
---
# <a name="removefromblob-function"></a>Função RemoveFromBlob

A função **RemoveFromBlob** exclui qualquer nível de entrada de BLOB (**proprietário**, **categoria** ou **marca**).

## <a name="syntax"></a>Sintaxe


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB do qual uma entrada é excluída.

</dd> <dt>

*pOwnerName* \[ no\]
</dt> <dd>

Ponteiro para o nome do **proprietário** .

</dd> <dt>

*pCategoryName* \[ no\]
</dt> <dd>

Ponteiro para o nome da **categoria** . Um valor de parâmetro **nulo** indica que o chamador está tentando excluir as informações de **proprietário** fornecidas e todas as suas entradas filhas. Observe que, se o valor do parâmetro *pCategoryName* for **NULL**, o parâmetro *pTagName* também deverá ser **nulo**.

</dd> <dt>

*pTagName* \[ no\]
</dt> <dd>

Ponteiro para o nome da **marca** . Um valor **nulo** de _pTagName_ indica que o chamador está tentando excluir a **categoria** determinada e todas as suas entradas filhas. Se o valor do parâmetro não for **nulo**, o chamador solicitará que apenas as entradas de **marca** especificadas sejam excluídas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




