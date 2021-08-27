---
title: Método IWMDRMLicenseManagement MonitorLicenseAcquisition (wmdrmsdk. h)
description: O método MonitorLicenseAcquisition inicia o monitoramento para um processo de aquisição de licença.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Formato de mídia do Windows do método MonitorLicenseAcquisition
- Método MonitorLicenseAcquisition Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método MonitorLicenseAcquisition
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7ab3188425decca614ae104989fdc2f07930ac0de463e492be630a3fb54556e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027574"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a>Método IWMDRMLicenseManagement:: MonitorLicenseAcquisition

O método **MonitorLicenseAcquisition** inicia o monitoramento para um processo de aquisição de licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrKID* \[ no\]
</dt> <dd>

ID da chave (KID) da licença que está sendo adquirida.

</dd> <dt>

*bstrHeader* \[ no\]
</dt> <dd>

Cabeçalho de conteúdo que foi usado na chamada para o método [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) .

</dd> <dt>

*bstrActions* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém as ações solicitadas na chamada para o método **AcquireLicense** .

</dd> <dt>

*ppunkCancelationCookie* \[ fora\]
</dt> <dd>

Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona. Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





