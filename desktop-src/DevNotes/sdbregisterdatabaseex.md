---
description: Registra o banco de dados especificado.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Função SdbRegisterDatabaseEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500873"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="8cf33-103">Função SdbRegisterDatabaseEx</span><span class="sxs-lookup"><span data-stu-id="8cf33-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="8cf33-104">Registra o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="8cf33-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf33-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8cf33-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="8cf33-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cf33-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf33-107">*pszDatabasePath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cf33-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf33-108">O caminho do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8cf33-108">The database path.</span></span> <span data-ttu-id="8cf33-109">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8cf33-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8cf33-110">*dwDatabaseType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8cf33-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf33-111">O tipo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8cf33-111">The database type.</span></span> <span data-ttu-id="8cf33-112">Consulte [Shim de tipos de banco de dados](shim-database-types.md) para obter uma lista de valores.</span><span class="sxs-lookup"><span data-stu-id="8cf33-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="8cf33-113">*pTimeStamp* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8cf33-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf33-114">O carimbo de data/hora do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="8cf33-114">The time stamp for the database.</span></span> <span data-ttu-id="8cf33-115">Se esse parâmetro for **NULL**, a hora do sistema será usada.</span><span class="sxs-lookup"><span data-stu-id="8cf33-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf33-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cf33-116">Return value</span></span>

<span data-ttu-id="8cf33-117">A função retorna **true** em caso de êxito ou **false** em caso de falha.</span><span class="sxs-lookup"><span data-stu-id="8cf33-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cf33-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cf33-118">Remarks</span></span>

<span data-ttu-id="8cf33-119">Um banco de dados deve ser registrado antes que você possa usar outras funções SDB.</span><span class="sxs-lookup"><span data-stu-id="8cf33-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf33-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cf33-120">Requirements</span></span>



| <span data-ttu-id="8cf33-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cf33-121">Requirement</span></span> | <span data-ttu-id="8cf33-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8cf33-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf33-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cf33-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf33-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8cf33-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8cf33-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cf33-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf33-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cf33-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8cf33-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8cf33-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cf33-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cf33-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cf33-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cf33-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf33-130">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="8cf33-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 




