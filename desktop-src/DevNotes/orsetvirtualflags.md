---
description: Define os sinalizadores de virtualização na chave do registro aberta especificada em um hive do registro offline.
ms.assetid: c625af35-8e14-4379-8d0a-6f5b65a1aebb
title: Função ORSetVirtualFlags (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetVirtualFlags
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: f694d69684a474cfa6d4f6c33c6d8cab7072f605
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755754"
---
# <a name="orsetvirtualflags-function"></a><span data-ttu-id="314f9-103">Função ORSetVirtualFlags</span><span class="sxs-lookup"><span data-stu-id="314f9-103">ORSetVirtualFlags function</span></span>

<span data-ttu-id="314f9-104">Define os sinalizadores de virtualização na chave do registro aberta especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="314f9-104">Sets virtualization flags on the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="314f9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="314f9-105">Syntax</span></span>


```C++
DWORD ORSetVirtualFlags(
  _In_ ORHKEY Handle,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="314f9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="314f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="314f9-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="314f9-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314f9-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="314f9-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="314f9-109">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="314f9-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="314f9-110">Esse parâmetro controla o comportamento do registro quando uma operação de criação ou abertura falha em uma chave em um Hive virtualizado.</span><span class="sxs-lookup"><span data-stu-id="314f9-110">This parameter controls the behavior of the registry when a Create or Open operation fails on a key in a virtualized hive.</span></span> <span data-ttu-id="314f9-111">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="314f9-111">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="314f9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="314f9-112">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="314f9-113">Significado</span><span class="sxs-lookup"><span data-stu-id="314f9-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_KEY_DONT_SILENT_FAIL"></span><span id="reg_key_dont_silent_fail"></span><dl> <span data-ttu-id="314f9-114"><dt>**Reg \_ CHAVE \_ não \_ silenciosa com \_ falha**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="314f9-114"><dt>**REG\_KEY\_DONT\_SILENT\_FAIL**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="314f9-115">Se esse sinalizador for definido e uma operação de abertura falhar em uma chave para a qual a virtualização está habilitada, o registro não tentará reabrir a chave.</span><span class="sxs-lookup"><span data-stu-id="314f9-115">If this flag is set and an Open operation fails on a key for which virtualization is enabled, the registry does not attempt to reopen the key.</span></span> <span data-ttu-id="314f9-116">Se esse sinalizador estiver claro, o registro tentará reabrir a chave com o máximo \_ permitido de acesso.</span><span class="sxs-lookup"><span data-stu-id="314f9-116">If this flag is clear, the registry attempts to reopen the key with the MAXIMUM\_ALLOWED access.</span></span><br/>                                                                                    |
| <span id="REG_KEY_DONT_VIRTUALIZE"></span><span id="reg_key_dont_virtualize"></span><dl> <span data-ttu-id="314f9-117"><dt>**Reg \_ A chave não \_ \_ virtualiza**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="314f9-117"><dt>**REG\_KEY\_DONT\_VIRTUALIZE**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="314f9-118">Se esse sinalizador for definido e uma operação de criação de chave falhar porque o chamador não tem a chave \_ Create \_ sub \_ Key diretamente na chave pai, o registro falhará na operação de criação.</span><span class="sxs-lookup"><span data-stu-id="314f9-118">If this flag is set and a Create Key operation fails because the caller does not have the KEY\_CREATE\_SUB\_KEY right on the parent key, the registry fails the Create operation.</span></span> <span data-ttu-id="314f9-119">Se esse sinalizador for claro, o registro tentará criar a chave no repositório virtual.</span><span class="sxs-lookup"><span data-stu-id="314f9-119">If this flag is clear, the registry attempts to create the key in the virtual store.</span></span> <span data-ttu-id="314f9-120">O chamador deve ter o direito de leitura de chave \_ na chave pai.</span><span class="sxs-lookup"><span data-stu-id="314f9-120">The caller must have the KEY\_READ right on the parent key.</span></span><br/> |
| <span id="REG_KEY_RECURSE_FLAG"></span><span id="reg_key_recurse_flag"></span><dl> <span data-ttu-id="314f9-121"><dt>**Reg \_ \_ \_ Sinalizador de recursão de chave**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="314f9-121"><dt>**REG\_KEY\_RECURSE\_FLAG**</dt> <dt>8</dt></span></span> </dl>              | <span data-ttu-id="314f9-122">Se esse sinalizador for definido, os sinalizadores de virtualização do registro serão propagados da chave pai.</span><span class="sxs-lookup"><span data-stu-id="314f9-122">If this flag is set, registry virtualization flags are propagated from the parent key.</span></span> <span data-ttu-id="314f9-123">Se esse sinalizador for claro, os sinalizadores de virtualização do registro não serão propagados.</span><span class="sxs-lookup"><span data-stu-id="314f9-123">If this flag is clear, registry virtualization flags are not propagated.</span></span><br/>                                                                                                                                                                    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="314f9-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="314f9-124">Return value</span></span>

<span data-ttu-id="314f9-125">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="314f9-125">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="314f9-126">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="314f9-126">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="314f9-127">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="314f9-127">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="314f9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="314f9-128">Remarks</span></span>

<span data-ttu-id="314f9-129">A virtualização do registro é uma tecnologia de compatibilidade de aplicativos provisória que permite que as operações de gravação do registro que têm impacto global sejam redirecionadas para locais por usuário.</span><span class="sxs-lookup"><span data-stu-id="314f9-129">Registry virtualization is an interim application compatibility technology that enables registry write operations that have global impact to be redirected to per-user locations.</span></span> <span data-ttu-id="314f9-130">Esse redirecionamento é transparente para os aplicativos que lêem ou gravam no registro.</span><span class="sxs-lookup"><span data-stu-id="314f9-130">This redirection is transparent to applications reading from or writing to the registry.</span></span>

<span data-ttu-id="314f9-131">A virtualização do registro tem suporte a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="314f9-131">Registry virtualization is supported starting with Windows Vista.</span></span> <span data-ttu-id="314f9-132">No entanto, a Microsoft pretende removê-la de versões futuras do sistema operacional Windows à medida que mais aplicativos são tornados compatíveis com o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="314f9-132">However, Microsoft intends to remove it from future versions of the Windows operating system as more applications are made compatible with Windows Vista.</span></span> <span data-ttu-id="314f9-133">Portanto, os aplicativos não devem depender do comportamento da virtualização do registro no sistema.</span><span class="sxs-lookup"><span data-stu-id="314f9-133">Therefore, applications should not depend on the behavior of registry virtualization in the system.</span></span>

<span data-ttu-id="314f9-134">A virtualização do registro é habilitada apenas para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="314f9-134">Registry virtualization is enabled only for the following:</span></span>

-   <span data-ttu-id="314f9-135">processos interativos de 32 bits</span><span class="sxs-lookup"><span data-stu-id="314f9-135">32-bit interactive processes</span></span>
-   <span data-ttu-id="314f9-136">Chaves em **HKEY \_ local \_ Machine \\ software**</span><span class="sxs-lookup"><span data-stu-id="314f9-136">Keys in **HKEY\_LOCAL\_MACHINE\\Software**</span></span>
-   <span data-ttu-id="314f9-137">Chaves que um administrador pode gravar</span><span class="sxs-lookup"><span data-stu-id="314f9-137">Keys that an administrator can write to</span></span>

<span data-ttu-id="314f9-138">Para obter mais informações, consulte [virtualização de registro](../sysinfo/registry-virtualization.md).</span><span class="sxs-lookup"><span data-stu-id="314f9-138">For more information, see [Registry Virtualization](../sysinfo/registry-virtualization.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="314f9-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="314f9-139">Requirements</span></span>



| <span data-ttu-id="314f9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="314f9-140">Requirement</span></span> | <span data-ttu-id="314f9-141">Valor</span><span class="sxs-lookup"><span data-stu-id="314f9-141">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="314f9-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="314f9-142">Redistributable</span></span><br/> | <span data-ttu-id="314f9-143">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="314f9-143">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="314f9-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="314f9-144">Header</span></span><br/>          | <dl> <span data-ttu-id="314f9-145"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="314f9-145"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="314f9-146">DLL</span><span class="sxs-lookup"><span data-stu-id="314f9-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="314f9-147"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="314f9-147"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314f9-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="314f9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314f9-149">**ORGetVirtualFlags**</span><span class="sxs-lookup"><span data-stu-id="314f9-149">**ORGetVirtualFlags**</span></span>](orgetvirtualflags.md)
</dt> <dt>

[<span data-ttu-id="314f9-150">Virtualização do registro</span><span class="sxs-lookup"><span data-stu-id="314f9-150">Registry Virtualization</span></span>](../sysinfo/registry-virtualization.md)
</dt> </dl>

 

 
