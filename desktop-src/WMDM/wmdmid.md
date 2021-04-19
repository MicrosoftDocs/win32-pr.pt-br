---
title: Estrutura WMDMID
description: A estrutura WMDMID descreve os números de série e as IDs de grupo.
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- Estrutura WMDMID Windows Media Gerenciador de Dispositivos
- Ponteiro de estrutura PWMDMID Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781469"
---
# <a name="wmdmid-structure"></a><span data-ttu-id="10ac3-105">Estrutura WMDMID</span><span class="sxs-lookup"><span data-stu-id="10ac3-105">WMDMID structure</span></span>

<span data-ttu-id="10ac3-106">A estrutura **WMDMID** descreve os números de série e as IDs de grupo.</span><span class="sxs-lookup"><span data-stu-id="10ac3-106">The **WMDMID** structure describes serial numbers and group IDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="10ac3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10ac3-107">Syntax</span></span>


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a><span data-ttu-id="10ac3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="10ac3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="10ac3-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="10ac3-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="10ac3-110">Tamanho da estrutura **WMDMID** , em bytes.</span><span class="sxs-lookup"><span data-stu-id="10ac3-110">Size of the **WMDMID** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="10ac3-111">**dwVendorID**</span><span class="sxs-lookup"><span data-stu-id="10ac3-111">**dwVendorID**</span></span>
</dt> <dd>

<span data-ttu-id="10ac3-112">**DWORD** que contém o número de ID registrado do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="10ac3-112">**DWORD** containing the registered ID number of the vendor.</span></span> <span data-ttu-id="10ac3-113">Contém zero se não estiver em uso.</span><span class="sxs-lookup"><span data-stu-id="10ac3-113">Contains zero if not in use.</span></span>

</dd> <dt>

<span data-ttu-id="10ac3-114">**\[comprimento de WMDMID pID \_\]**</span><span class="sxs-lookup"><span data-stu-id="10ac3-114">**pID\[WMDMID\_LENGTH\]**</span></span>
</dt> <dd>

<span data-ttu-id="10ac3-115">Ponteiro para uma matriz de bytes que contém o número de série.</span><span class="sxs-lookup"><span data-stu-id="10ac3-115">Pointer to an array of bytes containing the serial number.</span></span> <span data-ttu-id="10ac3-116">O número de série é uma cadeia de caracteres de valores de bytes que não têm nenhum formato padrão.</span><span class="sxs-lookup"><span data-stu-id="10ac3-116">The serial number is a string of byte values that have no standard format.</span></span> <span data-ttu-id="10ac3-117">Observe que esse não é um valor de caractere largo.</span><span class="sxs-lookup"><span data-stu-id="10ac3-117">Note that this is not a wide-character value.</span></span> <span data-ttu-id="10ac3-118">**WMDMID \_ LENGTH** é um valor constante definido em mswmdm. h.</span><span class="sxs-lookup"><span data-stu-id="10ac3-118">**WMDMID\_LENGTH** is a constant value defined in mswmdm.h.</span></span>

</dd> <dt>

<span data-ttu-id="10ac3-119">**SerialNumberLength**</span><span class="sxs-lookup"><span data-stu-id="10ac3-119">**SerialNumberLength**</span></span>
</dt> <dd>

<span data-ttu-id="10ac3-120">Comprimento real do número de série retornado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="10ac3-120">Actual length of the serial number returned, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10ac3-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10ac3-121">Requirements</span></span>



| <span data-ttu-id="10ac3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="10ac3-122">Requirement</span></span> | <span data-ttu-id="10ac3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="10ac3-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="10ac3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10ac3-124">Header</span></span><br/> | <dl> <span data-ttu-id="10ac3-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="10ac3-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10ac3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="10ac3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10ac3-127">**IMDSPDevice:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="10ac3-127">**IMDSPDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="10ac3-128">**IMDSPStorageGlobals:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="10ac3-128">**IMDSPStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="10ac3-129">**IWMDMDevice:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="10ac3-129">**IWMDMDevice::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[<span data-ttu-id="10ac3-130">**IWMDMStorageGlobals:: GetSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="10ac3-130">**IWMDMStorageGlobals::GetSerialNumber**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[<span data-ttu-id="10ac3-131">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="10ac3-131">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





