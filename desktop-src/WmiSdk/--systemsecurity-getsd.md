---
description: Obtém o descritor de segurança para o namespace ao qual o usuário está conectado. Esse método retorna um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Método obtido da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: d471db22a9f15a38ab693ae72332e5e1893b5c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810810"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a><span data-ttu-id="8ea03-105">Método obtido da \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="8ea03-105">GetSD method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="8ea03-106">O método **Extornado** Obtém o descritor de segurança para o namespace ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="8ea03-106">The **GetSD** method gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="8ea03-107">Esse método retorna um descritor de segurança em formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="8ea03-107">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="8ea03-108">Se você estiver escrevendo um script, use o método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea03-108">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span> <span data-ttu-id="8ea03-109">Para obter mais informações, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8ea03-109">For more information, see [Securing WMI Namespaces](securing-wmi-namespaces.md) and [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="8ea03-110">O usuário deve ter a **permissão \_ controle de leitura** .</span><span class="sxs-lookup"><span data-stu-id="8ea03-110">The user must have the **READ\_CONTROL** permission.</span></span> <span data-ttu-id="8ea03-111">Por padrão, os administradores têm essa permissão.</span><span class="sxs-lookup"><span data-stu-id="8ea03-111">By default, administrators have that permission.</span></span> <span data-ttu-id="8ea03-112">A única parte do descritor de segurança que é realmente usada é a DACL (lista de controle de acesso discricionário).</span><span class="sxs-lookup"><span data-stu-id="8ea03-112">The only part of the security descriptor that is actually used is the discretionary access control list (DACL).</span></span> <span data-ttu-id="8ea03-113">A DACL pode conter ACEs herdadas e não herdadas.</span><span class="sxs-lookup"><span data-stu-id="8ea03-113">The DACL can contain both inherited and non-inherited ACEs.</span></span> <span data-ttu-id="8ea03-114">As ACEs Deny e Allow são permitidas.</span><span class="sxs-lookup"><span data-stu-id="8ea03-114">Both deny and allow ACEs are permitted.</span></span>

<span data-ttu-id="8ea03-115">Se você estiver programando em C++, poderá manipular o descritor de segurança binário usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="8ea03-115">If you are programming in C++, you can manipulate the binary security descriptor using [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea03-116">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ea03-116">Syntax</span></span>


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a><span data-ttu-id="8ea03-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ea03-117">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea03-118">*SD* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8ea03-118">*SD* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea03-119">Descritor de segurança em formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="8ea03-119">Security descriptor in binary byte array format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea03-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ea03-120">Return value</span></span>

<span data-ttu-id="8ea03-121">Esse método retorna um **HRESULT** que indica o status da chamada do método.</span><span class="sxs-lookup"><span data-stu-id="8ea03-121">This method returns an **HRESULT** indicating the status of the method call.</span></span> <span data-ttu-id="8ea03-122">A lista a seguir lista os valores de retorno que são de significância a serem **obtidas**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-122">The following list lists the return values that are of significance to **GetSD**.</span></span> <span data-ttu-id="8ea03-123">Para aplicativos de script e Visual Basic, o resultado pode ser obtido de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8ea03-123">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="8ea03-124">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8ea03-124">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="8ea03-125">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="8ea03-125">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="8ea03-126">Método executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8ea03-126">Method executed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="8ea03-127">**acesso ao WBEM \_ E \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="8ea03-127">**WBEM\_E\_ACCESS\_DENIED**</span></span>
</dt> <dd>

<span data-ttu-id="8ea03-128">O chamador não tem direitos suficientes para chamar este método.</span><span class="sxs-lookup"><span data-stu-id="8ea03-128">Caller does not have sufficient rights to call this method.</span></span>

</dd> <dt>

<span data-ttu-id="8ea03-129">**\_método WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="8ea03-129">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="8ea03-130">Tentativa de executar este método em um sistema sem suporte.</span><span class="sxs-lookup"><span data-stu-id="8ea03-130">Attempted to run this method on an unsupported system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ea03-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ea03-131">Remarks</span></span>

<span data-ttu-id="8ea03-132">Para obter mais informações sobre como modificar a segurança do namespace de forma programática ou manual, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="8ea03-132">For more information about modifying namespace security programmatically or manually, see [Securing WMI Namespaces](securing-wmi-namespaces.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8ea03-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ea03-133">Examples</span></span>

<span data-ttu-id="8ea03-134">O script a seguir mostra como usar o **obtémd** para obter o descritor de segurança atual para o \\ namespace raiz Cimv2 e alterá-lo para a matriz de bytes mostrada em **exibido**.</span><span class="sxs-lookup"><span data-stu-id="8ea03-134">The following script shows you how to use **GetSD** to obtain the current security descriptor for the Root\\Cimv2 namespace and change it to the byte array shown in **DisplaySD**.</span></span>


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a><span data-ttu-id="8ea03-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea03-135">Requirements</span></span>



| <span data-ttu-id="8ea03-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea03-136">Requirement</span></span> | <span data-ttu-id="8ea03-137">Valor</span><span class="sxs-lookup"><span data-stu-id="8ea03-137">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8ea03-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ea03-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8ea03-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ea03-139">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8ea03-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ea03-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8ea03-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ea03-141">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8ea03-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="8ea03-142">Namespace</span></span><br/>                | <span data-ttu-id="8ea03-143">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="8ea03-143">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8ea03-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ea03-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea03-145">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="8ea03-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="8ea03-146">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="8ea03-146">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="8ea03-147">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8ea03-147">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="8ea03-148">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8ea03-148">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="8ea03-149">**\_\_SystemSecurity:: definido**</span><span class="sxs-lookup"><span data-stu-id="8ea03-149">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="8ea03-150">**\_Descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="8ea03-150">**Security\_Descriptor**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="8ea03-151">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="8ea03-151">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="8ea03-152">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="8ea03-152">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> </dl>

 

