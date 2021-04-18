---
description: Abre a chave do Registro especificada em um hive do registro offline.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: Função OROpenKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749709"
---
# <a name="oropenkey-function"></a><span data-ttu-id="28fc5-103">Função OROpenKey</span><span class="sxs-lookup"><span data-stu-id="28fc5-103">OROpenKey function</span></span>

<span data-ttu-id="28fc5-104">Abre a chave do Registro especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="28fc5-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="28fc5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28fc5-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="28fc5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28fc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28fc5-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="28fc5-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28fc5-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="28fc5-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="28fc5-109">*lpSubKeyName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="28fc5-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="28fc5-110">Um ponteiro para uma cadeia de caracteres UNICODE que contém o nome da chave do registro a ser aberta.</span><span class="sxs-lookup"><span data-stu-id="28fc5-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="28fc5-111">Essa chave deve ser uma subchave da chave identificada pelo parâmetro *Handle* .</span><span class="sxs-lookup"><span data-stu-id="28fc5-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="28fc5-112">Os nomes de chave não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="28fc5-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="28fc5-113">Se esse parâmetro for **nulo** ou um ponteiro para uma cadeia de caracteres vazia, a função retornará o mesmo identificador que foi passado.</span><span class="sxs-lookup"><span data-stu-id="28fc5-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="28fc5-114">Se a chave especificada pelo parâmetro *Handle* for a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="28fc5-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="28fc5-115">Para obter mais informações, consulte [limites de tamanho do elemento do registro](../sysinfo/registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="28fc5-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="28fc5-116">*phkResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="28fc5-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28fc5-117">Um ponteiro para uma variável que recebe um identificador para a chave aberta.</span><span class="sxs-lookup"><span data-stu-id="28fc5-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="28fc5-118">Use a função [**ORCloseKey**](orclosekey.md) para fechar a chave depois de terminar de usar o identificador.</span><span class="sxs-lookup"><span data-stu-id="28fc5-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28fc5-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28fc5-119">Return value</span></span>

<span data-ttu-id="28fc5-120">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="28fc5-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="28fc5-121">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="28fc5-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="28fc5-122">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="28fc5-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="28fc5-123">Se o identificador a ser retornado for um identificador para a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="28fc5-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="28fc5-124">Se a chave especificada tiver sido marcada como excluída, essa função retornará a chave de erro \_ \_ excluída.</span><span class="sxs-lookup"><span data-stu-id="28fc5-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="28fc5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="28fc5-125">Remarks</span></span>

<span data-ttu-id="28fc5-126">A função **OROpenKey** não pode ser usada para abrir a chave raiz em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="28fc5-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="28fc5-127">Para obter um identificador para a chave raiz de um Hive, use a função [**OROpenHive**](oropenhive.md) para carregar o hive na memória.</span><span class="sxs-lookup"><span data-stu-id="28fc5-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="28fc5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28fc5-128">Requirements</span></span>



| <span data-ttu-id="28fc5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="28fc5-129">Requirement</span></span> | <span data-ttu-id="28fc5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="28fc5-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28fc5-131">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="28fc5-131">Redistributable</span></span><br/> | <span data-ttu-id="28fc5-132">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="28fc5-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="28fc5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28fc5-133">Header</span></span><br/>          | <dl> <span data-ttu-id="28fc5-134"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="28fc5-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="28fc5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="28fc5-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="28fc5-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28fc5-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28fc5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="28fc5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28fc5-138">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="28fc5-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="28fc5-139">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="28fc5-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="28fc5-140">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="28fc5-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="28fc5-141">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="28fc5-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
