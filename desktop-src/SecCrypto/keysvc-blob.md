---
description: A \_ estrutura de blob KEYSVC define um blob de serviço de chave. Essa estrutura é usada pela função RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Estrutura de KEYSVC_BLOB (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769279"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="0cfd6-104">\_Estrutura de blob KEYSVC</span><span class="sxs-lookup"><span data-stu-id="0cfd6-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="0cfd6-105">A estrutura de **\_ blob KEYSVC** define um blob de serviço de chave.</span><span class="sxs-lookup"><span data-stu-id="0cfd6-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="0cfd6-106">Essa estrutura é usada pela função [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="0cfd6-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfd6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cfd6-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="0cfd6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0cfd6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0cfd6-109">**CB**</span><span class="sxs-lookup"><span data-stu-id="0cfd6-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="0cfd6-110">Um valor **ULONG** que especifica o tamanho, em bytes, de **PB**.</span><span class="sxs-lookup"><span data-stu-id="0cfd6-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="0cfd6-111">**PB**</span><span class="sxs-lookup"><span data-stu-id="0cfd6-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="0cfd6-112">Um ponteiro para um **byte** que contém o blob, no formato [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0cfd6-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0cfd6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cfd6-113">Requirements</span></span>



| <span data-ttu-id="0cfd6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cfd6-114">Requirement</span></span> | <span data-ttu-id="0cfd6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0cfd6-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfd6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cfd6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfd6-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0cfd6-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="0cfd6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0cfd6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfd6-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0cfd6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0cfd6-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cfd6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cfd6-121"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfd6-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cfd6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0cfd6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfd6-123">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="0cfd6-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="0cfd6-124">**\_cadeia de \_ caracteres Unicode KEYSVC**</span><span class="sxs-lookup"><span data-stu-id="0cfd6-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
