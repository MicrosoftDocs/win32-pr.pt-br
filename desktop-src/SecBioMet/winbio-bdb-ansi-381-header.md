---
title: Estrutura de WINBIO_BDB_ANSI_381_HEADER (WinBio \_ Types. h)
description: Especifica informações sobre uma série de exemplos de impressão digital ou Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BDB_ANSI_381_HEADER
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811070"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="36410-104">\_Estrutura de cabeçalho WINBIO BdB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="36410-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="36410-105">A estrutura de **\_ cabeçalho WINBIO BDB \_ ANSI \_ 381 \_** especifica informações sobre uma série de exemplos de impressão digital ou Palm.</span><span class="sxs-lookup"><span data-stu-id="36410-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="36410-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36410-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="36410-107">Membros</span><span class="sxs-lookup"><span data-stu-id="36410-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="36410-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="36410-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="36410-109">O tamanho, em bytes, dessa estrutura mais o tamanho de todas as estruturas de [**\_ registro WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) para as amostras de impressão digital ou Palm capturadas de um usuário final.</span><span class="sxs-lookup"><span data-stu-id="36410-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="36410-110">Somente os seis bytes baixos são válidos.</span><span class="sxs-lookup"><span data-stu-id="36410-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="36410-111">**FormatIdentifier**</span><span class="sxs-lookup"><span data-stu-id="36410-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="36410-112">Especifica o formato.</span><span class="sxs-lookup"><span data-stu-id="36410-112">Specifies the format.</span></span> <span data-ttu-id="36410-113">Atualmente, isso deve ser 0x46495200.</span><span class="sxs-lookup"><span data-stu-id="36410-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="36410-114">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="36410-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="36410-115">Especifica o número de versão.</span><span class="sxs-lookup"><span data-stu-id="36410-115">Specifies the version number.</span></span> <span data-ttu-id="36410-116">Atualmente, isso deve ser 0x30313000 que corresponde internamente a 0.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="36410-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="36410-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="36410-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="36410-118">Uma estrutura de [**\_ \_ formato registrada WINBIO**](winbio-registered-format.md) que contém o formato de dados registrado como um par de proprietário/tipo.</span><span class="sxs-lookup"><span data-stu-id="36410-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="36410-119">**CaptureDeviceId**</span><span class="sxs-lookup"><span data-stu-id="36410-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="36410-120">Contém a ID de unidade do dispositivo usado para capturar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="36410-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="36410-121">**ImageAcquisitionLevel**</span><span class="sxs-lookup"><span data-stu-id="36410-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="36410-122">Especifica o nível de resolução no qual o exemplo é capturado.</span><span class="sxs-lookup"><span data-stu-id="36410-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="36410-123">**HorizontalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="36410-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="36410-124">Especifica a resolução horizontal da verificação.</span><span class="sxs-lookup"><span data-stu-id="36410-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="36410-125">**VerticalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="36410-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="36410-126">Especifica a resolução vertical da verificação.</span><span class="sxs-lookup"><span data-stu-id="36410-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="36410-127">**HorizontalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="36410-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="36410-128">Especifica a resolução horizontal da imagem de impressão digital ou Palm capturada.</span><span class="sxs-lookup"><span data-stu-id="36410-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="36410-129">**VerticalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="36410-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="36410-130">Especifica a resolução vertical da imagem de impressão digital ou Palm capturada.</span><span class="sxs-lookup"><span data-stu-id="36410-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="36410-131">**ElementCount**</span><span class="sxs-lookup"><span data-stu-id="36410-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="36410-132">Número de registros de dedos ou de Palm nesta estrutura.</span><span class="sxs-lookup"><span data-stu-id="36410-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="36410-133">**ScaleUnits**</span><span class="sxs-lookup"><span data-stu-id="36410-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="36410-134">Contém a unidade de medida, 1 para polegadas e 2 para centímetros.</span><span class="sxs-lookup"><span data-stu-id="36410-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="36410-135">**PixelDepth**</span><span class="sxs-lookup"><span data-stu-id="36410-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="36410-136">Especifica o número de bits em um pixel.</span><span class="sxs-lookup"><span data-stu-id="36410-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="36410-137">Pode ser de 1 a 16 bits por pixel para cor.</span><span class="sxs-lookup"><span data-stu-id="36410-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="36410-138">**ImageCompressionAlg**</span><span class="sxs-lookup"><span data-stu-id="36410-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="36410-139">Especifica o algoritmo usado para compactar a imagem de dedo ou Palm.</span><span class="sxs-lookup"><span data-stu-id="36410-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="36410-140">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="36410-140">**Reserved**</span></span>
<span data-ttu-id="36410-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="36410-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="36410-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36410-142">Requirements</span></span>



| <span data-ttu-id="36410-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="36410-143">Requirement</span></span> | <span data-ttu-id="36410-144">Valor</span><span class="sxs-lookup"><span data-stu-id="36410-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36410-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36410-145">Minimum supported client</span></span><br/> | <span data-ttu-id="36410-146">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36410-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="36410-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36410-147">Minimum supported server</span></span><br/> | <span data-ttu-id="36410-148">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="36410-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="36410-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36410-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="36410-150"><dt>WinBio \_ Types. h (inclui WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36410-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36410-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="36410-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36410-152">Estruturas de aplicativo cliente</span><span class="sxs-lookup"><span data-stu-id="36410-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





