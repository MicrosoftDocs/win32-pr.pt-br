---
title: Métodos de propriedade IADsOctetList (IADs. h)
description: O método Property da interface IADsOctetList define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsOctetList
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3631adaf00cf599214296e1792ffab8697ba5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918887"
---
# <a name="iadsoctetlist-property-methods"></a>Métodos de propriedade IADsOctetList

O método Property da interface [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Octetlist**
</dt> <dd> <dl>

Uma sequência ordenada de matrizes de bytes.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsOctetList é definido como 7B28B80F-4680-11D1-A3B4-00C04FB950DC<br/>        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[**\_lista de octetos ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





