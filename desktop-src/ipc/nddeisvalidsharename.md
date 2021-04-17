---
description: Determina se um nome de compartilhamento usa a sintaxe apropriada.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Função NDdeIsValidShareName (Nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780211"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="498fd-103">Função NDdeIsValidShareName</span><span class="sxs-lookup"><span data-stu-id="498fd-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="498fd-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="498fd-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="498fd-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="498fd-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="498fd-106">Determina se um nome de compartilhamento usa a sintaxe apropriada.</span><span class="sxs-lookup"><span data-stu-id="498fd-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="498fd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="498fd-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="498fd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="498fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="498fd-109">*ShareName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="498fd-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="498fd-110">O nome do compartilhamento a ser validado.</span><span class="sxs-lookup"><span data-stu-id="498fd-110">The share name to be validated.</span></span> <span data-ttu-id="498fd-111">Este parâmetro não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="498fd-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="498fd-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="498fd-112">Return value</span></span>

<span data-ttu-id="498fd-113">Se o nome do compartilhamento tiver uma sintaxe válida, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="498fd-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="498fd-114">Se o nome do compartilhamento não tiver uma sintaxe válida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="498fd-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="498fd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="498fd-115">Remarks</span></span>

<span data-ttu-id="498fd-116">Essa função também é chamada por [**NDdeShareAdd**](nddeshareadd.md) quando cria o compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="498fd-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="498fd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="498fd-117">Requirements</span></span>



| <span data-ttu-id="498fd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="498fd-118">Requirement</span></span> | <span data-ttu-id="498fd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="498fd-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="498fd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="498fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="498fd-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="498fd-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="498fd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="498fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="498fd-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="498fd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="498fd-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="498fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="498fd-125"><dt>Nddeapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="498fd-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="498fd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="498fd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="498fd-127"><dt>Nddeapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="498fd-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="498fd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="498fd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="498fd-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="498fd-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="498fd-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="498fd-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="498fd-131">**NDdeIsValidShareNameW** (Unicode) e **NDdeIsValidShareNameA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="498fd-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="498fd-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="498fd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="498fd-133">Visão geral de troca dinâmica de dados de rede</span><span class="sxs-lookup"><span data-stu-id="498fd-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="498fd-134">Funções DDE de rede</span><span class="sxs-lookup"><span data-stu-id="498fd-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="498fd-135">**NDdeShareAdd**</span><span class="sxs-lookup"><span data-stu-id="498fd-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




