---
description: A função DllGetMonitorObject deve ser implementada pelo monitor. O MCSVC chama essa função para criar uma instância do monitor.
ms.assetid: 2c39f752-264c-4ab9-8710-a0d660c4772f
title: Função de retorno de chamada DllGetMonitorObject (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllGetMonitorObject
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 723c085fe86e8c24ebc13d83c760e5bfdd08eab2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836991"
---
# <a name="dllgetmonitorobject-callback-function"></a>Função de retorno de chamada DllGetMonitorObject

A função **DllGetMonitorObject** deve ser implementada pelo monitor. O MCSVC chama essa função para criar uma instância do monitor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DllGetMonitorObject(
  _In_  REFIID riid,
  _Out_ LPVOID *ppObj
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ no\]
</dt> <dd>

UUID de monitores, mostrado abaixo, conforme definido no arquivo de cabeçalho IMonitor. h. Se um UUID inválido for fornecido, a função falhará e o monitor deverá retornar E \_ nointerface.

``` syntax
IID_IMonitor
```

</dd> <dt>

*ppObj* \[ fora\]
</dt> <dd>

Ponteiro para um ponteiro que recebe a interface solicitada em *riid*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).

Se a função não for bem-sucedida, o valor de retorno será um código de falha. Quando um código de falha é retornado, o MCSVC não cria o objeto monitor e o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) não é chamado no ponteiro de interface.

## <a name="remarks"></a>Comentários

A função **DllGetMonitorObject** é chamada cada vez que o MCSVC tenta criar uma instância do monitor. Essa função possui intencionalmente uma forte semelhança com a função [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) mais comum. A principal diferença é que um CLSID não é passado para **DllGetMonitorObject**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

