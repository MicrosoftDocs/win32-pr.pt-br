---
description: O método GetMaximumCursors recupera o número máximo de cursores que um dispositivo de Tablet dá suporte.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'Método ITablet3:: GetMaximumCursors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788783"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="c2dc5-103">Método ITablet3:: GetMaximumCursors</span><span class="sxs-lookup"><span data-stu-id="c2dc5-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="c2dc5-104">O método **GetMaximumCursors** recupera o número máximo de cursores que um dispositivo de Tablet dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c2dc5-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2dc5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2dc5-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="c2dc5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2dc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2dc5-107">*pMaximumCursors*</span><span class="sxs-lookup"><span data-stu-id="c2dc5-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="c2dc5-108">O número máximo de entradas que o dispositivo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c2dc5-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2dc5-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2dc5-109">Return value</span></span>

<span data-ttu-id="c2dc5-110">Retorna S \_ OK em caso de êxito; caso contrário, retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="c2dc5-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2dc5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2dc5-111">Requirements</span></span>



| <span data-ttu-id="c2dc5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2dc5-112">Requirement</span></span> | <span data-ttu-id="c2dc5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c2dc5-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dc5-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2dc5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c2dc5-115">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c2dc5-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c2dc5-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2dc5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c2dc5-117">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="c2dc5-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c2dc5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2dc5-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2dc5-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c2dc5-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2dc5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2dc5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2dc5-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="c2dc5-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




