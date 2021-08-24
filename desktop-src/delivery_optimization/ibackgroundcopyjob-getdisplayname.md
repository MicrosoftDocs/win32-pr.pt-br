---
title: Método GetDisplayName de método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera o nome de exibição para o trabalho. Normalmente, você usa o nome de exibição para identificar o trabalho em uma interface do usuário.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- Método GetDisplayName
- Método GetDisplayName, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, Método GetDisplayName
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1a50d2bdc1c492725b79368774f07755c7b629d73209a7d53f865cc738eb7025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755536"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a>Método método ibackgroundcopyjob:: GetDisplayName

Recupera o nome de exibição para o trabalho. Normalmente, você usa o nome de exibição para identificar o trabalho em uma interface do usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDisplayName* \[ fora\]
</dt> <dd>

Cadeia de caracteres terminada em nulo que contém o nome para exibição que identifica o trabalho. Mais de um trabalho pode ter o mesmo nome de exibição. Chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppDisplayName* quando terminar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna os valores **HRESULT** a seguir, bem como outros.



| Código de retorno                                                                                  | Descrição                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | O nome para exibição foi recuperado com êxito.<br/>          |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | O parâmetro *ppDisplayName* não pode ser **nulo**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

