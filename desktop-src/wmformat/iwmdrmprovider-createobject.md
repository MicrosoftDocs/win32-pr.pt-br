---
title: Método CreateObject IWMDRMProvider (Wmdrmsdk.h)
description: O método CreateObject recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Formato de mídia do windows do método CreateObject
- Formato de mídia do windows do método CreateObject, interface IWMDRMProvider
- Formato de mídia da interface IWMDRMProvider, método CreateObject
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50341e33092b33b19ec3f41d968e0a1b7bc883ae959b200f6c7062e4c69996b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700772"
---
# <a name="iwmdrmprovidercreateobject-method"></a>Método IWMDRMProvider::CreateObject

O **método CreateObject** recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ Em\]
</dt> <dd>

Identificador da interface a ser criada. De definido como um dos valores a seguir.

-   IID \_ IWMDRMLicenseManagement
-   IID \_ IWMDRMLicenseQuery
-   IID \_ IWMDRMNetReceiver
-   IID \_ IWMDRMNetTransmitter
-   IID \_ IWMDRMSecurity

</dd> <dt>

*ppvObject* \[ out\]
</dt> <dd>

Endereço de um ponteiro que recebe o endereço da interface solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMProvider Interface**](iwmdrmprovider.md)
</dt> <dt>

[**IWMDRMLicenseManagement Interface**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**IWMDRMLicenseQuery Interface**](iwmdrmlicensequery.md)
</dt> <dt>

[**IWMDRMNetReceiver Interface**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetTransmitter Interface**](iwmdrmnettransmitter.md)
</dt> <dt>

[**IWMDRMSecurity Interface**](iwmdrmsecurity.md)
</dt> </dl>

 

 





