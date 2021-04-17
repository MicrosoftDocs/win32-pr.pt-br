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
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105763974"
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

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                      |
| INSERI<br/>                      | <dl> <dt>Mfmediaengine. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




