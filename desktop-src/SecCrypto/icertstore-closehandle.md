---
description: Fecha um identificador HCERTSTORE adquirido por meio da Propriedade StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Método ICertStore:: CloseHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754599"
---
# <a name="icertstoreclosehandle-method"></a>Método ICertStore:: CloseHandle

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

O método **CloseHandle** fecha um identificador HCERTSTORE adquirido por meio da propriedade [**StoreHandle**](icertstore-storehandle.md) .

## <a name="syntax"></a>Sintaxe


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HCERTSTORE* \[ no\]
</dt> <dd>

O identificador HCERTSTORE a ser fechado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um **HRESULT**. Um valor de **S \_ OK** indica êxito. Qualquer outro valor indica que a operação falhou.

## <a name="remarks"></a>Comentários

Esse método não libera o identificador HCERTSTORE contido em um objeto [**Store**](store.md) . Ele deve ser usado apenas para liberar um identificador HCERTSTORE adquirido por meio da propriedade [**StoreHandle**](icertstore-storehandle.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




