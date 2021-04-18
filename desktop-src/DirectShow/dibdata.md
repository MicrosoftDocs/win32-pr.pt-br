---
description: A estrutura DIBDATA contém informações sobre um bitmap independente de dispositivo (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Estrutura DIBDATA (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760710"
---
# <a name="dibdata-structure"></a><span data-ttu-id="a47b9-103">Estrutura DIBDATA</span><span class="sxs-lookup"><span data-stu-id="a47b9-103">DIBDATA structure</span></span>

<span data-ttu-id="a47b9-104">A `DIBDATA` estrutura contém informações sobre um bitmap independente de dispositivo (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="a47b9-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="a47b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a47b9-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="a47b9-106">Membros</span><span class="sxs-lookup"><span data-stu-id="a47b9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a47b9-107">**PaletteVersion**</span><span class="sxs-lookup"><span data-stu-id="a47b9-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="a47b9-108">Esse membro deve ser incrementado sempre que a paleta for alterada.</span><span class="sxs-lookup"><span data-stu-id="a47b9-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="a47b9-109">**DibSection**</span><span class="sxs-lookup"><span data-stu-id="a47b9-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="a47b9-110">Estrutura **DIBSECTION** que contém informações sobre o DIB.</span><span class="sxs-lookup"><span data-stu-id="a47b9-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="a47b9-111">Consulte a documentação do GDI para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="a47b9-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="a47b9-112">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="a47b9-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="a47b9-113">Identificador para o bitmap.</span><span class="sxs-lookup"><span data-stu-id="a47b9-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="a47b9-114">**hMapping**</span><span class="sxs-lookup"><span data-stu-id="a47b9-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="a47b9-115">Identificador para um objeto de mapeamento de arquivo usado para compartilhar memória entre GDI e um objeto [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="a47b9-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="a47b9-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="a47b9-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="a47b9-117">Endereço do bitmap.</span><span class="sxs-lookup"><span data-stu-id="a47b9-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a47b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a47b9-118">Requirements</span></span>



| <span data-ttu-id="a47b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a47b9-119">Requirement</span></span> | <span data-ttu-id="a47b9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a47b9-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a47b9-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a47b9-121">Header</span></span><br/> | <dl> <span data-ttu-id="a47b9-122"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a47b9-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 




