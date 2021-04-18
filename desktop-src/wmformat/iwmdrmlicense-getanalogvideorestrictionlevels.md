---
title: Método IWMDRMLicense GetAnalogVideoRestrictionLevels (wmdrmsdk. h)
description: O método GetAnalogVideoRestrictionLevels recupera todas as restrições de vídeo analógicas definidas na licença atual.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Formato de mídia do Windows do método GetAnalogVideoRestrictionLevels
- Método GetAnalogVideoRestrictionLevels Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método GetAnalogVideoRestrictionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105807841"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a>Método IWMDRMLicense:: GetAnalogVideoRestrictionLevels

O método **GetAnalogVideoRestrictionLevels** recupera todas as restrições de vídeo analógicas definidas na licença atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*\[ rgAnalogVideoRestrictions \]* \[out\]
</dt> <dd>

Recebe uma matriz de estruturas de [**\_ \_ \_ restrições de vídeo analógicos do WMDRM**](wmdrm-analog-video-restrictions.md) . Defina como **NULL** para obter o número de elementos na matriz em *pcResctrictions*.

</dd> <dt>

*pcRestrictions* \[ entrada, saída\]
</dt> <dd>

O número de elementos na matriz de restrições. Se *rgAnalogVideoRestrictions* for definido como **NULL**, esse valor será definido como o número de elementos necessários na matriz.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Você deve alocar memória para a matriz de restrições. Para fazer isso, primeiro chame o método com *rgAnalogVideoRestrictions* definido como **NULL**, que definirá o valor em *pcRestrictions* como o número de elementos necessários.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





