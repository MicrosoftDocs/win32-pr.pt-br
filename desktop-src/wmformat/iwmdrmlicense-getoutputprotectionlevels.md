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
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105813679"
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

## <a name="return-value"></a>Retornar valor

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

 

 





