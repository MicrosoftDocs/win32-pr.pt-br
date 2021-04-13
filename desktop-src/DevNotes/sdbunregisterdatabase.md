---
description: Cancela o registro do banco de dados especificado, tornando-o não mais disponível.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Função SdbUnregisterDatabase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456974"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="42a76-103">Função SdbUnregisterDatabase</span><span class="sxs-lookup"><span data-stu-id="42a76-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="42a76-104">Cancela o registro do banco de dados especificado, tornando-o não mais disponível.</span><span class="sxs-lookup"><span data-stu-id="42a76-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a76-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42a76-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="42a76-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42a76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a76-107">*pguidDB* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="42a76-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a76-108">O GUID do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="42a76-108">The GUID of the database.</span></span> <span data-ttu-id="42a76-109">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="42a76-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a76-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42a76-110">Return value</span></span>

<span data-ttu-id="42a76-111">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="42a76-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a76-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a76-112">Requirements</span></span>



| <span data-ttu-id="42a76-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a76-113">Requirement</span></span> | <span data-ttu-id="42a76-114">Valor</span><span class="sxs-lookup"><span data-stu-id="42a76-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42a76-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a76-115">Minimum supported client</span></span><br/> | <span data-ttu-id="42a76-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42a76-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="42a76-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a76-117">Minimum supported server</span></span><br/> | <span data-ttu-id="42a76-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42a76-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="42a76-119">DLL</span><span class="sxs-lookup"><span data-stu-id="42a76-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42a76-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a76-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a76-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="42a76-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a76-122">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="42a76-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




