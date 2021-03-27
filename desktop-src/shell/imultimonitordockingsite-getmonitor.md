---
description: Obtém o monitor padrão atual.
title: 'Método IMultiMonitorDockingSite:: getmonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 1260da5ee4404a7ec4597a57e7e3836d6f133426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989049"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>Método IMultiMonitorDockingSite:: getmonitor

Obtém o monitor padrão atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*punkSrc* \[ no\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Um ponteiro para o objeto que implementa a interface [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para a qual o monitor está sendo solicitado.

</dd> <dt>

*phMon* \[ fora\]
</dt> <dd>

Tipo: **HMONITOR \** _

Quando a função retorna, contém um ponteiro para a alça do monitor padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                   |



 

 
