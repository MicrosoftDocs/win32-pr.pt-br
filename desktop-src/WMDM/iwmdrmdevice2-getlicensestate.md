---
title: Método getlicenciadostate IWMDRMDevice2
description: O método getlicenciadostate Obtém o estado da licença.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Método getlicenciadostate Windows Media Gerenciador de Dispositivos
- Método getlicenciadostate Windows Media Gerenciador de Dispositivos, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gerenciador de Dispositivos, método getlicenciadostate
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759761"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>Método IWMDRMDevice2:: getlicenciadostate

O método **Getlicenciadostate** Obtém o estado da licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbStateQueryData* \[ no\]
</dt> <dd>

Ponteiro para os dados consultados do estado da licença.

</dd> <dt>

*cbStateQueryData* \[ no\]
</dt> <dd>

Contagem dos dados consultados.

</dd> <dt>

*pdwCategory* \[ fora\]
</dt> <dd>

Ponteiro para a categoria.

</dd> <dt>

*pcRemainingCounts* \[ fora\]
</dt> <dd>

Ponteiro para as contagens restantes.

</dd> <dt>

*pcRemainingHours* \[ fora\]
</dt> <dd>

Ponteiro para as horas restantes.

</dd> <dt>

*pdwReserved* \[ fora\]
</dt> <dd>

Reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método é executado com sucesso.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





