---
description: Essa função habilita ou desabilita o suporte para EUDC (caracteres definidos pelo usuário final).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Função EnableEUDC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967670"
---
# <a name="enableeudc-function"></a><span data-ttu-id="3bb52-103">Função EnableEUDC</span><span class="sxs-lookup"><span data-stu-id="3bb52-103">EnableEUDC function</span></span>

<span data-ttu-id="3bb52-104">Essa função habilita ou desabilita o suporte para EUDC (caracteres definidos pelo usuário final).</span><span class="sxs-lookup"><span data-stu-id="3bb52-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb52-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bb52-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="3bb52-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bb52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb52-107">*fEnableEUDC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb52-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb52-108">Booliano que é definido como **true** para habilitar EUDC e **false** para desabilitar Eudc.</span><span class="sxs-lookup"><span data-stu-id="3bb52-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb52-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3bb52-109">Return value</span></span>

<span data-ttu-id="3bb52-110">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3bb52-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="3bb52-111">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="3bb52-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bb52-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bb52-112">Remarks</span></span>

<span data-ttu-id="3bb52-113">Se o EUDC estiver desabilitado, tentar exibir caracteres EUDC resultará em glifos ausentes ou inválidos.</span><span class="sxs-lookup"><span data-stu-id="3bb52-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="3bb52-114">Durante várias sessões, essa função afeta apenas a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="3bb52-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="3bb52-115">É recomendável que você use essa função com o Windows XP SP2 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3bb52-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb52-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bb52-116">Requirements</span></span>



| <span data-ttu-id="3bb52-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb52-117">Requirement</span></span> | <span data-ttu-id="3bb52-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3bb52-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb52-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bb52-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3bb52-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bb52-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3bb52-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bb52-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3bb52-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3bb52-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3bb52-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bb52-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="3bb52-124"><dt>GDI32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bb52-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3bb52-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3bb52-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bb52-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bb52-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 




