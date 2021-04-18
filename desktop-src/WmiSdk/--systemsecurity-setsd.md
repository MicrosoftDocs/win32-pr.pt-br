---
description: Define o descritor de segurança para o namespace ao qual um usuário está conectado. Esse método requer um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Método definido da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813018"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="588eb-105">Método SetS da \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="588eb-105">SetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="588eb-106">O método **sets** define o descritor de segurança para o namespace ao qual um usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="588eb-106">The **SetSD** method sets the security descriptor for the namespace to which a user is connected.</span></span> <span data-ttu-id="588eb-107">Esse método requer um descritor de segurança em formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="588eb-107">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="588eb-108">Se você estiver escrevendo um script, use o método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="588eb-108">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span> <span data-ttu-id="588eb-109">Para obter mais informações, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="588eb-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="588eb-110">Se você estiver programando em C++, poderá manipular o descritor de segurança binário usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="588eb-110">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="588eb-111">Um usuário deve ter a permissão **Write \_ DAC** e, por padrão, um administrador tem essa permissão.</span><span class="sxs-lookup"><span data-stu-id="588eb-111">A user must have the **WRITE\_DAC** permission, and by default, an administrator has that permission.</span></span> <span data-ttu-id="588eb-112">A única parte do descritor de segurança que é usada é a ACE (entrada de controle de acesso) não herdada na DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="588eb-112">The only part of the security descriptor that is used is the noninherited access control entry (ACE) in the discretionary access control list (DACL).</span></span> <span data-ttu-id="588eb-113">Ao definir o sinalizador de **\_ herança de contêiner** nas Aces, o descritor de segurança afeta os namespaces filho.</span><span class="sxs-lookup"><span data-stu-id="588eb-113">By setting the **CONTAINER\_INHERIT** flag in the ACEs, the security descriptor affects child namespaces.</span></span> <span data-ttu-id="588eb-114">As ACEs allow e Deny são permitidas.</span><span class="sxs-lookup"><span data-stu-id="588eb-114">Both allow and deny ACEs are permitted.</span></span>

