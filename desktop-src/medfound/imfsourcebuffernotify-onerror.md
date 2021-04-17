---
description: Usado para indicar que ocorreu um erro com o buffer de origem.
ms.assetid: a7187b7a-0090-4380-82bb-a7f72d54232e
title: 'Método IMFSourceBufferNotify:: OnError'
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
ms.openlocfilehash: 8b5f48c3517eb62b0a70acb9cbb28a5ecf7c90cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782548"
---
# <a name="imfsourcebuffernotifyonerror-method"></a>Método IMFSourceBufferNotify:: OnError

Usado para indicar que ocorreu um erro com o buffer de origem.

## <a name="syntax"></a>Sintaxe


```C++
void OnError(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HR* \[ no\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFSourceBufferNotify**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify)
</dt> </dl>

 

 




