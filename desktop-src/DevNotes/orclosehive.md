---
description: Fecha o hive do registro offline especificado e libera a memória alocada para o hive.
ms.assetid: e30a92dd-8533-406f-ad63-96306f125d78
title: Função ORCloseHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a7f018e2ccdb98de14f908224ade52d0cdf7819f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747877"
---
# <a name="orclosehive-function"></a><span data-ttu-id="76025-103">Função ORCloseHive</span><span class="sxs-lookup"><span data-stu-id="76025-103">ORCloseHive function</span></span>

<span data-ttu-id="76025-104">Fecha o hive do registro offline especificado e libera a memória alocada para o hive.</span><span class="sxs-lookup"><span data-stu-id="76025-104">Closes the specified offline registry hive and frees memory allocated for the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="76025-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76025-105">Syntax</span></span>


```C++
DWORD ORCloseHive(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a><span data-ttu-id="76025-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76025-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76025-107">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="76025-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76025-108">Um identificador para a chave raiz do hive do registro offline a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="76025-108">A handle to the root key of the offline registry hive to be closed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76025-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76025-109">Return value</span></span>

<span data-ttu-id="76025-110">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="76025-110">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="76025-111">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="76025-111">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="76025-112">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="76025-112">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="76025-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="76025-113">Remarks</span></span>

<span data-ttu-id="76025-114">A função **ORCloseHive** libera toda a memória alocada pelas funções de registro offline em nome do hive especificado.</span><span class="sxs-lookup"><span data-stu-id="76025-114">The **ORCloseHive** function frees all memory allocated by the offline registry functions on behalf of the specified hive.</span></span>

<span data-ttu-id="76025-115">Para preservar as alterações no hive, chame a função [**ORSaveHive**](orsavehive.md) antes de chamar **ORCloseHive**.</span><span class="sxs-lookup"><span data-stu-id="76025-115">To preserve changes to the hive, call the [**ORSaveHive**](orsavehive.md) function before calling **ORCloseHive**.</span></span>

## <a name="requirements"></a><span data-ttu-id="76025-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76025-116">Requirements</span></span>



| <span data-ttu-id="76025-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="76025-117">Requirement</span></span> | <span data-ttu-id="76025-118">Valor</span><span class="sxs-lookup"><span data-stu-id="76025-118">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76025-119">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="76025-119">Redistributable</span></span><br/> | <span data-ttu-id="76025-120">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="76025-120">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="76025-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76025-121">Header</span></span><br/>          | <dl> <span data-ttu-id="76025-122"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="76025-122"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="76025-123">DLL</span><span class="sxs-lookup"><span data-stu-id="76025-123">DLL</span></span><br/>             | <dl> <span data-ttu-id="76025-124"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76025-124"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76025-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="76025-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76025-126">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="76025-126">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="76025-127">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="76025-127">**ORSaveHive**</span></span>](orsavehive.md)
</dt> </dl>

 

 
