---
title: Métodos de propriedade IADsPostalAddress (Iads.h)
description: O método de propriedade da interface IADsPostalAddress define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte Métodos de propriedade de interface.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd01887751a4389984a4bc765d924d6c8a8e81dd9a65be3b7a868a3cbb845cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691123"
---
# <a name="iadspostaladdress-property-methods"></a>Métodos de propriedade IADsPostalAddress

O método de propriedade da interface [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**PostalAddress**
</dt> <dd> <dl>

Uma matriz de seis cadeias de caracteres que mantém o endereço postal do usuário.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
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
| IID<br/>                      | IID \_ IADsPostalAddress é definido como 7ADECF29-4680-11D1-A3B4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[**ADS \_ POSTALADDRESS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





