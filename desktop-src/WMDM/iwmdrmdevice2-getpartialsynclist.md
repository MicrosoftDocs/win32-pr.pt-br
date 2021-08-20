---
title: Método GetPartialSyncList IWMDRMDevice2
description: O método GetPartialSyncList obtém uma lista de sincronização parcial.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Método GetPartialSyncList windows Media Gerenciador de Dispositivos
- Método GetPartialSyncList windows Media Gerenciador de Dispositivos , interface IWMDRMDevice2
- Interface IWMDRMDevice2 windows Media Gerenciador de Dispositivos , método GetPartialSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0bcff91d41ce77003219336431433ee511ff144dfcb8be7880526994689a929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055654"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>Método IWMDRMDevice2::GetPartialSyncList

O **método GetPartialSyncList** obtém uma lista de sincronização parcial.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
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

*dwStartingIndex* \[ Em\]
</dt> <dd>

Posição inicial para indexação.

</dd> <dt>

*cItems* \[ Em\]
</dt> <dd>

Contagem de itens a serem indexados.

</dd> <dt>

*ppbSyncList* \[ out\]
</dt> <dd>

Lista de sincronização de licença recuperada.

</dd> <dt>

*pcbSyncList* \[ out\]
</dt> <dd>

Tamanho da lista de sincronização de licenças, em bytes.

</dd> <dt>

*pdwNextStartingIndex* \[ out\]
</dt> <dd>

Próxima posição inicial para indexação.

</dd> <dt>

*pcItemsProcessed* \[ out\]
</dt> <dd>

Contagem de itens que estão sendo processados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Todos os métodos de interface no Windows Media Gerenciador de Dispositivos podem retornar qualquer uma das seguintes classes de códigos de erro:

-   Códigos de erro COM padrão
-   Windows códigos de erro convertidos em valores HRESULT
-   Windows Códigos Gerenciador de Dispositivos de erro de mídia

Para uma lista extensiva de possíveis códigos de erro, consulte [Códigos de erro](error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP.idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMDevice::GetSyncList**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**IWMDRMDevice2 Interface**](iwmdrmdevice2.md)
</dt> </dl>

 

 





