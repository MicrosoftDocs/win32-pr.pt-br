---
description: Recupera informações sobre a chave do Registro especificada em um hive do registro offline.
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: Função ORQueryInfoKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756105"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="c67cc-103">Função ORQueryInfoKey</span><span class="sxs-lookup"><span data-stu-id="c67cc-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="c67cc-104">Recupera informações sobre a chave do Registro especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="c67cc-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c67cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c67cc-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="c67cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c67cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67cc-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="c67cc-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-109">*lpClass* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-110">Um ponteiro para um buffer que recebe a classe de chave.</span><span class="sxs-lookup"><span data-stu-id="c67cc-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="c67cc-111">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-112">*lpcClass* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-113">Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpClass* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="c67cc-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="c67cc-114">O tamanho deve incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-114">The size should include the terminating null character.</span></span> <span data-ttu-id="c67cc-115">Quando a função retorna, essa variável contém o tamanho da cadeia de caracteres de classe que é armazenada no buffer.</span><span class="sxs-lookup"><span data-stu-id="c67cc-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="c67cc-116">A contagem retornada não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="c67cc-117">Se o buffer não for grande o suficiente, a função retornará um erro com \_ mais \_ dados, e a variável conterá o tamanho da cadeia de caracteres, em caracteres, sem contar o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="c67cc-118">Se *lpClass* for **nulo**, *lpcClass* poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="c67cc-119">Se o parâmetro *lpClass* for um endereço válido, mas o parâmetro *lpcClass* não for (por exemplo, se o parâmetro *lpcClass* for **nulo**), a função retornará um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="c67cc-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-120">*lpcSubKeys* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-121">Um ponteiro para uma variável que recebe o número de subchaves que estão contidas na chave especificada.</span><span class="sxs-lookup"><span data-stu-id="c67cc-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="c67cc-122">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-123">*lpcMaxSubKeyLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-124">Um ponteiro para uma variável que recebe o tamanho da subchave da chave com o nome mais longo, em caracteres Unicode, sem incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="c67cc-125">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-126">*lpcMaxClassLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-127">Um ponteiro para uma variável que recebe o tamanho da cadeia de caracteres mais longa que especifica uma classe de subchave, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c67cc-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="c67cc-128">A contagem retornada não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="c67cc-129">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-130">*lpcValues* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-131">Um ponteiro para uma variável que recebe o número de valores associados à chave.</span><span class="sxs-lookup"><span data-stu-id="c67cc-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="c67cc-132">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-133">*lpcMaxValueNameLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-134">Um ponteiro para uma variável que recebe o tamanho do nome de valor mais longo da chave, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c67cc-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="c67cc-135">O tamanho não inclui o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="c67cc-136">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-137">*lpcMaxValueLen* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-138">Um ponteiro para uma variável que recebe o tamanho do componente de dados mais longo entre os valores da chave, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c67cc-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="c67cc-139">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-140">*lpcbSecurityDescriptor* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-141">Um ponteiro para uma variável que recebe o tamanho do descritor de segurança da chave, em bytes.</span><span class="sxs-lookup"><span data-stu-id="c67cc-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="c67cc-142">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c67cc-143">*lpftLastWriteTime* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c67cc-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c67cc-144">Um ponteiro para uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que recebe a última hora de gravação.</span><span class="sxs-lookup"><span data-stu-id="c67cc-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="c67cc-145">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c67cc-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="c67cc-146">A função define os membros da estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) para indicar a última vez que a chave ou qualquer uma de suas entradas de valor é modificada.</span><span class="sxs-lookup"><span data-stu-id="c67cc-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67cc-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c67cc-147">Return value</span></span>

<span data-ttu-id="c67cc-148">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="c67cc-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="c67cc-149">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="c67cc-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="c67cc-150">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="c67cc-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="c67cc-151">Se o buffer *lpClass* for muito pequeno para receber o nome da classe, a função retornará um erro \_ mais \_ dados.</span><span class="sxs-lookup"><span data-stu-id="c67cc-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67cc-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c67cc-152">Requirements</span></span>



| <span data-ttu-id="c67cc-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="c67cc-153">Requirement</span></span> | <span data-ttu-id="c67cc-154">Valor</span><span class="sxs-lookup"><span data-stu-id="c67cc-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c67cc-155">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c67cc-155">Redistributable</span></span><br/> | <span data-ttu-id="c67cc-156">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="c67cc-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="c67cc-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c67cc-157">Header</span></span><br/>          | <dl> <span data-ttu-id="c67cc-158"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67cc-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="c67cc-159">DLL</span><span class="sxs-lookup"><span data-stu-id="c67cc-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="c67cc-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c67cc-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c67cc-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="c67cc-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67cc-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="c67cc-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="c67cc-163">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="c67cc-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="c67cc-164">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="c67cc-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="c67cc-165">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="c67cc-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
