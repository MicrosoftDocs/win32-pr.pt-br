---
description: Especifica atributos para uma assinatura Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Estrutura de SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922879"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="62805-103">\_Estrutura de fatores attr de signatário \_</span><span class="sxs-lookup"><span data-stu-id="62805-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="62805-104">A **estrutura \_ \_ fatores attr de signatário** especifica atributos para uma assinatura [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="62805-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="62805-105">Essa estrutura não está definida em nenhum arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="62805-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="62805-106">Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.</span><span class="sxs-lookup"><span data-stu-id="62805-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="62805-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62805-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="62805-108">Membros</span><span class="sxs-lookup"><span data-stu-id="62805-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="62805-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="62805-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="62805-110">O tamanho, em bytes, da estrutura.</span><span class="sxs-lookup"><span data-stu-id="62805-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="62805-111">**fCommercial**</span><span class="sxs-lookup"><span data-stu-id="62805-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="62805-112">**True** para assinar o assunto como um editor comercial; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="62805-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62805-113">**fIndividual**</span><span class="sxs-lookup"><span data-stu-id="62805-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="62805-114">**True** para assinar o assunto como um Publicador individual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="62805-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62805-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="62805-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="62805-116">O nome de exibição do arquivo no download.</span><span class="sxs-lookup"><span data-stu-id="62805-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="62805-117">**pwszInfo**</span><span class="sxs-lookup"><span data-stu-id="62805-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="62805-118">O nome de exibição da URL do arquivo durante o download.</span><span class="sxs-lookup"><span data-stu-id="62805-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62805-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62805-119">Requirements</span></span>



| <span data-ttu-id="62805-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62805-120">Requirement</span></span> | <span data-ttu-id="62805-121">Valor</span><span class="sxs-lookup"><span data-stu-id="62805-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62805-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62805-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62805-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="62805-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="62805-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62805-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62805-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62805-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62805-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="62805-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62805-127">**\_informações de assinatura do assinante \_**</span><span class="sxs-lookup"><span data-stu-id="62805-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
