---
description: A função CreateNPPInterface usa o BLOB retornado do localizador para criar um NPP que o aplicativo pode usar.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Função CreateNPPInterface (Netmon. h)
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
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922008"
---
# <a name="createnppinterface-function"></a>Função CreateNPPInterface

A função **CreateNPPInterface** usa o blob retornado do localizador para criar um NPP que o aplicativo pode usar.

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

*hBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB retornado do localizador.

</dd> <dt>

*IID* \[ em\]
</dt> <dd>

Identificador da interface que você chama do NPP (**IRTC** ou **IDelaydC**, por exemplo).

</dd> <dt>

*ppvObject* \[ fora\]
</dt> <dd>

Ponteiro para o ponteiro retornado para a interface solicitada.

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



 

 




