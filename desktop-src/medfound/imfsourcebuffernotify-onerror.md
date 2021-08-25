---
description: Usado para indicar que ocorreu um erro com o buffer de origem.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: Método IMFSourceBufferNotify::OnError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBufferNotify.OnError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 0602340011bae5af974a3441b42d62d392394b79854015acc68da0b1c2fcf538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957796"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>Método IMFSourceBufferNotify::OnError

Usado para indicar que ocorreu um erro com o buffer de origem.

## <a name="syntax"></a>Sintaxe


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hr* \[ Em\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




