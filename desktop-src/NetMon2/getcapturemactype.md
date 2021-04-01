---
description: A função GetCaptureMacType retorna o tipo de MAC de uma determinada captura.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Função GetCaptureMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646798"
---
# <a name="getcapturemactype-function"></a>Função GetCaptureMacType

A função **GetCaptureMacType** retorna o tipo de Mac de uma determinada captura.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCapture* \[ no\]
</dt> <dd>

Identificador para a captura. Para obter informações sobre como obter o identificador de captura, consulte a seção comentários neste tópico de **GetCaptureMacType** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um dos tipos de MAC a seguir.

-   tipo de MAC \_ \_ desconhecido
-   tipo de MAC \_ \_ Ethernet
-   tipo de MAC \_ \_ TOKENRING
-   tipo de MAC \_ \_ FDDI

Se a função não for bem-sucedida, o valor de retorno será um código de erro.



| Código de retorno                                                                                              | Descrição                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>**tipo de NMERR de \_ Mac \_ \_ desconhecido**</dt> </dl> | Monitor de Rede não pôde encontrar um tipo de MAC conhecido.<br/> |



 

## <a name="remarks"></a>Comentários

O identificador da captura pode ser obtido de várias maneiras, dependendo de quem faz a chamada. Para especialistas, o identificador é especificado no membro **hCapture** da estrutura [EXPERTSTARTUPINFO](expertstartupinfo.md) . Para analisadores, o identificador de captura pode ser obtido chamando a função [GetFrameCaptureHandle](getframecapturehandle.md) .

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureMacType** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




