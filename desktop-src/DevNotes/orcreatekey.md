---
description: Cria a chave do Registro especificada em um hive do registro offline. Se a chave já existir, a função a abrirá.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: Função ORCreateKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755276"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="4ee8b-104">Função ORCreateKey</span><span class="sxs-lookup"><span data-stu-id="4ee8b-104">ORCreateKey function</span></span>

<span data-ttu-id="4ee8b-105">Cria a chave do Registro especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="4ee8b-106">Se a chave já existir, a função a abrirá.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ee8b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ee8b-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="4ee8b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4ee8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ee8b-109">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-110">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="4ee8b-111">*lpSubKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-112">Um ponteiro para uma cadeia de caracteres Unicode que contém o nome de uma subchave que essa função abre ou cria.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="4ee8b-113">O parâmetro *lpSubKey* deve especificar uma subchave da chave identificada pelo parâmetro *Handle* ; pode ter até 32 níveis de profundidade na árvore do registro.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="4ee8b-114">Para obter mais informações sobre nomes de chave, consulte [estrutura do registro](../sysinfo/structure-of-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="4ee8b-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="4ee8b-115">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="4ee8b-116">Os nomes de chave não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="4ee8b-117">*lpClass* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-118">A classe (tipo de objeto) dessa chave.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-118">The class (object type) of this key.</span></span> <span data-ttu-id="4ee8b-119">Esse parâmetro pode ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-119">This parameter may be ignored.</span></span> <span data-ttu-id="4ee8b-120">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4ee8b-121">*dwOptions* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-122">Esse parâmetro pode ser 0 ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="4ee8b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee8b-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="4ee8b-124">Significado</span><span class="sxs-lookup"><span data-stu-id="4ee8b-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="4ee8b-125"><dt>**Reg \_ OPÇÃO \_ Create \_ link**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="4ee8b-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="4ee8b-126">A chave é um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-126">The key is a symbolic link.</span></span> <span data-ttu-id="4ee8b-127">O caminho de destino é atribuído ao valor de L "SymbolicLinkValue" da chave.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="4ee8b-128">O caminho de destino deve ser um caminho de registro absoluto.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="4ee8b-129">Se essa opção for definida, **a \_ opção reg \_ não \_ volátil** também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="4ee8b-130">Se o parâmetro *lpSubKey* especificar uma chave existente, ele deverá ter sido criado com **a \_ opção reg \_ Create \_ link**.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="4ee8b-131">Os links simbólicos do registro devem ser usados somente quando absolutamente necessário para compatibilidade de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="4ee8b-132"><dt>**Reg \_ OPÇÃO \_ não \_ volátil**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4ee8b-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="4ee8b-133">A chave não é volátil; Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="4ee8b-134">As informações são armazenadas em um arquivo e são preservadas quando o sistema é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="4ee8b-135">A função [**ORSaveHive**](orsavehive.md) salva as chaves que não são voláteis.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="4ee8b-136">*pSecurityDescriptor* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-137">Um ponteiro para uma estrutura de [ \_ descritor de segurança](/windows/win32/api/winnt/ns-winnt-security_descriptor) que contém um descritor de segurança para a nova chave.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="4ee8b-138">Se *pSecurityDescriptor* for **NULL**, a chave obterá um descritor de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="4ee8b-139">As ACLs em um descritor de segurança padrão para uma chave são herdadas de sua chave pai direta.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="4ee8b-140">*phkResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-141">Um ponteiro para uma variável que recebe um identificador para a chave aberta ou criada.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="4ee8b-142">Use a função [**ORCloseKey**](orclosekey.md) para fechar a chave depois de terminar de usar o identificador.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="4ee8b-143">*pdwDisposition* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="4ee8b-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4ee8b-144">Um ponteiro para uma variável que recebe um dos seguintes valores de disposição.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="4ee8b-145">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee8b-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="4ee8b-146">Significado</span><span class="sxs-lookup"><span data-stu-id="4ee8b-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="4ee8b-147"><dt>**Reg \_ \_Nova \_ chave criada**</dt> em <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4ee8b-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="4ee8b-148">A chave não existia e foi criada.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="4ee8b-149"><dt>**Reg \_ 0x00000002L \_ de \_ chave existente aberta**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4ee8b-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="4ee8b-150">A chave existia e foi simplesmente aberta sem ser alterada.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="4ee8b-151">Se *pdwDisposition* for **NULL**, nenhuma informação de disposição será retornada.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ee8b-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4ee8b-152">Return value</span></span>

<span data-ttu-id="4ee8b-153">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="4ee8b-154">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="4ee8b-155">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="4ee8b-156">Se o parâmetro *dwOptions* for definido com **a \_ opção reg \_ criar \_ link** , mas a **opção reg \_ \_ não \_ volátil** estiver clara, ou se o identificador a ser retornado for um identificador para a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="4ee8b-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ee8b-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ee8b-157">Remarks</span></span>

<span data-ttu-id="4ee8b-158">A chave que a função **ORCreateKey** cria não tem nenhum valor.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="4ee8b-159">Um aplicativo pode usar a função [**ORSetValue**](orsetvalue.md) para definir valores de chave.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="4ee8b-160">A função **ORCreateKey** não pode ser usada para criar a chave raiz em um hive de registro offline.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="4ee8b-161">Use a função [**ORCreateHive**](orcreatehive.md) para criar a chave raiz e obter um identificador para a chave.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="4ee8b-162">O registro offline não oferece suporte ao salvamento de chaves individuais.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="4ee8b-163">Use a função [**ORSaveHive**](orsavehive.md) para salvar uma chave e suas subchaves em um Hive.</span><span class="sxs-lookup"><span data-stu-id="4ee8b-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ee8b-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ee8b-164">Requirements</span></span>



| <span data-ttu-id="4ee8b-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ee8b-165">Requirement</span></span> | <span data-ttu-id="4ee8b-166">Valor</span><span class="sxs-lookup"><span data-stu-id="4ee8b-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ee8b-167">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="4ee8b-167">Redistributable</span></span><br/> | <span data-ttu-id="4ee8b-168">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="4ee8b-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="4ee8b-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ee8b-169">Header</span></span><br/>          | <dl> <span data-ttu-id="4ee8b-170"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ee8b-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="4ee8b-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4ee8b-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="4ee8b-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ee8b-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ee8b-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ee8b-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ee8b-174">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="4ee8b-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="4ee8b-175">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="4ee8b-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="4ee8b-176">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="4ee8b-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="4ee8b-177">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="4ee8b-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="4ee8b-178">\_descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="4ee8b-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
