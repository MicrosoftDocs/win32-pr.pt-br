---
description: Obtém o objeto de chaves de mídia associado ao mecanismo de mídia ou nulo se não houver um objeto de chaves de mídia.
ms.assetid: e6556a02-445d-4436-80de-e4156d6a3d63
title: 'Método IMFMediaEngineEME:: get_Keys'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaEngineEME.get_Keys
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: dcb06352065b28739a616a9f2216c20eedebb913
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105798233"
---
# <a name="imfmediaengineemeget_keys-method"></a>Método IMFMediaEngineEME:: obter \_ chaves

Obtém o objeto de chaves de mídia associado ao mecanismo de mídia ou **nulo** se não houver um objeto de chaves de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Keys(
   IMFMediaKeys **keys
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*novas* 
</dt> <dd>

O objeto de chaves de mídia associado ao mecanismo de mídia ou **nulo** se não houver um objeto de chaves de mídia.

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

[**IMFMediaEngineEME**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme)
</dt> </dl>

 

 




