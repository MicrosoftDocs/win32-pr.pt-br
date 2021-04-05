---
title: Métodos de propriedade IADsDomain (IADs. h)
description: Os métodos de interface IADsDomain lêem e gravam as propriedades descritas neste tópico. Para obter mais informações, consulte interface Property Methods.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsDomain
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a10c6377c7e97f83046f60d46312a03db68cadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918893"
---
# <a name="iadsdomain-property-methods"></a><span data-ttu-id="eab69-105">Métodos de propriedade IADsDomain</span><span class="sxs-lookup"><span data-stu-id="eab69-105">IADsDomain Property Methods</span></span>

<span data-ttu-id="eab69-106">Os métodos de interface [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) lêem e gravam as propriedades descritas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="eab69-106">The [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) interface methods read and write the properties described in this topic.</span></span> <span data-ttu-id="eab69-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="eab69-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="eab69-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="eab69-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="eab69-109">**AutoUnlockInterval**</span><span class="sxs-lookup"><span data-stu-id="eab69-109">**AutoUnlockInterval**</span></span>
<span data-ttu-id="eab69-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-111">Indica o tempo mínimo que deve decorrer antes que a conta seja reabilitada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eab69-111">Indicates the minimum time that must elapse before the account is automatically reenabled.</span></span>

<dt>

<span data-ttu-id="eab69-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-114">**Grupo de trabalho**</span><span class="sxs-lookup"><span data-stu-id="eab69-114">**IsWorkgroup**</span></span>
<span data-ttu-id="eab69-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-116">Esta propriedade não é mais implementada.</span><span class="sxs-lookup"><span data-stu-id="eab69-116">This property is no longer implemented.</span></span>

<dt>

<span data-ttu-id="eab69-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="eab69-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eab69-118">Tipo de dados Scripting: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="eab69-118">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-119">**LockoutObservationInterval**</span><span class="sxs-lookup"><span data-stu-id="eab69-119">**LockoutObservationInterval**</span></span>
<span data-ttu-id="eab69-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-121">Indica a janela de tempo durante a qual a contagem de senha inadequada é monitorada e acumulada antes de determinar se a conta precisa ser bloqueada. Por exemplo, se o número de tentativas de senha incorretas em uma conta exceder o limite (máximo de senhas incorretas permitidas) durante o período de tempo especificado (intervalo de observação de bloqueio), a conta será bloqueada definindo a propriedade apropriada no conjunto de propriedades de parâmetro de logon.</span><span class="sxs-lookup"><span data-stu-id="eab69-121">Indicates the time window during which the bad password count is monitored and accumulated before determining whether the account needs to be locked out. For example, if the number of bad password attempts on an account exceed the threshold (Maximum Bad Passwords Allowed) during the specified time period (Lockout Observation Interval) the account will be locked out by setting the appropriate property in the Login Parameter property set.</span></span>

<dt>

<span data-ttu-id="eab69-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-123">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-124">**MaxBadPasswordsAllowed**</span><span class="sxs-lookup"><span data-stu-id="eab69-124">**MaxBadPasswordsAllowed**</span></span>
<span data-ttu-id="eab69-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-126">Indica o número máximo de logons de senha inválidos permitidos antes de um bloqueio de conta.</span><span class="sxs-lookup"><span data-stu-id="eab69-126">Indicates the maximum number of bad password logins allowed before an account lockout.</span></span>

<dt>

<span data-ttu-id="eab69-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-128">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-129">**MaxPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="eab69-129">**MaxPasswordAge**</span></span>
<span data-ttu-id="eab69-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-131">Indica o intervalo de tempo máximo, em segundos, após o qual a senha deve ser alterada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="eab69-131">Indicates the maximum time interval, in seconds, after which the password must be changed by the user.</span></span>

<dt>

<span data-ttu-id="eab69-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-133">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-134">**MinPasswordAge**</span><span class="sxs-lookup"><span data-stu-id="eab69-134">**MinPasswordAge**</span></span>
<span data-ttu-id="eab69-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-136">Indica o intervalo de tempo mínimo, em segundos, antes que a senha possa ser alterada.</span><span class="sxs-lookup"><span data-stu-id="eab69-136">Indicates the minimum time interval, in seconds, before the password can be changed.</span></span>

<dt>

