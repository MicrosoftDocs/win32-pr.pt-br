---
title: Métodos de propriedade IADsTimestamp (Iads.h)
description: O método de propriedade da interface IADsTimestamp define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte Métodos de propriedade de interface.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsTimestamp ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a105a2ba246c38b7cf6c5bdd1c7420096397e294bb29d5bed446b31d3ca9763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427556"
---
# <a name="iadstimestamp-property-methods"></a>Métodos de propriedade IADsTimestamp

O método de propriedade da interface [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**EventID**
</dt> <dd> <dl>

Um identificador de evento.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

**WholeSeconds**
</dt> <dd> <dl>

Número de segundos com valor zero sendo 12:00 AM, janeiro de 1970, UTC.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsTimestamp é definido como \_ B2F5A901-4080-11D1-A3AC-00C04FB950DC<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[**TIMESTAMP DO ADS \_**](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





