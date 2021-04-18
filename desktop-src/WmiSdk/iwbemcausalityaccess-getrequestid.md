---
description: O método getsolicitid retorna um valor de GUID (identificador global exclusivo) para uma solicitação. Um GUID é um número de bits de 128 exclusivo.
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'Método IWbemCausalityAccess:: getsolicitid (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767712"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a>Método IWbemCausalityAccess:: getsolicitid

O método **Getsolicitid** retorna um valor de GUID (identificador global exclusivo) para uma solicitação. Um GUID é um número de bits de 128 exclusivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pid* \[ fora\]
</dt> <dd>

O valor de GUID que identifica exclusivamente uma solicitação. Por exemplo, 5b2fc63a-8af4-44cb-960C-aefdced908d6.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

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

 

 




