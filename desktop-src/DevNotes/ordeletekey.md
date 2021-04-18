---
description: Exclui uma subchave e seus valores de um hive do registro offline.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Função ORDeleteKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751951"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="9838e-103">Função ORDeleteKey</span><span class="sxs-lookup"><span data-stu-id="9838e-103">ORDeleteKey function</span></span>

<span data-ttu-id="9838e-104">Exclui uma subchave e seus valores de um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="9838e-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9838e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9838e-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="9838e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9838e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9838e-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9838e-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9838e-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="9838e-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="9838e-109">Esse identificador é retornado pela função [**ORCreateKey**](orcreatekey.md) ou [**OROpenKey**](oropenkey.md) .</span><span class="sxs-lookup"><span data-stu-id="9838e-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="9838e-110">*lpSubKey* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9838e-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9838e-111">O nome da chave a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="9838e-111">The name of the key to be deleted.</span></span> <span data-ttu-id="9838e-112">Ele deve ser uma subchave da chave que o *identificador* identifica, mas não pode ter subchaves.</span><span class="sxs-lookup"><span data-stu-id="9838e-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="9838e-113">Se a subchave não existir, a função retornará o erro \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="9838e-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="9838e-114">Se esse parâmetro for **NULL**, a função excluirá a chave especificada pelo parâmetro *Handle* .</span><span class="sxs-lookup"><span data-stu-id="9838e-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="9838e-115">Se a chave especificada pelo parâmetro *Handle* for a chave raiz do hive, a função retornará um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="9838e-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="9838e-116">Os nomes de chave não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9838e-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9838e-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9838e-117">Return value</span></span>

<span data-ttu-id="9838e-118">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="9838e-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="9838e-119">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9838e-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="9838e-120">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="9838e-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="9838e-121">Os códigos de erro possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9838e-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="9838e-122">Se a subchave especificada não existir, a função retornará o \_ arquivo de erro \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="9838e-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="9838e-123">Se a subchave especificada for a chave raiz do hive do registro, a função retornará um parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="9838e-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="9838e-124">Se a subchave especificada tiver subchaves, a função retornará a chave de erro \_ \_ tem \_ filhos.</span><span class="sxs-lookup"><span data-stu-id="9838e-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="9838e-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="9838e-125">Remarks</span></span>

<span data-ttu-id="9838e-126">Se a chave do Registro especificada existir, ela será marcada como excluída.</span><span class="sxs-lookup"><span data-stu-id="9838e-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="9838e-127">Uma chave excluída não é removida até que o último identificador seja fechado.</span><span class="sxs-lookup"><span data-stu-id="9838e-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="9838e-128">A chave a ser excluída não deve ter subchaves.</span><span class="sxs-lookup"><span data-stu-id="9838e-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="9838e-129">Para excluir uma chave e todas as suas subchaves, use a função [**OREnumKey**](orenumkey.md) para enumerar as subchaves e excluí-las individualmente.</span><span class="sxs-lookup"><span data-stu-id="9838e-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="9838e-130">Somente a função [**ORCloseKey**](orclosekey.md) pode ser chamada em uma chave excluída; todas as outras operações de registro offline falham.</span><span class="sxs-lookup"><span data-stu-id="9838e-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="9838e-131">Se a chave excluída tiver sido explicitamente criada chamando [**ORCreateKey**](orcreatekey.md), os recursos associados à chave serão liberados quando o último identificador da chave excluída for fechado.</span><span class="sxs-lookup"><span data-stu-id="9838e-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9838e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9838e-132">Requirements</span></span>



| <span data-ttu-id="9838e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9838e-133">Requirement</span></span> | <span data-ttu-id="9838e-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9838e-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9838e-135">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="9838e-135">Redistributable</span></span><br/> | <span data-ttu-id="9838e-136">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9838e-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="9838e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9838e-137">Header</span></span><br/>          | <dl> <span data-ttu-id="9838e-138"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9838e-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9838e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9838e-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="9838e-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9838e-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9838e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="9838e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9838e-142">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="9838e-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="9838e-143">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="9838e-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="9838e-144">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="9838e-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="9838e-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="9838e-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
