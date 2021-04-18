---
description: Contém um BLOB assinado.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: Estrutura de SIGNER_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764612"
---
# <a name="signer_context-structure"></a><span data-ttu-id="b4fd0-103">Estrutura de contexto do signatário \_</span><span class="sxs-lookup"><span data-stu-id="b4fd0-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="b4fd0-104">A estrutura de **\_ contexto do signatário** contém um [*blob*](../secgloss/b-gly.md)assinado.</span><span class="sxs-lookup"><span data-stu-id="b4fd0-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="b4fd0-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="b4fd0-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="b4fd0-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b4fd0-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b4fd0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4fd0-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="b4fd0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b4fd0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b4fd0-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="b4fd0-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b4fd0-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="b4fd0-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="b4fd0-111">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="b4fd0-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="b4fd0-112">O tamanho, em bytes, do membro **pbBlob** .</span><span class="sxs-lookup"><span data-stu-id="b4fd0-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="b4fd0-113">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="b4fd0-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="b4fd0-114">Um ponteiro para o BLOB assinado.</span><span class="sxs-lookup"><span data-stu-id="b4fd0-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4fd0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4fd0-115">Requirements</span></span>



| <span data-ttu-id="b4fd0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4fd0-116">Requirement</span></span> | <span data-ttu-id="b4fd0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b4fd0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b4fd0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4fd0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b4fd0-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b4fd0-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b4fd0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4fd0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b4fd0-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4fd0-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b4fd0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4fd0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fd0-123">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="b4fd0-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="b4fd0-124">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="b4fd0-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
