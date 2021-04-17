---
description: Essa função recupera a versão da biblioteca offline do registro.
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: Função ORGetVersion (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748688"
---
# <a name="orgetversion-function"></a><span data-ttu-id="10a2f-103">Função ORGetVersion</span><span class="sxs-lookup"><span data-stu-id="10a2f-103">ORGetVersion function</span></span>

<span data-ttu-id="10a2f-104">Essa função recupera a versão da biblioteca offline do registro.</span><span class="sxs-lookup"><span data-stu-id="10a2f-104">This function retrieves the version of the offline registry library.</span></span>

## <a name="syntax"></a><span data-ttu-id="10a2f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10a2f-105">Syntax</span></span>


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a><span data-ttu-id="10a2f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10a2f-107">*pdwMajorVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10a2f-107">*pdwMajorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10a2f-108">Um ponteiro para uma variável para receber a versão principal da biblioteca do registro offline.</span><span class="sxs-lookup"><span data-stu-id="10a2f-108">A pointer to a variable to receive the major version of the offline registry library.</span></span> <span data-ttu-id="10a2f-109">Para a versão inicial da biblioteca, o valor é 1.</span><span class="sxs-lookup"><span data-stu-id="10a2f-109">For the initial release of the library, the value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="10a2f-110">*pdwMinorVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10a2f-110">*pdwMinorVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10a2f-111">Um ponteiro para uma variável para receber a versão secundária da biblioteca do registro offline.</span><span class="sxs-lookup"><span data-stu-id="10a2f-111">A pointer to a variable to receive the minor version of the offline registry library.</span></span> <span data-ttu-id="10a2f-112">Para a versão inicial da biblioteca, o valor é 0.</span><span class="sxs-lookup"><span data-stu-id="10a2f-112">For the initial release of the library, the value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10a2f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10a2f-113">Return value</span></span>

<span data-ttu-id="10a2f-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="10a2f-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="10a2f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10a2f-115">Requirements</span></span>



| <span data-ttu-id="10a2f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="10a2f-116">Requirement</span></span> | <span data-ttu-id="10a2f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="10a2f-117">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10a2f-118">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="10a2f-118">Redistributable</span></span><br/> | <span data-ttu-id="10a2f-119">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="10a2f-119">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="10a2f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10a2f-120">Header</span></span><br/>          | <dl> <span data-ttu-id="10a2f-121"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="10a2f-121"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="10a2f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="10a2f-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="10a2f-123"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10a2f-123"><dt>Offreg.dll</dt></span></span> </dl> |



 

 




