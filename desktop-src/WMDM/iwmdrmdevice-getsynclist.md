---
title: Método GetSyncList de IWMDRMDevice
description: O método GetSyncList recupera a lista de sincronização de licenças no dispositivo. A sincronização de licenças permite que o computador host transfira licenças atualizadas para um dispositivo de acordo com os critérios especificados.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Janelas de mídia do método GetSyncList Gerenciador de Dispositivos
- Método GetSyncList windows Media Gerenciador de Dispositivos , interface IWMDRMDevice
- Interface IWMDRMDevice windows Media Gerenciador de Dispositivos , método GetSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6424daa720f9987228175a7698a29f7056e5d4b4d174d1d635bbcd1ed7f8382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619576"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>Método IWMDRMDevice::GetSyncList

O **método GetSyncList** recupera a lista de sincronização de licenças no dispositivo. A sincronização de licenças permite que o computador host transfira licenças atualizadas para um dispositivo de acordo com os critérios especificados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cMinCountThreshold* \[ Em\]
</dt> <dd>

Limite mínimo de contagem.

</dd> <dt>

*cMinHoursThreshold* \[ Em\]
</dt> <dd>

Limite mínimo de horas.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Lista de sincronização de licença recuperada.

</dd> <dt>

*pcbSyncList* \[ out\]
</dt> <dd>

Tamanho da lista de sincronização de licenças, em bytes.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMDevice Interface**](iwmdrmdevice.md)
</dt> </dl>

 

 





