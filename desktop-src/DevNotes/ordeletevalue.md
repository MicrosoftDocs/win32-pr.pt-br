---
description: Remove um valor nomeado da chave do Registro especificada em um hive do registro offline.
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: Função ORDeleteValue (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755755"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="9d83f-103">Função ORDeleteValue</span><span class="sxs-lookup"><span data-stu-id="9d83f-103">ORDeleteValue function</span></span>

<span data-ttu-id="9d83f-104">Remove um valor nomeado da chave do Registro especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="9d83f-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d83f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d83f-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="9d83f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d83f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d83f-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9d83f-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d83f-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="9d83f-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="9d83f-109">*lpValueName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9d83f-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d83f-110">O valor do registro a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9d83f-110">The registry value to be removed.</span></span> <span data-ttu-id="9d83f-111">Se esse parâmetro for **nulo** ou uma cadeia de caracteres vazia, o valor padrão sem nome definido pela função [**ORSetValue**](orsetvalue.md) será removido.</span><span class="sxs-lookup"><span data-stu-id="9d83f-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="9d83f-112">Os nomes de valores não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9d83f-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d83f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9d83f-113">Return value</span></span>

<span data-ttu-id="9d83f-114">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="9d83f-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9d83f-115">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9d83f-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9d83f-116">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="9d83f-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d83f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d83f-117">Requirements</span></span>



| <span data-ttu-id="9d83f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d83f-118">Requirement</span></span> | <span data-ttu-id="9d83f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9d83f-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d83f-120">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9d83f-120">Redistributable</span></span><br/> | <span data-ttu-id="9d83f-121">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9d83f-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9d83f-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d83f-122">Header</span></span><br/>          | <dl> <span data-ttu-id="9d83f-123"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d83f-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d83f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9d83f-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="9d83f-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d83f-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d83f-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d83f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d83f-127">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="9d83f-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
