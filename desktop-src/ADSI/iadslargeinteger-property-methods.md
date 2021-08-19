---
title: Métodos de propriedade IADsLargeInteger (IADs. h)
description: Os métodos de propriedade da interface IADsLargeInteger obtêm e definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsLargeInteger
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b46a992accea468b6f3c8a70c7fcfcbe63cf72667c4394c27df273767a387b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023474"
---
# <a name="iadslargeinteger-property-methods"></a>Métodos de propriedade IADsLargeInteger

Os métodos de propriedade da interface [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) obtêm e definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**HighPart**
</dt> <dd> <dl>

A parte superior do inteiro.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

**LowPart**
</dt> <dd> <dl>

A parte inferior do inteiro.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Comentários

Se largeInt for do tipo **LargeInteger** , seu valor será especificado por aqueles de **HighPart** e **LowPart** de acordo com a fórmula a seguir.


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a>Exemplos

o exemplo de código a seguir Visual Basic define um inteiro grande como 43937327281.


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsLargeInteger é definido como 9068270B-0939-11D1-8BE1-00C04FD8D503<br/>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





