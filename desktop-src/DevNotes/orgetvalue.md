---
description: Recupera o tipo e os dados para o valor do registro especificado em um hive do registro offline.
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: Função ORGetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748904"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="3905a-103">Função ORGetValue</span><span class="sxs-lookup"><span data-stu-id="3905a-103">ORGetValue function</span></span>

<span data-ttu-id="3905a-104">Recupera o tipo e os dados para o valor do registro especificado em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="3905a-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3905a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3905a-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="3905a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3905a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3905a-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3905a-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3905a-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="3905a-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="3905a-109">*lpSubKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3905a-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3905a-110">O nome da chave do Registro.</span><span class="sxs-lookup"><span data-stu-id="3905a-110">The name of the registry key.</span></span> <span data-ttu-id="3905a-111">Essa chave deve ser uma subchave da chave especificada pelo parâmetro *Handle* .</span><span class="sxs-lookup"><span data-stu-id="3905a-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="3905a-112">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3905a-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="3905a-113">Os nomes de chave não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3905a-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="3905a-114">*lpValue* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3905a-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3905a-115">O nome do valor do registro.</span><span class="sxs-lookup"><span data-stu-id="3905a-115">The name of the registry value.</span></span> <span data-ttu-id="3905a-116">Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, "", a função recuperará o tipo e os dados para o valor padrão ou não nomeado da chave, se houver.</span><span class="sxs-lookup"><span data-stu-id="3905a-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="3905a-117">Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="3905a-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="3905a-118">As chaves não têm um valor padrão ou não nomeado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3905a-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="3905a-119">Os valores não nomeados podem ser de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="3905a-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="3905a-120">Os nomes de valores não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="3905a-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="3905a-121">*pdwType* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3905a-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3905a-122">Um ponteiro para uma variável que recebe um código que indica o tipo de dados armazenados no valor especificado.</span><span class="sxs-lookup"><span data-stu-id="3905a-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="3905a-123">Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="3905a-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="3905a-124">Esse parâmetro poderá ser **nulo** se o tipo não for necessário.</span><span class="sxs-lookup"><span data-stu-id="3905a-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="3905a-125">*pvData* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3905a-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3905a-126">Um ponteiro para um buffer que recebe os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="3905a-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="3905a-127">Esse parâmetro poderá ser **nulo** se os dados não forem necessários.</span><span class="sxs-lookup"><span data-stu-id="3905a-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="3905a-128">Se os dados forem uma cadeia de caracteres, a função verificará se há um caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="3905a-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="3905a-129">Se um não for encontrado, a cadeia de caracteres será armazenada com um terminador nulo se o buffer for grande o suficiente para acomodar o caractere extra.</span><span class="sxs-lookup"><span data-stu-id="3905a-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="3905a-130">Caso contrário, a função falhará e retornará \_ mais dados de erro \_ .</span><span class="sxs-lookup"><span data-stu-id="3905a-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="3905a-131">*pcbData* \[ entrada, saída, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3905a-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3905a-132">Um ponteiro para uma variável que especifica o tamanho do buffer apontado pelo parâmetro *pvData* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="3905a-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="3905a-133">Quando a função retorna, essa variável contém o tamanho dos dados copiados para *pvData*.</span><span class="sxs-lookup"><span data-stu-id="3905a-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="3905a-134">O parâmetro *pcbData* poderá ser **nulo** somente se *pvData* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3905a-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="3905a-135">Se os dados tiverem o \_ tipo reg sz, Reg \_ multi sz \_ ou reg \_ expande- \_ sz, esse tamanho incluirá qualquer caractere nulo de encerramento ou caracteres.</span><span class="sxs-lookup"><span data-stu-id="3905a-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="3905a-136">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="3905a-136">For more information, see Remarks.</span></span>

<span data-ttu-id="3905a-137">Se o buffer especificado pelo parâmetro *pvData* não for grande o suficiente para manter os dados, a função retornará um erro \_ mais \_ dados e armazenará o tamanho de buffer necessário na variável apontada por *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="3905a-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="3905a-138">Nesse caso, o conteúdo do buffer *pvData* é indefinido.</span><span class="sxs-lookup"><span data-stu-id="3905a-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="3905a-139">Se *pvData* for **nulo** e *pcbData* for não **nulo**, a função retornará êxito de erro \_ e armazenará o tamanho dos dados, em bytes, na variável apontada por *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="3905a-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="3905a-140">Isso permite que um aplicativo determine a melhor maneira de alocar um buffer para os dados do valor.</span><span class="sxs-lookup"><span data-stu-id="3905a-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3905a-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3905a-141">Return value</span></span>

<span data-ttu-id="3905a-142">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="3905a-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="3905a-143">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="3905a-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="3905a-144">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="3905a-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="3905a-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="3905a-145">Remarks</span></span>

<span data-ttu-id="3905a-146">Um aplicativo normalmente chama a função [**OREnumValue**](orenumvalue.md) para determinar os nomes de valor e, em seguida, chama a função **ORGetValue** para recuperar os dados para os nomes.</span><span class="sxs-lookup"><span data-stu-id="3905a-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="3905a-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3905a-147">Requirements</span></span>



| <span data-ttu-id="3905a-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="3905a-148">Requirement</span></span> | <span data-ttu-id="3905a-149">Valor</span><span class="sxs-lookup"><span data-stu-id="3905a-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3905a-150">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3905a-150">Redistributable</span></span><br/> | <span data-ttu-id="3905a-151">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="3905a-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="3905a-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3905a-152">Header</span></span><br/>          | <dl> <span data-ttu-id="3905a-153"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3905a-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="3905a-154">DLL</span><span class="sxs-lookup"><span data-stu-id="3905a-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="3905a-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3905a-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3905a-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="3905a-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3905a-157">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="3905a-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="3905a-158">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="3905a-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="3905a-159">**OREnumValue**</span><span class="sxs-lookup"><span data-stu-id="3905a-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="3905a-160">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="3905a-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="3905a-161">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="3905a-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
