---
title: Estrutura WMFILECAPABILITIES
description: A estrutura WMFILECAPABILITIES descreve o tipo MIME.
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- Estrutura WMFILECAPABILITIES Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781290"
---
# <a name="wmfilecapabilities-structure"></a><span data-ttu-id="85f3f-104">Estrutura WMFILECAPABILITIES</span><span class="sxs-lookup"><span data-stu-id="85f3f-104">WMFILECAPABILITIES structure</span></span>

<span data-ttu-id="85f3f-105">A estrutura **WMFILECAPABILITIES** descreve o tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="85f3f-105">The **WMFILECAPABILITIES** structure describes the MIME type.</span></span>

## <a name="syntax"></a><span data-ttu-id="85f3f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="85f3f-106">Syntax</span></span>


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a><span data-ttu-id="85f3f-107">Membros</span><span class="sxs-lookup"><span data-stu-id="85f3f-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="85f3f-108">**pwszMimeType**</span><span class="sxs-lookup"><span data-stu-id="85f3f-108">**pwszMimeType**</span></span>
</dt> <dd>

<span data-ttu-id="85f3f-109">Tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="85f3f-109">MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="85f3f-110">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="85f3f-110">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="85f3f-111">**DWORD** reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="85f3f-111">**DWORD** reserved for future use.</span></span> <span data-ttu-id="85f3f-112">Defina como zero (0).</span><span class="sxs-lookup"><span data-stu-id="85f3f-112">Set to zero (0).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85f3f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85f3f-113">Requirements</span></span>



| <span data-ttu-id="85f3f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="85f3f-114">Requirement</span></span> | <span data-ttu-id="85f3f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="85f3f-115">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="85f3f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85f3f-116">Header</span></span><br/> | <dl> <span data-ttu-id="85f3f-117"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85f3f-117"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85f3f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="85f3f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85f3f-119">**IWMDMDevice2::GetFormatSupport2**</span><span class="sxs-lookup"><span data-stu-id="85f3f-119">**IWMDMDevice2::GetFormatSupport2**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[<span data-ttu-id="85f3f-120">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="85f3f-120">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





