---
description: O método DoInitialize deve ser implementado pelo monitor. O MCSVC chama esse método para obter um filtro de captura imediatamente antes de chamar o método NPPs IRTCConnect.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Método IMonitorDoInitialize (Netmon.h)
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
ms.openlocfilehash: 013a1604c1cbc709f35ac23378bab008d6c67f9053c171190b20669106303f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779176"
---
# <a name="imonitordoinitialize-method"></a>Método IMonitor::D oInitialize

O **método DoInitialize** deve ser implementado pelo monitor. O MCSVC chama esse método para obter um filtro de captura imediatamente antes de chamar o método [IRTC::Conexão](irtc-connect.md) NPP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnkMonitorCtrl* \[ Em\]
</dt> <dd>

Um [ponteiro IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passado pelo MCSVC. Para obter uma interface de controle de monitor com suporte, o monitor deve chamar [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro.

</dd> <dt>

*hNPPBlob* \[ in, out\]
</dt> <dd>

Na entrada, um alça para um BLOB NPP.

Na saída, um BLOB NPP que contém um filtro de captura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será S \_ OK (que é o mesmo que NOERROR).

Se o método não for bem-sucedido, o valor de retorno será um código de erro. Em caso de erro, o MCSVC não criará o monitor nem chamará [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro da interface.

## <a name="remarks"></a>Comentários

O MCSVC chama o **método DoInitialize** para executar qualquer inicialização de monitor necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

