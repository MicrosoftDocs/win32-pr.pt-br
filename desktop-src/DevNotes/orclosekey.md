---
description: Fecha um identificador para a chave do Registro especificada em um hive do registro offline.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Função ORCloseKey (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754907"
---
# <a name="orclosekey-function"></a><span data-ttu-id="21993-103">Função ORCloseKey</span><span class="sxs-lookup"><span data-stu-id="21993-103">ORCloseKey function</span></span>

<span data-ttu-id="21993-104">Fecha um identificador para a chave do Registro especificada em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="21993-104">Closes a handle to the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="21993-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21993-105">Syntax</span></span>


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="21993-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21993-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21993-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="21993-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21993-108">Um identificador para uma chave do registro aberta em um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="21993-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21993-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21993-109">Return value</span></span>

<span data-ttu-id="21993-110">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="21993-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="21993-111">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="21993-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="21993-112">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="21993-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="21993-113">Se a chave especificada for a chave raiz do hive do registro, a função falhará com o parâmetro de erro \_ inválido \_ .</span><span class="sxs-lookup"><span data-stu-id="21993-113">If the specified key is the root key of the registry hive, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="21993-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="21993-114">Remarks</span></span>

<span data-ttu-id="21993-115">O identificador de uma chave especificada não deve ser usado depois de ser fechado, pois ele não será mais válido.</span><span class="sxs-lookup"><span data-stu-id="21993-115">The handle for a specified key should not be used after it has been closed, because it will no longer be valid.</span></span> <span data-ttu-id="21993-116">Os identificadores de chave não devem ser deixados abertos mais do que o necessário.</span><span class="sxs-lookup"><span data-stu-id="21993-116">Key handles should not be left open any longer than necessary.</span></span>

<span data-ttu-id="21993-117">Use a função [**ORCloseHive**](orclosehive.md) para fechar um hive do registro offline.</span><span class="sxs-lookup"><span data-stu-id="21993-117">Use the [**ORCloseHive**](orclosehive.md) function to close an offline registry hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="21993-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21993-118">Requirements</span></span>



| <span data-ttu-id="21993-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="21993-119">Requirement</span></span> | <span data-ttu-id="21993-120">Valor</span><span class="sxs-lookup"><span data-stu-id="21993-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21993-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="21993-121">Redistributable</span></span><br/> | <span data-ttu-id="21993-122">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="21993-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="21993-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21993-123">Header</span></span><br/>          | <dl> <span data-ttu-id="21993-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="21993-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="21993-125">DLL</span><span class="sxs-lookup"><span data-stu-id="21993-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="21993-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21993-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21993-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="21993-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21993-128">**ORCloseHive**</span><span class="sxs-lookup"><span data-stu-id="21993-128">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="21993-129">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="21993-129">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="21993-130">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="21993-130">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="21993-131">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="21993-131">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
