---
description: Determina se o Terminal Server está no modo de instalação.
ms.assetid: edf362e6-c1a4-49fe-8e07-1188c66616be
title: Função TermsrvAppInstallMode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TermsrvAppInstallMode
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: f80e51dc417cd637b2abaf8d5dfdc5c0d00f6578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751124"
---
# <a name="termsrvappinstallmode-function"></a><span data-ttu-id="a33f1-103">Função TermsrvAppInstallMode</span><span class="sxs-lookup"><span data-stu-id="a33f1-103">TermsrvAppInstallMode function</span></span>

<span data-ttu-id="a33f1-104">\[Essa função não tem suporte e não deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="a33f1-104">\[This function is not supported and should not be used.</span></span> <span data-ttu-id="a33f1-105">Ele pode mudar ou desaparecer completamente sem aviso prévio.\]</span><span class="sxs-lookup"><span data-stu-id="a33f1-105">It may change or disappear completely without advance notice.\]</span></span>

<span data-ttu-id="a33f1-106">Determina se o Terminal Server está no modo de instalação.</span><span class="sxs-lookup"><span data-stu-id="a33f1-106">Determines whether the Terminal Server is in the INSTALL mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a33f1-107">Syntax</span></span>


```C++
BOOL TermsrvAppInstallMode(void);
```



## <a name="parameters"></a><span data-ttu-id="a33f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a33f1-108">Parameters</span></span>

<span data-ttu-id="a33f1-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a33f1-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a33f1-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a33f1-110">Return value</span></span>

<span data-ttu-id="a33f1-111">Essa função retornará **true** se o Terminal Server estiver no modo de instalação e **false** se estiver no modo de execução.</span><span class="sxs-lookup"><span data-stu-id="a33f1-111">This function returns **TRUE** if the Terminal Server is in INSTALL mode and **FALSE** if it is in EXECUTE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="a33f1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a33f1-112">Requirements</span></span>



| <span data-ttu-id="a33f1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a33f1-113">Requirement</span></span> | <span data-ttu-id="a33f1-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a33f1-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a33f1-115">DLL</span><span class="sxs-lookup"><span data-stu-id="a33f1-115">DLL</span></span><br/> | <dl> <span data-ttu-id="a33f1-116"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a33f1-116"><dt>Kernel32.dll</dt></span></span> </dl> |



 

 




