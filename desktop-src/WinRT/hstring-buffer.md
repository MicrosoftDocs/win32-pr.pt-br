---
description: Um identificador para um buffer de cadeia de caracteres mutável que você pode usar para criar um HSTRING.
ms.assetid: D173CE70-ABF3-4703-A229-0753F2AF6F70
title: HSTRING_BUFFER (hstring. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d70b961d442739e084e3b17d5666653c103cc35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783734"
---
# <a name="hstring_buffer"></a><span data-ttu-id="a0f22-103">\_buffer HSTRING</span><span class="sxs-lookup"><span data-stu-id="a0f22-103">HSTRING\_BUFFER</span></span>

<span data-ttu-id="a0f22-104">Um identificador para um buffer de cadeia de caracteres mutável que você pode usar para criar um [**HSTRING**](hstring.md).</span><span class="sxs-lookup"><span data-stu-id="a0f22-104">A handle to a mutable string buffer that you can use to create an [**HSTRING**](hstring.md).</span></span>


```C++
typedef HANDLE HSTRING_BUFFER;
```



## <a name="remarks"></a><span data-ttu-id="a0f22-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0f22-105">Remarks</span></span>

<span data-ttu-id="a0f22-106">**HSTRING \_ BUFFER** representa um buffer de cadeia de caracteres que você pode modificar antes de convertê-lo em um [**HSTRING**](hstring.md)imutável.</span><span class="sxs-lookup"><span data-stu-id="a0f22-106">**HSTRING\_BUFFER** represents a string buffer that you can modify before converting it to an immutable [**HSTRING**](hstring.md).</span></span>

<span data-ttu-id="a0f22-107">Chame a função [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) para criar um **\_ buffer HSTRING**.</span><span class="sxs-lookup"><span data-stu-id="a0f22-107">Call the [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) function to create an **HSTRING\_BUFFER**.</span></span> <span data-ttu-id="a0f22-108">Chame o [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) para converter um **\_ buffer HSTRING** em uma [**HSTRING**](hstring.md)imutável.</span><span class="sxs-lookup"><span data-stu-id="a0f22-108">Call the [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) to convert an **HSTRING\_BUFFER** to an immutable [**HSTRING**](hstring.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0f22-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0f22-109">Requirements</span></span>



| <span data-ttu-id="a0f22-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f22-110">Requirement</span></span> | <span data-ttu-id="a0f22-111">Valor</span><span class="sxs-lookup"><span data-stu-id="a0f22-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f22-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0f22-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a0f22-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0f22-113">Windows 8</span></span><br/>                                                                 |
| <span data-ttu-id="a0f22-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0f22-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a0f22-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0f22-115">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="a0f22-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0f22-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0f22-117"><dt>Hstring. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0f22-117"><dt>Hstring.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f22-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0f22-118">See also</span></span>

<dl> <span data-ttu-id="a0f22-119"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="a0f22-119"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="a0f22-120">**HSTRING**</span><span class="sxs-lookup"><span data-stu-id="a0f22-120">**HSTRING**</span></span>](hstring.md)
</dt> <dt>

[<span data-ttu-id="a0f22-121">**WindowsPreallocateStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="a0f22-121">**WindowsPreallocateStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer)
</dt> <dt>

[<span data-ttu-id="a0f22-122">**WindowsPromoteStringBuffer**</span><span class="sxs-lookup"><span data-stu-id="a0f22-122">**WindowsPromoteStringBuffer**</span></span>](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer)
</dt> </dl>

 

 
