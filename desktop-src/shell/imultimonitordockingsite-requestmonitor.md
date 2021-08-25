---
description: Verifica se o monitor está ativo e disponível.
title: Método IMultiMonitorDockingSite::RequestMonitor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 9e5eeb2b99455d81bae36f1c5f26ed38126122bb58a5b8964a47cfb205f71ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942896"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>Método IMultiMonitorDockingSite::RequestMonitor

Verifica se o monitor está ativo e disponível.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*quedas de dados* \[ Em\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Um ponteiro para o objeto que implementa a interface [**IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)

</dd> <dt>

*phMon* \[ Em\]
</dt> <dd>

Tipo: **HMONITOR \***

Um ponteiro para o alça do monitor padrão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                   |



 

 
