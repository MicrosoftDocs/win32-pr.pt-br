---
description: Define a duração da origem de mídia em unidades de 100 a nanossegundos.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Método IMFMediaSourceExtension:: setduration'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: caad66946514eec91d1cac1dc9745b0d07d1546e32c9548297f01e76b921c46f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061206"
---
# <a name="imfmediasourceextensionsetduration-method"></a>Método IMFMediaSourceExtension:: setduration

Define a duração da origem de mídia em unidades de 100 a nanossegundos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*duração* \[ no\]
</dt> <dd>

A duração da origem de mídia em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




