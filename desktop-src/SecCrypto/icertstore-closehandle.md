---
description: Fecha um alça HCERTSTORE adquirido por meio da propriedade StoreHandle.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: Método ICertStore::CloseHandle
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
ms.openlocfilehash: 3d6f1b0b44cd0fdc71f8f3d37fa9bd8290c5d606eea1f97f5bf6644f9ce8e2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005654"
---
# <a name="icertstoreclosehandle-method"></a>Método ICertStore::CloseHandle

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.\]

O **método CloseHandle** fecha um alça HCERTSTORE adquirido por meio da [**propriedade StoreHandle.**](icertstore-storehandle.md)

## <a name="syntax"></a>Sintaxe


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hCertStore* \[ Em\]
</dt> <dd>

O alça HCERTSTORE a ser fechado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **um HRESULT.** Um valor de **S \_ OK** indica êxito. Qualquer outro valor indica que a operação falhou.

## <a name="remarks"></a>Comentários

Esse método não libera o identificador HCERTSTORE contido em um [**objeto**](store.md) Store. Ele deve ser usado apenas para liberar um alça HCERTSTORE adquirido por meio da [**propriedade StoreHandle.**](icertstore-storehandle.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ICertStore**](icertstore.md)
</dt> </dl>

 

 




