---
title: Método IWMDRMDevice2 GetPartialSyncList
description: O método GetPartialSyncList Obtém uma lista de sincronização parcial.
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- Método GetPartialSyncList Windows Media Gerenciador de Dispositivos
- Método GetPartialSyncList Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gerenciador de Dispositivos, método GetPartialSyncList
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
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811362"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a>Método IWMDRMDevice2:: GetPartialSyncList

O método **GetPartialSyncList** Obtém uma lista de sincronização parcial.

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

*cMinCountThreshold* \[ no\]
</dt> <dd>

Limite de contagem mínima.

</dd> <dt>

*cMinHoursThreshold* \[ no\]
</dt> <dd>

Limite mínimo de horas.

</dd> <dt>

*dwStartingIndex* \[ no\]
</dt> <dd>

Posição inicial para indexação.

</dd> <dt>

*cItems* \[ no\]
</dt> <dd>

Contagem de itens a serem indexados.

</dd> <dt>

*ppbSyncList* \[ fora\]
</dt> <dd>

Lista de sincronização de licenças recuperada.

</dd> <dt>

*pcbSyncList* \[ fora\]
</dt> <dd>

Tamanho da lista de sincronização de licenças, em bytes.

</dd> <dt>

*pdwNextStartingIndex* \[ fora\]
</dt> <dd>

Próxima posição de início para indexação.

</dd> <dt>

*pcItemsProcessed* \[ fora\]
</dt> <dd>

Contagem de itens que estão sendo processados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Todos os métodos de interface no Windows Media Gerenciador de Dispositivos podem retornar qualquer uma das seguintes classes de códigos de erro:

-   Códigos de erro padrão COM
-   Códigos de erro do Windows convertidos em valores HRESULT
-   Códigos de erro do Windows Media Gerenciador de Dispositivos

Para obter uma lista extensa de possíveis códigos de erro, consulte [códigos de erro](error-codes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMDevice:: getsynclist**](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[**Interface IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





