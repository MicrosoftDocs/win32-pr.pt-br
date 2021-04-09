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
ms.openlocfilehash: 0c5c07213a2d2a3a1b64621dbc40f707b0900703
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085472"
---
# <a name="iadssecuritydescriptor-property-methods"></a><span data-ttu-id="0d1b2-105">Métodos de propriedade IADsSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="0d1b2-105">IADsSecurityDescriptor Property Methods</span></span>

<span data-ttu-id="0d1b2-106">Os métodos de propriedade da interface [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-106">The property methods of the [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="0d1b2-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0d1b2-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0d1b2-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d1b2-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0d1b2-109">**Controle**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-109">**Control**</span></span>
<span data-ttu-id="0d1b2-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-111">Sinalizadores que qualificam o significado do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-111">Flags that qualify the meaning of the security descriptor.</span></span> <span data-ttu-id="0d1b2-112">Os valores são obtidos da estrutura [**de \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) do Win32.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-112">Values are taken from the Win32 [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) structure.</span></span>

<dt>

<span data-ttu-id="0d1b2-113">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-114">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-114">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="0d1b2-115">**DaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-115">**DaclDefaulted**</span></span>
<span data-ttu-id="0d1b2-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-117">Um sinalizador do tipo BOOL que indica se a DACL é derivada de um mecanismo padrão, em vez de ser fornecida explicitamente pelo provedor original do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-117">A flag of the BOOL type that indicates if the DACL is derived from a default mechanism, rather than being provided explicitly by the original provider of the security descriptor.</span></span> <span data-ttu-id="0d1b2-118">Por exemplo, se o criador de um objeto não especificar uma DACL, o objeto receberá a DACL padrão do token de acesso do criador.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-118">For example, if an object's creator does not specify a DACL, the object receives the default DACL from the creator's access token.</span></span> <span data-ttu-id="0d1b2-119">Esse sinalizador pode afetar como o sistema trata a DACL, em relação à herança de ACE.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-119">This flag can affect how the system treats the DACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="0d1b2-120">O sistema ignora esse sinalizador se o sinalizador SE a \_ DACL \_ presente não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-120">The system ignores this flag if the SE\_DACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="0d1b2-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-122">Tipo de dados Scripting: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-122">Scripting data type: **VARIANT\_BOOL**</span></span>
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

<span data-ttu-id="0d1b2-123">**DiscretionaryAcl**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-123">**DiscretionaryAcl**</span></span>
<span data-ttu-id="0d1b2-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-125">DACL (lista de controle de acesso discricionário) que especifica os tipos de acesso concedidos ao objeto para usuários e grupos especificados.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-125">Discretionary access-control list (DACL) that specifies the types of access granted to the object for specified users and groups.</span></span> <span data-ttu-id="0d1b2-126">Para obter mais informações sobre DACLs, consulte [DACLs nulas e DACLs vazias](/windows/desktop/AD/null-dacls-and-empty-dacls).</span><span class="sxs-lookup"><span data-stu-id="0d1b2-126">For more information about DACLs, see [Null DACLs and Empty DACLs](/windows/desktop/AD/null-dacls-and-empty-dacls).</span></span>

<dt>

<span data-ttu-id="0d1b2-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-128">Tipo de dados de script: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-128">Scripting data type: **IDispatch**</span></span>
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

<span data-ttu-id="0d1b2-129">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-129">**Group**</span></span>
<span data-ttu-id="0d1b2-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-131">Grupo ao qual a ID de segurança do proprietário pertence.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-131">Group to which the owner's security ID belongs.</span></span>

<dt>

<span data-ttu-id="0d1b2-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-133">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-133">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="0d1b2-134">**GroupDefaulted**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-134">**GroupDefaulted**</span></span>
<span data-ttu-id="0d1b2-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-136">Um sinalizador do tipo BOOL que indica se os dados do grupo são derivados de um mecanismo padrão, em vez de serem explicitamente fornecidos pelo provedor original do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-136">A flag of the BOOL type that indicates if the group data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="0d1b2-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-138">Tipo de dados Scripting: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-138">Scripting data type: **VARIANT\_BOOL**</span></span>
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

<span data-ttu-id="0d1b2-139">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-139">**Owner**</span></span>
<span data-ttu-id="0d1b2-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-141">Proprietário do objeto.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-141">Object owner.</span></span>

<dt>

<span data-ttu-id="0d1b2-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-143">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-143">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="0d1b2-144">**OwnerDefaulted**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-144">**OwnerDefaulted**</span></span>
<span data-ttu-id="0d1b2-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-146">Um sinalizador do tipo BOOL que indica que os dados do proprietário são derivados de um mecanismo padrão, em vez de serem explicitamente fornecidos pelo provedor original do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-146">A flag of the BOOL type that indicates that the owner data is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span>

<dt>

<span data-ttu-id="0d1b2-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-148">Tipo de dados Scripting: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-148">Scripting data type: **VARIANT\_BOOL**</span></span>
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

<span data-ttu-id="0d1b2-149">**Revisão**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-149">**Revision**</span></span>
<span data-ttu-id="0d1b2-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-151">Nível de revisão do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-151">Revision level of the security descriptor.</span></span> <span data-ttu-id="0d1b2-152">Esse valor é obtido da estrutura de [**\_ \_ informações de revisão da ACL**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) do Win32.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-152">This value is taken from the Win32 [**ACL\_REVISION\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-acl_revision_information) structure.</span></span> <span data-ttu-id="0d1b2-153">Todas as ACEs em uma ACL devem estar no mesmo nível de revisão.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-153">All ACEs in an ACL must be at the same revision level.</span></span>

<dt>

<span data-ttu-id="0d1b2-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-155">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-155">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="0d1b2-156">**SaclDefaulted**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-156">**SaclDefaulted**</span></span>
<span data-ttu-id="0d1b2-157"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-157"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-158">Um sinalizador do tipo BOOL que indica que a SACL é derivada de um mecanismo padrão, em vez de ser explicitamente fornecido pelo provedor original do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-158">A flag of the BOOL type that indicates that the SACL is derived from a default mechanism, rather than being explicitly provided by the original provider of the security descriptor.</span></span> <span data-ttu-id="0d1b2-159">Esse sinalizador pode afetar como o sistema manipula a SACL, com relação à herança de ACE.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-159">This flag can affect how the system handles the SACL, with respect to ACE inheritance.</span></span> <span data-ttu-id="0d1b2-160">O sistema ignora esse sinalizador se o sinalizador da \_ SACL \_ presente não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-160">The system ignores this flag if the SE\_SACL\_PRESENT flag is not set.</span></span>

<dt>

<span data-ttu-id="0d1b2-161">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-162">Tipo de dados Scripting: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-162">Scripting data type: **VARIANT\_BOOL**</span></span>
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

<span data-ttu-id="0d1b2-163">**SystemAcl**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-163">**SystemAcl**</span></span>
<span data-ttu-id="0d1b2-164"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d1b2-164"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d1b2-165">Acesso do sistema – lista de controle usada para gerar registros de auditoria para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-165">System access-control list used to generate audit records for the object.</span></span>

<dt>

<span data-ttu-id="0d1b2-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0d1b2-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d1b2-167">Tipo de dados de script: **IDispatch**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-167">Scripting data type: **IDispatch**</span></span>
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

 

## <a name="examples"></a><span data-ttu-id="0d1b2-168">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0d1b2-168">Examples</span></span>

<span data-ttu-id="0d1b2-169">O exemplo de código a seguir mostra como enumerar um descritor de segurança existente.</span><span class="sxs-lookup"><span data-stu-id="0d1b2-169">The following code example shows how to enumerate an existing security descriptor.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="0d1b2-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d1b2-170">Requirements</span></span>



| <span data-ttu-id="0d1b2-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d1b2-171">Requirement</span></span> | <span data-ttu-id="0d1b2-172">Valor</span><span class="sxs-lookup"><span data-stu-id="0d1b2-172">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1b2-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d1b2-173">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1b2-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d1b2-174">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="0d1b2-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d1b2-175">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1b2-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d1b2-176">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="0d1b2-177">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d1b2-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1b2-178"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1b2-178"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="0d1b2-179">DLL</span><span class="sxs-lookup"><span data-stu-id="0d1b2-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d1b2-180"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d1b2-180"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0d1b2-181">IID</span><span class="sxs-lookup"><span data-stu-id="0d1b2-181">IID</span></span><br/>                      | <span data-ttu-id="0d1b2-182">IID \_ IADsSecurityDescriptor é definido como B8C787CA-9BDD-11D0-852C-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="0d1b2-182">IID\_IADsSecurityDescriptor is defined as B8C787CA-9BDD-11D0-852C-00C04FD8D503</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d1b2-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d1b2-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1b2-184">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-184">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)
</dt> <dt>

[<span data-ttu-id="0d1b2-185">**IADsAccessControlEntry**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-185">**IADsAccessControlEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)
</dt> <dt>

[<span data-ttu-id="0d1b2-186">**IADsAccessControlList**</span><span class="sxs-lookup"><span data-stu-id="0d1b2-186">**IADsAccessControlList**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)
</dt> </dl>

 