<span data-ttu-id="eab69-137">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-138">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-139">**MinPasswordLength**</span><span class="sxs-lookup"><span data-stu-id="eab69-139">**MinPasswordLength**</span></span>
<span data-ttu-id="eab69-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-141">Indica o número mínimo de caracteres que devem ser usados para uma senha.</span><span class="sxs-lookup"><span data-stu-id="eab69-141">Indicates the minimum number of characters that must be used for a password.</span></span>

<dt>

<span data-ttu-id="eab69-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-143">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-143">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-144">**Senhaattributes**</span><span class="sxs-lookup"><span data-stu-id="eab69-144">**PasswordAttributes**</span></span>
<span data-ttu-id="eab69-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-146">Indica restrições em senhas, conforme definido pela lista de atributos e valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eab69-146">Indicates restrictions on passwords, as defined by the following list of attributes and values.</span></span>

> [!Note]  
> <span data-ttu-id="eab69-147">Para \_ a atributo de senha \_ complexo, a senha deve incluir pelo menos uma marca de pontuação ou um caractere não imprimível.</span><span class="sxs-lookup"><span data-stu-id="eab69-147">For PASSWORD\_ATTR\_COMPLEX, the password must include at least one punctuation mark or non-printable character.</span></span>

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

<span data-ttu-id="eab69-148">**Senha \_ do ATTR \_ None** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="eab69-148">**PASSWORD\_ATTR\_NONE** (0x00000000)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

<span data-ttu-id="eab69-149">**Senha \_ do \_ \_ Diferenciar maiúsculas de minúsculas** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="eab69-149">**PASSWORD\_ATTR\_MIXED\_CASE** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

<span data-ttu-id="eab69-150">**Senha \_ do ATTR \_ complexo** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="eab69-150">**PASSWORD\_ATTR\_COMPLEX** (0x00000002)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="eab69-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-151">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-152">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-152">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="eab69-153">**PasswordHistoryLength**</span><span class="sxs-lookup"><span data-stu-id="eab69-153">**PasswordHistoryLength**</span></span>
<span data-ttu-id="eab69-154"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="eab69-154"></dt> <dd> <dl></span></span>

<span data-ttu-id="eab69-155">Indica o número de senhas anteriores salvas na lista de histórico.</span><span class="sxs-lookup"><span data-stu-id="eab69-155">Indicates the number of previous passwords saved in the history list.</span></span> <span data-ttu-id="eab69-156">O usuário não pode reutilizar uma senha na lista de histórico.</span><span class="sxs-lookup"><span data-stu-id="eab69-156">The user cannot reuse a password in the history list.</span></span>

<dt>

<span data-ttu-id="eab69-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="eab69-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="eab69-158">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="eab69-158">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="eab69-159">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eab69-159">Examples</span></span>

<span data-ttu-id="eab69-160">O exemplo de código a seguir exibe o valor da propriedade **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="eab69-160">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



<span data-ttu-id="eab69-161">O exemplo de código a seguir exibe o valor da propriedade **PasswordHistoryLength** .</span><span class="sxs-lookup"><span data-stu-id="eab69-161">The following code example displays the value of the **PasswordHistoryLength** property.</span></span>


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a><span data-ttu-id="eab69-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eab69-162">Requirements</span></span>



| <span data-ttu-id="eab69-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="eab69-163">Requirement</span></span> | <span data-ttu-id="eab69-164">Valor</span><span class="sxs-lookup"><span data-stu-id="eab69-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eab69-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eab69-165">Minimum supported client</span></span><br/> | <span data-ttu-id="eab69-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eab69-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eab69-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eab69-167">Minimum supported server</span></span><br/> | <span data-ttu-id="eab69-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eab69-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eab69-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eab69-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="eab69-170"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab69-170"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="eab69-171">DLL</span><span class="sxs-lookup"><span data-stu-id="eab69-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab69-172"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eab69-172"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="eab69-173">IID</span><span class="sxs-lookup"><span data-stu-id="eab69-173">IID</span></span><br/>                      | <span data-ttu-id="eab69-174">IID \_ IADsDomain é definido como 00E4C220-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="eab69-174">IID\_IADsDomain is defined as 00E4C220-FD16-11CE-ABC4-02608C9E7553</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="eab69-175">Confira também</span><span class="sxs-lookup"><span data-stu-id="eab69-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab69-176">**IADsDomain**</span><span class="sxs-lookup"><span data-stu-id="eab69-176">**IADsDomain**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[<span data-ttu-id="eab69-177">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="eab69-177">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





