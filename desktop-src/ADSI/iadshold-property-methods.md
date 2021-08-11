---
title: Métodos de propriedade IADsHold (Iads.h)
description: O método de propriedade da interface IADsHold define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte Métodos de propriedade de interface.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- ADSI (métodos de propriedade IADsHold)
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fae4d5f5a83577d297bfea6e109d78ad3d8bd2291cfa028f37fb8ab1a4f825b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179554"
---
# <a name="iadshold-property-methods"></a>Métodos de propriedade IADsHold

O método de propriedade da interface [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [Métodos de propriedade de interface](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Valor**
</dt> <dd> <dl>

A quantidade de encargos contra o usuário durante o período em espera enquanto o servidor verifica o saldo da conta do usuário.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

**ObjectName**
</dt> <dd> <dl>

O nome do objeto que representa um usuário em espera.

<dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID IADsHold é definido como \_ B3EB3B37-4080-11D1-A3AC-00C04FB950DC<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





