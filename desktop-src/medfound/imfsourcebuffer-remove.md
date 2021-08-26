---
description: Remove os segmentos de mídia definidos pelo intervalo de tempo especificado do IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: Método IMFSourceBuffer::Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: af9aed011a1a4b53733d70646fc14b21e7c97f9d193a60e679f5f5f532679e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941906"
---
# <a name="imfsourcebufferremove-method"></a>Método IMFSourceBuffer::Remove

Remove os segmentos de mídia definidos pelo intervalo de tempo especificado do [**IMFSourceBuffer.**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iniciar* \[ Em\]
</dt> <dd>

O início do intervalo de tempo.

</dd> <dt>

*end* \[ Em\]
</dt> <dd>

O final do intervalo de tempo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                      |
| Idl<br/>                      | <dl> <dt>Mfmediaengine.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




