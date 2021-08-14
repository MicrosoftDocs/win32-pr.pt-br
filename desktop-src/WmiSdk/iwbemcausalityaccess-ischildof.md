---
description: O método IsChildOf determina se uma solicitação é um filho de uma solicitação especificada (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'Método IWbemCausalityAccess:: IsChildOf (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 509508d5e1a273dc681cf3c9f645ead1037408d6ecfe5ed666186ba6e2a2c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318288"
---
# <a name="iwbemcausalityaccessischildof-method"></a>Método IWbemCausalityAccess:: IsChildOf

O método **IsChildOf** determina se uma solicitação é um filho de uma solicitação especificada (PID). Uma solicitação pai pode ter várias solicitações filho. Cada solicitação é identificada por um GUID (identificador global exclusivo) e pode ter uma solicitação pai ou pode ser uma solicitação superior. Um GUID é um número de bits de 128 exclusivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pid* \[ no\]
</dt> <dd>

O valor de GUID que identifica exclusivamente uma solicitação. Por exemplo, 5b2fc63a-8af4-44cb-960C-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará com êxito se a solicitação especificada for um filho da solicitação que chama o método **IsChildOf** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




