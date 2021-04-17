---
description: Recarrega as configurações de cor do registro.
ms.assetid: 1F2EE08A-4193-4F0C-BE4F-0551FA71CFA8
title: Função FRefreshStyle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRefreshStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 098e79ab49373dc115189a2c47dc3604fba10ef9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752323"
---
# <a name="frefreshstyle-function"></a><span data-ttu-id="c8a93-103">Função FRefreshStyle</span><span class="sxs-lookup"><span data-stu-id="c8a93-103">FRefreshStyle function</span></span>

<span data-ttu-id="c8a93-104">Recarrega as configurações de cor do registro.</span><span class="sxs-lookup"><span data-stu-id="c8a93-104">Reloads color settings from registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8a93-105">Syntax</span></span>


```C++
BOOL __cdecl FRefreshStyle(void);
```



## <a name="parameters"></a><span data-ttu-id="c8a93-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8a93-106">Parameters</span></span>

<span data-ttu-id="c8a93-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c8a93-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8a93-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c8a93-108">Return value</span></span>

<span data-ttu-id="c8a93-109">Retorna verdadeiro em caso de êxito; caso contrário, FALSE.</span><span class="sxs-lookup"><span data-stu-id="c8a93-109">Returns TRUE on success; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8a93-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8a93-110">Remarks</span></span>

<span data-ttu-id="c8a93-111">Esta função não está associada a uma biblioteca de importação ou arquivo de cabeçalho; Ele deve ser chamado usando as funções [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) .</span><span class="sxs-lookup"><span data-stu-id="c8a93-111">This function is not associated with an import library or header file; it must be called using the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a93-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8a93-112">Requirements</span></span>



| <span data-ttu-id="c8a93-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a93-113">Requirement</span></span> | <span data-ttu-id="c8a93-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c8a93-114">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a93-115">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a93-115">DLL</span></span><br/> | <dl> <span data-ttu-id="c8a93-116"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a93-116"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a93-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8a93-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a93-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="c8a93-118">**GetProcAddress**</span></span>](-getprocaddress-.md)
</dt> <dt>

[<span data-ttu-id="c8a93-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="c8a93-119">**LoadLibrary**</span></span>](-loadlibrary.md)
</dt> </dl>

 

 




