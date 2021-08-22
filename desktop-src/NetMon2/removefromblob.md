---
description: A função RemoveFromBlob exclui qualquer nível de entrada BLOB (Proprietário, Categoria ou Marca).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Função RemoveFromBlob (Netmon.h)
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
ms.openlocfilehash: 09c9c7f5ada320f33d38cd9e935add7e47721c554fbeed11c35a1b73248d963c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063686"
---
# <a name="removefromblob-function"></a>Função RemoveFromBlob

A **função RemoveFromBlob** exclui qualquer nível de entrada BLOB (**Proprietário,** **Categoria** ou **Marca**).

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

*hBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB do qual uma entrada é excluída.

</dd> <dt>

*pOwnerName* \[ Em\]
</dt> <dd>

Ponteiro para o **nome do** proprietário.

</dd> <dt>

*pCategoryName* \[ Em\]
</dt> <dd>

Ponteiro para o **Nome da** categoria. Um **valor de** parâmetro NULL indica que o chamador está tentando excluir as informações de **Proprietário** determinadas e todas as suas entradas filho. Observe que, se *o valor do parâmetro pCategoryName* for **NULL,** o *parâmetro pTagName* também deverá ser **NULL.**

</dd> <dt>

*pTagName* \[ Em\]
</dt> <dd>

Ponteiro para o **Nome da** marca. Um **valor null**_pTagName_ indica que o chamador está tentando excluir a **Categoria** determinada e todas as suas entradas filho. Se o valor do parâmetro não for **NULL,** o chamador pedirá que apenas as entradas de **Marca** especificadas sejam excluídas.

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



 

 




