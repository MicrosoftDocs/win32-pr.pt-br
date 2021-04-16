---
description: Define os dados para o valor de uma chave do Registro especificada em um hive do registro offline.
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: Função ORSetValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752370"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="63a72-103">Função ORSetValue</span><span class="sxs-lookup"><span data-stu-id="63a72-103">ORSetValue function</span></span>

<span data-ttu-id="63a72-104">Define os dados para o valor de uma chave do Registro especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="63a72-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63a72-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="63a72-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63a72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a72-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="63a72-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a72-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="63a72-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="63a72-109">*lpValueName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63a72-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63a72-110">O nome do valor a ser definido.</span><span class="sxs-lookup"><span data-stu-id="63a72-110">The name of the value to be set.</span></span> <span data-ttu-id="63a72-111">Se um valor com esse nome ainda não estiver presente na chave, a função o adicionará à chave.</span><span class="sxs-lookup"><span data-stu-id="63a72-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="63a72-112">Se *lpValueName* for **nulo** ou uma cadeia de caracteres vazia, "", a função definirá o tipo e os dados para o valor padrão ou não nomeado da chave.</span><span class="sxs-lookup"><span data-stu-id="63a72-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="63a72-113">Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="63a72-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="63a72-114">As chaves do registro não têm valores padrão, mas podem ter um valor não nomeado, que pode ser de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="63a72-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="63a72-115">*dwType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63a72-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a72-116">O tipo de dados apontado pelo parâmetro *lpData* .</span><span class="sxs-lookup"><span data-stu-id="63a72-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="63a72-117">Para obter uma lista dos tipos possíveis, consulte [tipos de valor do registro](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="63a72-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="63a72-118">*lpData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="63a72-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="63a72-119">Os dados a serem armazenados.</span><span class="sxs-lookup"><span data-stu-id="63a72-119">The data to be stored.</span></span>

<span data-ttu-id="63a72-120">Para tipos baseados em cadeia de caracteres, como REG \_ sz, a cadeia de caracteres deve ser terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="63a72-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="63a72-121">Para o \_ tipo de dados reg multi \_ sz, a cadeia de caracteres deve ser terminada com dois caracteres nulos.</span><span class="sxs-lookup"><span data-stu-id="63a72-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="63a72-122">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="63a72-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63a72-123">O tamanho das informações apontadas pelo parâmetro *lpData* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="63a72-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="63a72-124">Se os dados forem do tipo REG \_ sz, Reg \_ Expand \_ sz ou reg \_ multi \_ sz, *cbData* deverá incluir o tamanho do caractere ou dos caracteres nulos de terminação.</span><span class="sxs-lookup"><span data-stu-id="63a72-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a72-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="63a72-125">Return value</span></span>

<span data-ttu-id="63a72-126">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="63a72-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="63a72-127">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="63a72-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="63a72-128">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="63a72-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a72-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="63a72-129">Remarks</span></span>

<span data-ttu-id="63a72-130">Os tamanhos de valor são limitados pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="63a72-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="63a72-131">Valores longos (mais de 2048 bytes) devem ser armazenados como arquivos com os nomes de arquivo armazenados no registro.</span><span class="sxs-lookup"><span data-stu-id="63a72-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="63a72-132">Isso ajuda o registro a ser executado com eficiência.</span><span class="sxs-lookup"><span data-stu-id="63a72-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="63a72-133">Elementos de aplicativo, como ícones, bitmaps e arquivos executáveis, devem ser armazenados como arquivos e não podem ser colocados no registro.</span><span class="sxs-lookup"><span data-stu-id="63a72-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a72-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63a72-134">Requirements</span></span>



| <span data-ttu-id="63a72-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="63a72-135">Requirement</span></span> | <span data-ttu-id="63a72-136">Valor</span><span class="sxs-lookup"><span data-stu-id="63a72-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63a72-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="63a72-137">Redistributable</span></span><br/> | <span data-ttu-id="63a72-138">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="63a72-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="63a72-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63a72-139">Header</span></span><br/>          | <dl> <span data-ttu-id="63a72-140"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="63a72-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="63a72-141">DLL</span><span class="sxs-lookup"><span data-stu-id="63a72-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="63a72-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63a72-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a72-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="63a72-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63a72-144">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="63a72-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="63a72-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="63a72-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
