---
title: Função MB_GetString (User. h)
description: Retorna cadeias de caracteres para botões de caixa de mensagem padrão.
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Caixas de diálogo MB_GetString função
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813321"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="89526-104">\_Função GetString de MB</span><span class="sxs-lookup"><span data-stu-id="89526-104">MB\_GetString function</span></span>

<span data-ttu-id="89526-105">Retorna cadeias de caracteres para botões de caixa de mensagem padrão.</span><span class="sxs-lookup"><span data-stu-id="89526-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="89526-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89526-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="89526-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89526-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89526-108">*wBtn*</span><span class="sxs-lookup"><span data-stu-id="89526-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="89526-109">A ID da cadeia de caracteres a ser retornada.</span><span class="sxs-lookup"><span data-stu-id="89526-109">The id of the string to return.</span></span> <span data-ttu-id="89526-110">Eles são identificados pelos valores de ID de comando da caixa de diálogo listados em winuser. h.</span><span class="sxs-lookup"><span data-stu-id="89526-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89526-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89526-111">Return value</span></span>

<span data-ttu-id="89526-112">A cadeia de caracteres ou NULL se não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="89526-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="89526-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89526-113">Requirements</span></span>



| <span data-ttu-id="89526-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="89526-114">Requirement</span></span> | <span data-ttu-id="89526-115">Valor</span><span class="sxs-lookup"><span data-stu-id="89526-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89526-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89526-116">Header</span></span><br/>  | <dl> <span data-ttu-id="89526-117"><dt>User. h</dt></span><span class="sxs-lookup"><span data-stu-id="89526-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="89526-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89526-118">Library</span></span><br/> | <dl> <span data-ttu-id="89526-119"><dt>User32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89526-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="89526-120">DLL</span><span class="sxs-lookup"><span data-stu-id="89526-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="89526-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89526-121"><dt>User32.dll</dt></span></span> </dl> |



 

 





