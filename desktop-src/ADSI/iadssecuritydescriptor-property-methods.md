---
title: Métodos de propriedade IADsSecurityDescriptor (IADs. h)
description: Os métodos de propriedade da interface IADsSecurityDescriptor obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: e0c50740-de98-4913-b3df-6fd53263bcc8
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsSecurityDescriptor
topic_type:
- apiref
api_name:
- IADsSecurityDescriptor Property Methods
- IADsSecurityDescriptor.Revision
- IADsSecurityDescriptor.get_Revision
- IADsSecurityDescriptor.put_Revision
- IADsSecurityDescriptor.Control
- IADsSecurityDescriptor.get_Control
- IADsSecurityDescriptor.put_Control
- IADsSecurityDescriptor.Owner
- IADsSecurityDescriptor.get_Owner
- IADsSecurityDescriptor.put_Owner
- IADsSecurityDescriptor.OwnerDefaulted
- IADsSecurityDescriptor.get_OwnerDefaulted
- IADsSecurityDescriptor.put_OwnerDefaulted
- IADsSecurityDescriptor.Group
- IADsSecurityDescriptor.get_Group
- IADsSecurityDescriptor.put_Group
- IADsSecurityDescriptor.GroupDefaulted
- IADsSecurityDescriptor.get_GroupDefaultedY
- IADsSecurityDescriptor.put_GroupDefaulted
- IADsSecurityDescriptor.DiscretionaryAcl
- IADsSecurityDescriptor.get_DiscretionaryAcl
- IADsSecurityDescriptor.put_DiscretionaryAcl
- IADsSecurityDescriptor.DaclDefaulted
- IADsSecurityDescriptor.get_DaclDefaulted
- IADsSecurityDescriptor.put_DaclDefaulted
- IADsSecurityDescriptor.SystemAcl
- IADsSecurityDescriptor.get_SystemAcl
- IADsSecurityDescriptor.put_SystemAcl
- IADsSecurityDescriptor.SaclDefaulted
- IADsSecurityDescriptor.get_SaclDefaulted
- IADsSecurityDescriptor.put_SaclDefaulted
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a795195af94e248f304747ba7edcf4f7a55e11e051e1cb66937242de1d732bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427622"
---
# <a name="iadssecuritydescriptor-property-methods"></a>Métodos de propriedade IADsSecurityDescriptor