> [!Note]  
> <span data-ttu-id="588eb-115">Como Deny e Allow ACEs são permitidas em uma DACL, a ordem das ACEs é importante.</span><span class="sxs-lookup"><span data-stu-id="588eb-115">Because deny and allow ACEs are both permitted in a DACL, the order of ACEs is important.</span></span> <span data-ttu-id="588eb-116">Para obter mais informações, consulte [ordenando ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="588eb-116">For more information, see [Ordering of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="588eb-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="588eb-117">Syntax</span></span>


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="588eb-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="588eb-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="588eb-119">*SD* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="588eb-119">*SD* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="588eb-120">Matriz de bytes que compõe o descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="588eb-120">Byte array that makes up the security descriptor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="588eb-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="588eb-121">Return value</span></span>

<span data-ttu-id="588eb-122">Retorna um **HRESULT** que indica o status de uma chamada de método.</span><span class="sxs-lookup"><span data-stu-id="588eb-122">Returns an **HRESULT** that indicates the status of a method call.</span></span> <span data-ttu-id="588eb-123">Para aplicativos de script e Visual Basic, o resultado pode ser obtido de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="588eb-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="588eb-124">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="588eb-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="588eb-125">A lista a seguir lista os valores de retorno que são significativos para **conjuntos**.</span><span class="sxs-lookup"><span data-stu-id="588eb-125">The following list lists the return values that are significant to **SetSD**.</span></span>

<dl> <dt>

<span data-ttu-id="588eb-126">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="588eb-126">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="588eb-127">Método executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="588eb-127">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="588eb-128">**acesso ao WBEM \_ E \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="588eb-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="588eb-129">O chamador não tem direitos suficientes para chamar este método.</span><span class="sxs-lookup"><span data-stu-id="588eb-129">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="588eb-130">**\_método WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="588eb-130">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="588eb-131">Tentativa de executar este método no sistema operacional que não oferece suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="588eb-131">Attempted to run this method on OS that does not support it.</span></span>

</dd> <dt>

<span data-ttu-id="588eb-132">**\_objeto WBEM E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="588eb-132">**WBEM\_E\_INVALID\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="588eb-133">O SD não passa por testes de validade básicos.</span><span class="sxs-lookup"><span data-stu-id="588eb-133">SD does not pass basic validity tests.</span></span>

</dd> <dt>

<span data-ttu-id="588eb-134">**parâmetro de WBEM \_ E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="588eb-134">**WBEM\_E\_INVALID\_PARAMETER**</span></span>
</dt> <dd>

<span data-ttu-id="588eb-135">O SD não é válido devido a um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="588eb-135">SD is not valid due to one of the following:</span></span>

-   <span data-ttu-id="588eb-136">A DACL está ausente.</span><span class="sxs-lookup"><span data-stu-id="588eb-136">DACL is missing.</span></span>
-   <span data-ttu-id="588eb-137">A DACL não é válida.</span><span class="sxs-lookup"><span data-stu-id="588eb-137">DACL is not valid.</span></span>
-   <span data-ttu-id="588eb-138">ACE tem o sinalizador de **\_ \_ \_ representante de gravação completa de WBEM** definido e o sinalizador de **\_ \_ \_ Representante** de gravação parcial do WBEM ou do **\_ \_ provedor de gravação** do WBEM não está definido.</span><span class="sxs-lookup"><span data-stu-id="588eb-138">ACE has the **WBEM\_FULL\_WRITE\_REP** flag set, and the **WBEM\_PARTIAL\_WRITE\_REP** or **WBEM\_WRITE\_PROVIDER** flag is not set.</span></span>
-   <span data-ttu-id="588eb-139">ACE tem o **sinalizador \_ \_ ACE somente Inherit** definido sem o **sinalizador \_ \_ Ace Inherit do contêiner** .</span><span class="sxs-lookup"><span data-stu-id="588eb-139">ACE has the **INHERIT\_ONLY\_ACE** flag set without the **CONTAINER\_INHERIT\_ACE** flag.</span></span>
-   <span data-ttu-id="588eb-140">ACE tem um conjunto de bits de acesso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="588eb-140">ACE has an unknown access bit set.</span></span>
-   <span data-ttu-id="588eb-141">ACE tem um sinalizador definido que não está na tabela.</span><span class="sxs-lookup"><span data-stu-id="588eb-141">ACE has a flag set that is not in the table.</span></span>
-   <span data-ttu-id="588eb-142">ACE tem um tipo que não está na tabela.</span><span class="sxs-lookup"><span data-stu-id="588eb-142">ACE has a type that is not in the table.</span></span>
-   <span data-ttu-id="588eb-143">O proprietário e o grupo estão ausentes no SD.</span><span class="sxs-lookup"><span data-stu-id="588eb-143">The owner and group are missing from the SD.</span></span>

<span data-ttu-id="588eb-144">Para obter mais informações sobre os sinalizadores de ACE (entrada de controle de acesso), consulte [constantes de segurança do WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="588eb-144">For more information about the access control entry (ACE) flags, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="588eb-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="588eb-145">Remarks</span></span>

<span data-ttu-id="588eb-146">Para obter mais informações sobre como modificar a segurança do namespace de forma programática ou manual, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="588eb-146">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="588eb-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="588eb-147">Examples</span></span>

<span data-ttu-id="588eb-148">O script a seguir mostra como usar o **sets** para definir o descritor de segurança do namespace para o namespace raiz e alterá-lo para a matriz de bytes mostrada em *strSD*.</span><span class="sxs-lookup"><span data-stu-id="588eb-148">The following script shows how to use **SetSD** to set the namespace security descriptor for the root namespace and change it to the byte array shown in *strSD*.</span></span>


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



<span data-ttu-id="588eb-149">O exemplo de código C# a seguir usa System. Security. AccessControl. RawSecurityDescriptor para enumerar, inserir e remover novos objetos CommonAce em RawSecurityDescriptor. DiscretionaryAcl e, em seguida, convertê-lo novamente em uma matriz de bytes para salvá-lo por meio de SetS.</span><span class="sxs-lookup"><span data-stu-id="588eb-149">The following C# code sample uses the System.Security.AccessControl.RawSecurityDescriptor to enumerate, insert and remove new CommonAce objects in RawSecurityDescriptor.DiscretionaryAcl and then convert it back to an byte array to save it via SetSD.</span></span> <span data-ttu-id="588eb-150">Um SecurityIdentifier pode ser recuperado usando NTAccount e translate.</span><span class="sxs-lookup"><span data-stu-id="588eb-150">An SecurityIdentifier can be retrieved by using NTAccount and Translate.</span></span>


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a><span data-ttu-id="588eb-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="588eb-151">Requirements</span></span>



| <span data-ttu-id="588eb-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="588eb-152">Requirement</span></span> | <span data-ttu-id="588eb-153">Valor</span><span class="sxs-lookup"><span data-stu-id="588eb-153">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="588eb-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="588eb-154">Minimum supported client</span></span><br/> | <span data-ttu-id="588eb-155">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="588eb-155">Windows Vista</span></span><br/>       |
| <span data-ttu-id="588eb-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="588eb-156">Minimum supported server</span></span><br/> | <span data-ttu-id="588eb-157">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="588eb-157">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="588eb-158">Namespace</span><span class="sxs-lookup"><span data-stu-id="588eb-158">Namespace</span></span><br/>                | <span data-ttu-id="588eb-159">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="588eb-159">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="588eb-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="588eb-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="588eb-161">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="588eb-161">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="588eb-162">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="588eb-162">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="588eb-163">**\_\_SystemSecurity:: Obtém-se**</span><span class="sxs-lookup"><span data-stu-id="588eb-163">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="588eb-164">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="588eb-164">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="588eb-165">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="588eb-165">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="588eb-166">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="588eb-166">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="588eb-167">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="588eb-167">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

