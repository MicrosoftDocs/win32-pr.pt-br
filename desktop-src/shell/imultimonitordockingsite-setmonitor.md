---
description: Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.
title: 'Método IMultiMonitorDockingSite:: setmonitor'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989113"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>Método IMultiMonitorDockingSite:: setmonitor

Altera qual monitor é usado para barras de ferramentas encaixadas em um sistema de vários monitores.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*punkSrc* \[ no\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Um ponteiro para o objeto que implementa a interface [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para a qual o monitor está sendo alterado.

</dd> <dt>

*hMonNew* \[ no\]
</dt> <dd>

Tipo: **HMONITOR**

Um identificador para o monitor que substitui o monitor padrão existente.

</dd> <dt>

*phMonOld* \[ fora\]
</dt> <dd>

Tipo: **HMONITOR \** _

Quando essa função retorna, contém um ponteiro para a alça do monitor padrão anterior.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: _ *HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                   |



 

 
