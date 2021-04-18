---
title: Método getsincronizalist do IWMDRMDevice
description: O método getsincronizarlist recupera a lista de sincronização de licenças no dispositivo. A sincronização de licenças permite que o computador host transfira licenças atualizadas para um dispositivo de acordo com os critérios especificados.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Método getsincronizarlist Windows Media Gerenciador de Dispositivos
- Método getsincronizarlist Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gerenciador de Dispositivos, método getsincronizarlist
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
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784930"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>Método IWMDRMDevice:: getsynclist

O método **Getsincronizarlist** recupera a lista de sincronização de licenças no dispositivo. A sincronização de licenças permite que o computador host transfira licenças atualizadas para um dispositivo de acordo com os critérios especificados.

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

*cMinCountThreshold* \[ no\]
</dt> <dd>

Limite de contagem mínima.

</dd> <dt>

*cMinHoursThreshold* \[ no\]
</dt> <dd>

Limite mínimo de horas.

</dd> <dt>

*ppbSyncList* \[ fora\]
</dt> <dd>

Lista de sincronização de licenças recuperada.

</dd> <dt>

*pcbSyncList* \[ fora\]
</dt> <dd>

Tamanho da lista de sincronização de licenças, em bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





