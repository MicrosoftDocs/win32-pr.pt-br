---
description: O método doinitialize deve ser implementado pelo monitor. O MCSVC chama esse método para obter um filtro de captura imediatamente antes de chamar o método NPPs IRTCConnect.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Método IMonitorDoInitialize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501343"
---
# <a name="imonitordoinitialize-method"></a>IMonitor: método oInitialize de:D

O método **doinitialize** deve ser implementado pelo monitor. O MCSVC chama esse método para obter um filtro de captura imediatamente antes de chamar o método [IRTC:: Connect](irtc-connect.md) do NPP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnkMonitorCtrl* \[ no\]
</dt> <dd>

Um ponteiro [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passado pelo MCSVC. Para obter uma interface de controle de monitor com suporte, o monitor deve chamar [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro.

</dd> <dt>

*hNPPBlob* \[ entrada, saída\]
</dt> <dd>

Na entrada, um identificador para um BLOB NPP.

Na saída, um BLOB NPP que contém um filtro de captura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).

Se o método não for bem-sucedido, o valor de retorno será um código de erro. Se houver erro, o MCSVC não criará o monitor ou chamará [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro de interface.

## <a name="remarks"></a>Comentários

O MCSVC chama o método **doinitialize** para executar qualquer inicialização de monitor necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

