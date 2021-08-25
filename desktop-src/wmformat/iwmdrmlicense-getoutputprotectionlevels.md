---
title: Método IWMDRMLicense GetOutputProtectionLevels
description: O método GetOutputProtectionLevels recupera informações sobre todos os níveis de proteção de saída (OPLs) atribuídos à licença.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Formato de mídia do Windows do método GetOutputProtectionLevels
- Método GetOutputProtectionLevels Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8d70aaae5e96b8328c091e49836ae743c0fd5ef9d5036fd5aca067f9305d7fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771316"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a>Método IWMDRMLicense:: GetOutputProtectionLevels

O método **GetOutputProtectionLevels** recupera informações sobre todos os níveis de proteção de saída (OPLs) atribuídos à licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pOPLs* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura de níveis de proteção de saída do WMDRM que recebe as informações de OPL. [**\_ \_ \_**](wmdrm-output-protection-levels.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





