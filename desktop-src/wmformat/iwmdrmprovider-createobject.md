---
title: Método CreateObject IWMDRMProvider (wmdrmsdk. h)
description: O método CreateObject recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Método CreateObject Windows Media Format
- Método CreateObject Windows Media Format, interface IWMDRMProvider
- Formato de mídia do Windows da interface IWMDRMProvider, método CreateObject
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
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747868"
---
# <a name="iwmdrmprovidercreateobject-method"></a>Método IWMDRMProvider:: CreateObject

O método **CreateObject** recupera um ponteiro para uma interface especificada, criando o objeto de implementação, se necessário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*riid* \[ no\]
</dt> <dd>

Identificador da interface a ser criada. Defina como um dos valores a seguir.

-   IWMDRMLicenseManagement de IID \_
-   IWMDRMLicenseQuery de IID \_
-   IWMDRMNetReceiver de IID \_
-   IWMDRMNetTransmitter de IID \_
-   IWMDRMSecurity de IID \_

</dd> <dt>

*ppvObject* \[ fora\]
</dt> <dd>

Endereço de um ponteiro que recebe o endereço da interface solicitada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMProvider**](iwmdrmprovider.md)
</dt> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





