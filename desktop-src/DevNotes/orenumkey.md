---
description: Enumera as subchaves da chave do registro aberta especificada em um hive do registro offline. A função recupera informações sobre uma subchave cada vez que ela é chamada.
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: Função OREnumKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748905"
---
# <a name="orenumkey-function"></a><span data-ttu-id="5b479-104">Função OREnumKey</span><span class="sxs-lookup"><span data-stu-id="5b479-104">OREnumKey function</span></span>

<span data-ttu-id="5b479-105">Enumera as subchaves da chave do registro aberta especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="5b479-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="5b479-106">A função recupera informações sobre uma subchave cada vez que ela é chamada.</span><span class="sxs-lookup"><span data-stu-id="5b479-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b479-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b479-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="5b479-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b479-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b479-109">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5b479-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-110">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="5b479-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="5b479-111">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5b479-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-112">O índice da subchave a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="5b479-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="5b479-113">Esse parâmetro deve ser zero para a primeira chamada para a função e, em seguida, incrementado para chamadas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5b479-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="5b479-114">Como as subchaves não são ordenadas, qualquer subnovação terá um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="5b479-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="5b479-115">Isso significa que a função pode retornar subchaves em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="5b479-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="5b479-116">*lpName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5b479-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-117">Um ponteiro para um buffer que recebe o nome da subchave, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5b479-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="5b479-118">A função copia apenas o nome da subchave, não a hierarquia de chave completa, para o buffer.</span><span class="sxs-lookup"><span data-stu-id="5b479-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="5b479-119">Se a função falhar, nenhuma informação será copiada para esse buffer.</span><span class="sxs-lookup"><span data-stu-id="5b479-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="5b479-120">Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="5b479-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b479-121">*lpcName* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5b479-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-122">Um ponteiro para uma variável que especifica o tamanho do buffer especificado pelo parâmetro *lpName* , em **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="5b479-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="5b479-123">Esse tamanho deve incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5b479-123">This size should include the terminating null character.</span></span> <span data-ttu-id="5b479-124">Se a função for realizada com sucesso, a variável apontada por *lpcName* conterá o número de caracteres armazenados no buffer, sem incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5b479-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="5b479-125">*lpClass* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5b479-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-126">Um ponteiro para um buffer que recebe a cadeia de caracteres de classe terminada em nulo da subchave enumerada.</span><span class="sxs-lookup"><span data-stu-id="5b479-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="5b479-127">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5b479-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b479-128">*lpcClass* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5b479-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-129">Um ponteiro para uma variável que especifica o tamanho do buffer especificado pelo parâmetro *lpClass* , em **WCHARs**.</span><span class="sxs-lookup"><span data-stu-id="5b479-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="5b479-130">O tamanho deve incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5b479-130">The size should include the terminating null character.</span></span> <span data-ttu-id="5b479-131">Se a função for realizada com sucesso, *lpcClass* conterá o número de caracteres armazenados no buffer, sem incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="5b479-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="5b479-132">Esse parâmetro poderá ser **nulo** somente se *lpClass* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="5b479-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b479-133">*lpftLastWriteTime* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5b479-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5b479-134">Um ponteiro para a estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recebe a hora em que a subchave enumerada foi gravada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="5b479-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="5b479-135">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5b479-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b479-136">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b479-136">Return value</span></span>

<span data-ttu-id="5b479-137">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="5b479-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="5b479-138">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="5b479-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="5b479-139">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="5b479-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="5b479-140">Os códigos de erro possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5b479-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="5b479-141">Se o buffer *lpName* for muito pequeno para receber o nome da chave, a função retornará um erro com \_ mais \_ dados.</span><span class="sxs-lookup"><span data-stu-id="5b479-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="5b479-142">Se não houver mais subchaves disponíveis, a função retornará \_ um erro sem \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="5b479-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b479-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b479-143">Remarks</span></span>

<span data-ttu-id="5b479-144">Para enumerar subchaves, um aplicativo deve chamar inicialmente a função **OREnumKey** com o parâmetro *dwIndex* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="5b479-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="5b479-145">O aplicativo deve incrementar o parâmetro *dwIndex* e chamar **OREnumKey** até que não haja mais subchaves (o que significa que a função retorna \_ um erro sem \_ mais \_ itens).</span><span class="sxs-lookup"><span data-stu-id="5b479-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="5b479-146">O aplicativo também pode definir *dwIndex* para o índice da última subchave na primeira chamada para a função e decrementar o índice até que a subchave com o índice 0 seja enumerada.</span><span class="sxs-lookup"><span data-stu-id="5b479-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="5b479-147">Para recuperar o índice da última subchave, use a função [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) .</span><span class="sxs-lookup"><span data-stu-id="5b479-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="5b479-148">Embora um aplicativo esteja usando a função **OREnumKey** , ele não deve fazer chamadas para nenhuma das funções de registro offline que possam alterar a chave que está sendo enumerada.</span><span class="sxs-lookup"><span data-stu-id="5b479-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b479-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b479-149">Requirements</span></span>



| <span data-ttu-id="5b479-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b479-150">Requirement</span></span> | <span data-ttu-id="5b479-151">Valor</span><span class="sxs-lookup"><span data-stu-id="5b479-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b479-152">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5b479-152">Redistributable</span></span><br/> | <span data-ttu-id="5b479-153">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5b479-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="5b479-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b479-154">Header</span></span><br/>          | <dl> <span data-ttu-id="5b479-155"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b479-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b479-156">DLL</span><span class="sxs-lookup"><span data-stu-id="5b479-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="5b479-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b479-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b479-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b479-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b479-159">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="5b479-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="5b479-160">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="5b479-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="5b479-161">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="5b479-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="5b479-162">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="5b479-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