Os métodos de propriedade da interface [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**Controle**
</dt> <dd> <dl>

Sinalizadores que qualificam o significado do descritor de segurança. Os valores são obtidos da estrutura [**de \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) do Win32.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Control(
  [out] LONG* plControl
);
HRESULT put_Control(
  [in] LONG lControl
);
```


</dt> </dl> </dd> <dt>

**DaclDefaulted**
</dt> <dd> <dl>

Um sinalizador do tipo BOOL que indica se a DACL é derivada de um mecanismo padrão, em vez de ser fornecida explicitamente pelo provedor original do descritor de segurança. Por exemplo, se o criador de um objeto não especificar uma DACL, o objeto receberá a DACL padrão do token de acesso do criador. Esse sinalizador pode afetar como o sistema trata a DACL, em relação à herança de ACE. o sistema ignorará esse sinalizador se o sinalizador de ES \_ DACL \_ presente não estiver definido.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados Scripting: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DaclDefaulted(
  [out] VARIANT_BOOL* fDaclDefaulted
);
HRESULT put_DaclDefaulted(
  [in] VARIANT_BOOL fDaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**DiscretionaryAcl**
</dt> <dd> <dl>

DACL (lista de controle de acesso discricionário) que especifica os tipos de acesso concedidos ao objeto para usuários e grupos especificados. Para obter mais informações sobre DACLs, consulte [DACLs nulas e DACLs vazias](/windows/desktop/AD/null-dacls-and-empty-dacls).

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DiscretionaryAcl(
  [out] IDispatch** ppIDispDACL
);
HRESULT put_DiscretionaryAcl(
  [in] IDispatch* pIDispDACL
);
```


</dt> </dl> </dd> <dt>

**Grupo**
</dt> <dd> <dl>

Grupo ao qual a ID de segurança do proprietário pertence.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Group(
  [out] BSTR* pbstrGroupl
);
HRESULT put_Group(
  [in] BSTR bstrGroup
);
```


</dt> </dl> </dd> <dt>

**GroupDefaulted**
</dt> <dd> <dl>

Um sinalizador do tipo BOOL que indica se os dados do grupo são derivados de um mecanismo padrão, em vez de serem explicitamente fornecidos pelo provedor original do descritor de segurança.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados Scripting: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GroupDefaultedY(
  [out] VARIANT_BOOL* fGroupDefaulted
);
HRESULT put_GroupDefaulted(
  [in] VARIANT_BOOL fGroupDefaulted
);
```


</dt> </dl> </dd> <dt>

**Proprietário**
</dt> <dd> <dl>

Proprietário do objeto.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Owner(
  [out] BSTR* pbstrOwnerl
);
HRESULT put_Owner(
  [in] BSTR bstrOwner
);
```


</dt> </dl> </dd> <dt>

**OwnerDefaulted**
</dt> <dd> <dl>

Um sinalizador do tipo BOOL que indica que os dados do proprietário são derivados de um mecanismo padrão, em vez de serem explicitamente fornecidos pelo provedor original do descritor de segurança.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados Scripting: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OwnerDefaulted(
  [out] VARIANT_BOOL* fOwnerDefaulted
);
HRESULT put_OwnerDefaulted(
  [in] VARIANT_BOOL fOwnerDefaulted
);
```


</dt> </dl> </dd> <dt>

**Revisão**
</dt> <dd> <dl>

Nível de revisão do descritor de segurança. Esse valor é obtido da estrutura de [**\_ \_ informações de revisão da ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) do Win32. Todas as ACEs em uma ACL devem estar no mesmo nível de revisão.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **longo**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Revision(
  [out] LONG* plRevision
);
HRESULT put_Revision(
  [in] LONG lRevision
);
```


</dt> </dl> </dd> <dt>

**SaclDefaulted**
</dt> <dd> <dl>

Um sinalizador do tipo BOOL que indica que a SACL é derivada de um mecanismo padrão, em vez de ser explicitamente fornecido pelo provedor original do descritor de segurança. Esse sinalizador pode afetar como o sistema manipula a SACL, com relação à herança de ACE. o sistema ignora esse sinalizador se o sinalizador de ES \_ SACL \_ presente não estiver definido.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados Scripting: **Variant \_ bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SaclDefaulted(
  [out] VARIANT_BOOL* fSaclDefaulted
);
HRESULT put_SaclDefaulted(
  [in] VARIANT_BOOL fSaclDefaulted
);
```


</dt> </dl> </dd> <dt>

**SystemAcl**
</dt> <dd> <dl>

Acesso do sistema – lista de controle usada para gerar registros de auditoria para o objeto.

<dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Tipo de dados de script: **IDispatch**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SystemAcl(
  [out] IDispatch** ppIDispSACL
);
HRESULT put_SystemAcl(
  [in] IDispatch* pIDispSACL
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como enumerar um descritor de segurança existente.


```VB
Dim ou As IADs
Dim sd As IADsSecurityDescriptor
Dim dacl As IADsAccessControlList
Dim sacl As IADsAccessControlList

On Error GoTo Cleanup 
 
Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set sd = ou.Get("ntSecurityDescriptor")
Debug.Print sd.Owner
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
Set dacl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
' Add code to perform an operation with the Discretionary and System ACLs.

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
    Set sd = Nothing
    Set dacl = Nothing
    Set sacl = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsSecurityDescriptor é definido como B8C787CA-9BDD-11D0-852C-00C04FD8D503<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

