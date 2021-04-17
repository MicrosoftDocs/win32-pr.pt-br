---
description: A \_ estrutura de cadeia de caracteres Unicode KEYSVC \_ define uma cadeia de caracteres Unicode e um comprimento máximo para a cadeia de caracteres. Essa estrutura é usada pela função RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Estrutura de KEYSVC_UNICODE_STRING (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782948"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="4a996-104">\_Estrutura de \_ cadeia de caracteres Unicode KEYSVC</span><span class="sxs-lookup"><span data-stu-id="4a996-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="4a996-105">A estrutura de **\_ cadeia de \_ caracteres Unicode KEYSVC** define uma cadeia de caracteres [*Unicode*](../secgloss/u-gly.md) e um comprimento máximo para a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="4a996-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="4a996-106">Essa estrutura é usada pela função [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="4a996-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a996-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a996-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="4a996-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4a996-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4a996-109">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="4a996-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="4a996-110">Um valor **UShort** que especifica o comprimento, em bytes, usado para o **buffer**.</span><span class="sxs-lookup"><span data-stu-id="4a996-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="4a996-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="4a996-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="4a996-112">Um valor **UShort** que especifica o comprimento máximo, em bytes, permitido para o **buffer**.</span><span class="sxs-lookup"><span data-stu-id="4a996-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="4a996-113">**Buffer**</span><span class="sxs-lookup"><span data-stu-id="4a996-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="4a996-114">Um ponteiro para um **UShort** que representa a cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="4a996-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a996-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a996-115">Requirements</span></span>



| <span data-ttu-id="4a996-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a996-116">Requirement</span></span> | <span data-ttu-id="4a996-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4a996-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4a996-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a996-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a996-119">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4a996-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="4a996-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a996-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a996-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4a996-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4a996-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a996-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a996-123"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a996-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a996-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a996-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a996-125">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="4a996-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="4a996-126">**\_blob KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="4a996-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
