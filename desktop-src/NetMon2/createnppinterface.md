---
description: A função CreateNPPInterface usa o BLOB retornado do finder para criar um NPP que o aplicativo pode usar.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Função CreateNPPInterface (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 03c2bb7fae0f68e6d38016df353266cfc9ec11757eeb98f6a5e41ab4316e63c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744536"
---
# <a name="createnppinterface-function"></a>Função CreateNPPInterface

A **função CreateNPPInterface** usa o BLOB retornado do finder para criar um NPP que o aplicativo pode usar.

## <a name="syntax"></a>Sintaxe


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hBlob* \[ Em\]
</dt> <dd>

Lidar com o BLOB retornado do finder.

</dd> <dt>

*iid* \[ em\]
</dt> <dd>

Identificador da interface que você chama do NPP (**IRTC** ou **IDelaydC**, por exemplo).

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Ponteiro para o ponteiro retornado para a interface solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NMERR \_ SUCCESS.

Se a função não for bem-sucedida, o valor de retorno será um valor NMERR que descreve o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




