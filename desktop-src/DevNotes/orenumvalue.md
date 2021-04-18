---
description: Enumera os valores para a chave de registro aberta especificada em um hive de registro offline. A função recupera informações de um valor sob a chave especificada cada vez que a função é chamada.
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: Função OREnumValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753059"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="50104-104">Função OREnumValue</span><span class="sxs-lookup"><span data-stu-id="50104-104">OREnumValue function</span></span>

<span data-ttu-id="50104-105">Enumera os valores para a chave de registro aberta especificada em um hive de registro offline.</span><span class="sxs-lookup"><span data-stu-id="50104-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="50104-106">A função recupera informações de um valor sob a chave especificada cada vez que a função é chamada.</span><span class="sxs-lookup"><span data-stu-id="50104-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="50104-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50104-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="50104-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50104-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50104-109">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="50104-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-110">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="50104-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="50104-111">*dwIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="50104-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-112">O índice do valor a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="50104-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="50104-113">Esse parâmetro deve ser zero para a primeira chamada para a função e, em seguida, ser incrementado para chamadas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="50104-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="50104-114">Como os valores não são ordenados, qualquer valor novo terá um índice arbitrário.</span><span class="sxs-lookup"><span data-stu-id="50104-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="50104-115">Isso significa que a função pode retornar valores em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="50104-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="50104-116">*lpValueName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="50104-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-117">Um ponteiro para um buffer que recebe o nome do valor como uma cadeia de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="50104-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="50104-118">Esse buffer deve ser grande o suficiente para incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="50104-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="50104-119">Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="50104-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="50104-120">*lpcValueName* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="50104-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-121">Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpValueName* , em caracteres.</span><span class="sxs-lookup"><span data-stu-id="50104-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="50104-122">Quando a função retorna, a variável recebe o número de caracteres armazenados no buffer, sem incluir o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="50104-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="50104-123">*lpType* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50104-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-124">Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado.</span><span class="sxs-lookup"><span data-stu-id="50104-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="50104-125">Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="50104-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="50104-126">O parâmetro *lpType* poderá ser **nulo** se o código de tipo não for necessário.</span><span class="sxs-lookup"><span data-stu-id="50104-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="50104-127">*lpData* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50104-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-128">Um ponteiro para um buffer que recebe os dados para a entrada de valor.</span><span class="sxs-lookup"><span data-stu-id="50104-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="50104-129">Esse parâmetro poderá ser **nulo** se os dados não forem necessários.</span><span class="sxs-lookup"><span data-stu-id="50104-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="50104-130">Se *lpData* for **nulo** e *lpcbData* for não **nulo**, a função armazenará o tamanho dos dados, em bytes, na variável apontada por *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="50104-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="50104-131">Isso permite que um aplicativo determine a melhor maneira de alocar um buffer para os dados.</span><span class="sxs-lookup"><span data-stu-id="50104-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="50104-132">*lpcbData* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="50104-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="50104-133">Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *lpData* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="50104-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="50104-134">Quando a função retorna, a variável recebe o número de bytes armazenados no buffer.</span><span class="sxs-lookup"><span data-stu-id="50104-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="50104-135">Esse parâmetro poderá ser **nulo** somente se *lpData* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="50104-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="50104-136">Se os dados tiverem o \_ tipo reg sz, Reg \_ multi sz \_ ou reg \_ expande- \_ sz, esse tamanho incluirá qualquer caractere nulo de encerramento ou caracteres.</span><span class="sxs-lookup"><span data-stu-id="50104-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="50104-137">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="50104-137">For more information, see Remarks.</span></span>

<span data-ttu-id="50104-138">Se o buffer especificado por *lpData* não for grande o suficiente para manter os dados, a função retornará um erro \_ mais \_ dados e armazenará o tamanho de buffer necessário na variável apontada por *lpcbData*.</span><span class="sxs-lookup"><span data-stu-id="50104-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="50104-139">Nesse caso, o conteúdo de *lpData* é indefinido.</span><span class="sxs-lookup"><span data-stu-id="50104-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50104-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50104-140">Return value</span></span>

<span data-ttu-id="50104-141">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="50104-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="50104-142">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="50104-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="50104-143">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="50104-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="50104-144">Se o buffer *lpData* for muito pequeno para receber o valor, a função retornará um erro com \_ mais \_ dados.</span><span class="sxs-lookup"><span data-stu-id="50104-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="50104-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="50104-145">Remarks</span></span>

<span data-ttu-id="50104-146">Para enumerar valores, um aplicativo deve chamar inicialmente a função **OREnumValue** com o parâmetro *dwIndex* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="50104-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="50104-147">O aplicativo deve incrementar *dwIndex* e chamar a função **OREnumValue** até que não haja mais valores (até que a função retorne \_ um erro sem \_ mais \_ itens).</span><span class="sxs-lookup"><span data-stu-id="50104-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="50104-148">O aplicativo também pode definir *dwIndex* como o índice do último valor na primeira chamada para a função e decrementar o índice até que o valor com o índice 0 seja enumerado.</span><span class="sxs-lookup"><span data-stu-id="50104-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="50104-149">Para recuperar o índice do último valor, use a função [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="50104-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="50104-150">Ao usar **OREnumValue**, um aplicativo não deve chamar nenhuma função de registro offline que possa alterar a chave que está sendo consultada.</span><span class="sxs-lookup"><span data-stu-id="50104-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="50104-151">Se os dados tiverem o \_ tipo reg sz, Reg \_ multi sz \_ ou reg \_ expandem \_ sz, a cadeia de caracteres poderá não ter sido armazenada com os caracteres de terminação de nulo apropriados.</span><span class="sxs-lookup"><span data-stu-id="50104-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="50104-152">Portanto, mesmo que a função retorne o êxito do erro \_ , o aplicativo deve garantir que a cadeia de caracteres seja encerrada corretamente antes de usá-la; caso contrário, ela poderá substituir um buffer.</span><span class="sxs-lookup"><span data-stu-id="50104-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="50104-153">(Observe que REG \_ As \_ cadeias de caracteres de vários sz devem ter dois personagens de terminação nulo.)</span><span class="sxs-lookup"><span data-stu-id="50104-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="50104-154">Para determinar o tamanho máximo do nome e dos buffers de dados, use a função [**ORQueryInfoKey**](orqueryinfokey.md) .</span><span class="sxs-lookup"><span data-stu-id="50104-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="50104-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50104-155">Requirements</span></span>



| <span data-ttu-id="50104-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="50104-156">Requirement</span></span> | <span data-ttu-id="50104-157">Valor</span><span class="sxs-lookup"><span data-stu-id="50104-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50104-158">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="50104-158">Redistributable</span></span><br/> | <span data-ttu-id="50104-159">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="50104-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="50104-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50104-160">Header</span></span><br/>          | <dl> <span data-ttu-id="50104-161"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="50104-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="50104-162">DLL</span><span class="sxs-lookup"><span data-stu-id="50104-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="50104-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50104-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50104-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="50104-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50104-165">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="50104-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="50104-166">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="50104-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="50104-167">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="50104-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="50104-168">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="50104-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
