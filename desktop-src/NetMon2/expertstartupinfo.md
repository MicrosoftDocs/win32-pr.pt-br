---
description: Contém dados que descrevem um especialista quando ele é iniciado.
ms.assetid: 9ecd5395-d10c-411b-a6bd-fbac724d8603
title: Estrutura EXPERTSTARTUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTARTUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 627d47cec09a683f80c16374561899ab008d0596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920708"
---
# <a name="expertstartupinfo-structure"></a><span data-ttu-id="5c640-103">Estrutura EXPERTSTARTUPINFO</span><span class="sxs-lookup"><span data-stu-id="5c640-103">EXPERTSTARTUPINFO structure</span></span>

<span data-ttu-id="5c640-104">A estrutura **EXPERTSTARTUPINFO** contém dados que descrevem um especialista quando ele é iniciado.</span><span class="sxs-lookup"><span data-stu-id="5c640-104">The **EXPERTSTARTUPINFO** structure contains data that describes an expert when it starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c640-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c640-105">Syntax</span></span>


```C++
typedef struct _EXPERTSTARTUPINFO {
  DWORD          Flags;
  HCAPTURE       hCapture;
  char           szCaptureFile[MAX_PATH];
  DWORD          dwFrameNumber;
  HPROTOCOL      hProtocol;
  LPPROPERTYINST lpPropertyInst;
  struct {
    BYTE BitNumber;
    BOOL bOn;
  } sBitfield;
} EXPERTSTARTUPINFO, *PEXPERTSTARTUPINFO;
```



## <a name="members"></a><span data-ttu-id="5c640-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5c640-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c640-107">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="5c640-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-108">Sinalizadores que descrevem o especialista.</span><span class="sxs-lookup"><span data-stu-id="5c640-108">Flags that describe the expert.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-109">**hCapture**</span><span class="sxs-lookup"><span data-stu-id="5c640-109">**hCapture**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-110">Identificador para uma captura.</span><span class="sxs-lookup"><span data-stu-id="5c640-110">Handle to a capture.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-111">**szCaptureFile**</span><span class="sxs-lookup"><span data-stu-id="5c640-111">**szCaptureFile**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-112">Nome do arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="5c640-112">Name of the capture file.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-113">**dwFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="5c640-113">**dwFrameNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-114">Número do quadro.</span><span class="sxs-lookup"><span data-stu-id="5c640-114">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-115">**hProtocol**</span><span class="sxs-lookup"><span data-stu-id="5c640-115">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-116">Identificador para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="5c640-116">Handle to the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-117">**lpPropertyInst**</span><span class="sxs-lookup"><span data-stu-id="5c640-117">**lpPropertyInst**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-118">Ponteiro para uma estrutura [**PROPERTYINST**](propertyinst.md) .</span><span class="sxs-lookup"><span data-stu-id="5c640-118">Pointer to a [**PROPERTYINST**](propertyinst.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-119">**sBitfield**</span><span class="sxs-lookup"><span data-stu-id="5c640-119">**sBitfield**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c640-120">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="5c640-120">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-121">Usado somente se o membro **Dataqualificador** da estrutura [**PROPERTYINST**](propertyinst.md) estiver definido para os \_ sinalizadores prop igual \_ .</span><span class="sxs-lookup"><span data-stu-id="5c640-121">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> <dt>

<span data-ttu-id="5c640-122">**Bno**</span><span class="sxs-lookup"><span data-stu-id="5c640-122">**bOn**</span></span>
</dt> <dd>

<span data-ttu-id="5c640-123">Usado somente se o membro **Dataqualificador** da estrutura [**PROPERTYINST**](propertyinst.md) estiver definido para os \_ sinalizadores prop igual \_ .</span><span class="sxs-lookup"><span data-stu-id="5c640-123">Used only if the **DataQualifier** member of the [**PROPERTYINST**](propertyinst.md) structure is set to PROP\_QUAL\_FLAGS.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c640-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c640-124">Requirements</span></span>



| <span data-ttu-id="5c640-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c640-125">Requirement</span></span> | <span data-ttu-id="5c640-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5c640-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c640-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c640-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5c640-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c640-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5c640-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c640-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5c640-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5c640-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c640-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5c640-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c640-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c640-132"><dt>Netmon.h</dt></span></span> </dl> |



 

 




