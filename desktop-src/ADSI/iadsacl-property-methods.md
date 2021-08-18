---
title: Métodos de propriedade IADsAcl (IADs. h)
description: O método Property da interface IADsAcl define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: eb4786d7-d366-4924-8255-dc28ea47a246
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsAcl
topic_type:
- apiref
api_name:
- IADsAcl Property Methods
- IADsAcl.ProtectedAttrName
- IADsAcl.get_ProtecteAttrName
- IADsAcl.put_ProtectedAttrName
- IADsAcl.SubjectName
- IADsAcl.get_SubjectName
- IADsAcl.put_SubjectName
- IADsAcl.Privileges
- IADsAcl.get_Privileges
- IADsAcl.put_Privileges
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebe534df506bcf25aa618213a4e274500035c8ea8b21941ae4e57a784d26c30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961925"
---
# <a name="iadsacl-property-methods"></a>Métodos de propriedade IADsAcl

O método Property da interface [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl) define a propriedade descrita na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Privilégios**
</dt> <dd> <dl>

Configurações de privilégio.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Privileges(
  [out] LONG* retval
);
HRESULT put_Privileges(
  [in] LONG lnPrivileges
);
```


</dt> </dl> </dd> <dt>

**ProtectedAttrName**
</dt> <dd> <dl>

Nome de um atributo protegido.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ProtecteAttrName(
  [out] BSTR* retVal
);
HRESULT put_ProtectedAttrName(
  [in] BSTR bstrProtectedAttrName
);
```


</dt> </dl> </dd> <dt>

**SubjectName**
</dt> <dd> <dl>

Nome do assunto.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SubjectName(
  [out] BSTR* retval
);
HRESULT put_SubjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsAcl é definido como 8452D3AB-0869-11D1-A377-00C04FB950DC<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)
</dt> </dl>

 

 





