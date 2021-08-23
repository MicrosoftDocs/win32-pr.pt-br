---
title: Métodos de propriedade IADsCaseIgnoreList (Iads.h)
description: O método de propriedade da interface IADsCaseIgnoreList define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte Métodos de propriedade de interface.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsCaseIgnoreList ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e2f07d3c4afa6cd55f6a757ccae6f2d1076b954e0afdd0c82c8a5247af33f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961915"
---
# <a name="iadscaseignorelist-property-methods"></a>Métodos de propriedade IADsCaseIgnoreList

O método de propriedade da interface [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**CaseIgnoreList**
</dt> <dd> <dl>

Uma sequência ordenada de cadeias de caracteres sem valor de maiúsculas e minúsculas.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
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
| IID<br/>                      | IID \_ IADsCaseIgnoreList é definido como 7B66B533-4680-11D1-A3B4-00C04FB950DC<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[**ADS \_ CASEIGNORE \_ LIST**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





