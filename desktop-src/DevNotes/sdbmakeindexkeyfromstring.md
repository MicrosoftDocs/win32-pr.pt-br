---
description: Cria uma chave a partir de uma cadeia de caracteres.
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: Função SdbMakeIndexKeyFromString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920100"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="382e0-103">Função SdbMakeIndexKeyFromString</span><span class="sxs-lookup"><span data-stu-id="382e0-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="382e0-104">Cria uma chave a partir de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="382e0-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="382e0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="382e0-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="382e0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="382e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="382e0-107">*pwszKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="382e0-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="382e0-108">A cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="382e0-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="382e0-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="382e0-109">Return value</span></span>

<span data-ttu-id="382e0-110">A função retornará a chave ou 0 se houver um erro.</span><span class="sxs-lookup"><span data-stu-id="382e0-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="382e0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="382e0-111">Remarks</span></span>

<span data-ttu-id="382e0-112">A chave de índice padrão são os oito primeiros caracteres da cadeia de caracteres, convertidos em letras maiúsculas e, em seguida, convertidos em um valor de **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="382e0-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="382e0-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="382e0-113">Requirements</span></span>



| <span data-ttu-id="382e0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="382e0-114">Requirement</span></span> | <span data-ttu-id="382e0-115">Valor</span><span class="sxs-lookup"><span data-stu-id="382e0-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="382e0-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="382e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="382e0-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="382e0-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="382e0-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="382e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="382e0-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="382e0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="382e0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="382e0-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="382e0-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="382e0-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




