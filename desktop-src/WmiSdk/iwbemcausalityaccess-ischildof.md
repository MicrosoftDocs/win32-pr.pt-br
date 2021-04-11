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
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170607"
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

## <a name="return-value"></a>Retornar valor

Retornará com êxito se a solicitação especificada for um filho da solicitação que chama o método **IsChildOf** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemint. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWbemCausalityAccess**](iwbemcausalityaccess.md)
</dt> </dl>

 

 




