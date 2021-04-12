---
description: Define uma matriz de quantização.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: Estrutura de DXVA_Qmatrix_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501174"
---
# <a name="dxva_qmatrix_hevc-structure"></a><span data-ttu-id="8155b-103">Estrutura de HEVC de DXVA \_ Qmatrix \_</span><span class="sxs-lookup"><span data-stu-id="8155b-103">DXVA\_Qmatrix\_HEVC structure</span></span>

<span data-ttu-id="8155b-104">Define uma matriz de quantização.</span><span class="sxs-lookup"><span data-stu-id="8155b-104">Defines a quantization matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="8155b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8155b-105">Syntax</span></span>


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a><span data-ttu-id="8155b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="8155b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="8155b-107">**ucScalingLists0 \[ 6 \] \[ 16\]**</span><span class="sxs-lookup"><span data-stu-id="8155b-107">**ucScalingLists0\[6\]\[16\]**</span></span>
</dt> <dd>

<span data-ttu-id="8155b-108">Contém as listas de dimensionamento para o processo de dimensionamento de 4x4, correspondente a DimensionID \[ 0 \] \[ matrixid \] \[ i \] na especificação de HEVC, em que matrixid está no intervalo de 0 a 5, inclusive, e estou no intervalo de 0 a 15, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8155b-108">Contains the scaling lists for the 4x4 scaling process, corresponding to ScalingList\[ 0 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 15, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="8155b-109">**ucScalingLists1 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="8155b-109">**ucScalingLists1\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="8155b-110">Contém as listas de dimensionamento para o processo de dimensionamento de 8x8, correspondente a DimensionID \[ 1 \] \[ matrixid \] \[ i \] na especificação de HEVC, em que matrixid está no intervalo de 0 a 5, inclusive, e estou no intervalo de 0 a 63, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8155b-110">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 1 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="8155b-111">**ucScalingLists2 \[ 6 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="8155b-111">**ucScalingLists2\[6\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="8155b-112">Contém as listas de dimensionamento para o processo de dimensionamento de 8x8, correspondente à redimensionable \[ 2 \] \[ matrixid \] \[ i \] na especificação HEVC, em que matrixid está no intervalo de 0 a 5, inclusive, e estou no intervalo de 0 a 63, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8155b-112">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 2 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 5, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="8155b-113">**ucScalingLists3 \[ 2 \] \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="8155b-113">**ucScalingLists3\[2\]\[64\]**</span></span>
</dt> <dd>

<span data-ttu-id="8155b-114">Contém as listas de dimensionamento para o processo de dimensionamento de 8x8, correspondente à redimensional \[ 3 \] \[ matrixid \] \[ i \] na especificação HEVC, em que matrixid está no intervalo de 0 a 1, inclusive, e estou no intervalo de 0 a 63, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8155b-114">Contains the scaling lists for the 8x8 scaling process, corresponding to ScalingList\[ 3 \]\[ MatrixID \]\[ i \] in HEVC specification, where MatrixID is in the range of 0 to 1, inclusive, and i is in the range of 0 to 63, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="8155b-115">**ucScalingListDCCoefSizeID2**</span><span class="sxs-lookup"><span data-stu-id="8155b-115">**ucScalingListDCCoefSizeID2**</span></span>
</dt> <dd>

<span data-ttu-id="8155b-116">Contém o valor de DC da lista de dimensionamento para o tamanho de 16x16 com sizeid igual a 2 e correspondente à lista de dimensionamento \_ \_ DC \_ Coef \_ minus8 \[ sizeid − 2 \] \[ matrixid \] + 8 com sizeid igual a 2 e matrixid no intervalo de 0 a 5, inclusive, na especificação HEVC.</span><span class="sxs-lookup"><span data-stu-id="8155b-116">Contains the DC value of the scaling list for 16x16 size with sizeID equal to 2 and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 2 and matrixID in the range of 0 to 5, inclusive, in HEVC specification.</span></span>

</dd> <dt>

<span data-ttu-id="8155b-117">**ucScalingListDCCoefSizeID3**</span><span class="sxs-lookup"><span data-stu-id="8155b-117">**ucScalingListDCCoefSizeID3**</span></span>
</dt> <dd>

<span data-ttu-id="8155b-118">Contém o valor de DC da lista de dimensionamento para o tamanho de 32x32 com sizeid igual a 3 e correspondente à lista de dimensionamento \_ \_ DC \_ Coef \_ minus8 \[ sizeid − 2 \] \[ matrixid \] + 8 com sizeid igual a 3 e matrixid no intervalo de 0 a 1, inclusive, na especificação HEVC.</span><span class="sxs-lookup"><span data-stu-id="8155b-118">Contains the DC value of the scaling list for 32x32 size with sizeID equal to 3, and corresponding to scaling\_list\_dc\_coef\_minus8\[ sizeID − 2 \]\[ matrixID \] +8 with sizeID equal to 3 and matrixID in the range of 0 to 1, inclusive, in HEVC specification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8155b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8155b-119">Requirements</span></span>



| <span data-ttu-id="8155b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8155b-120">Requirement</span></span> | <span data-ttu-id="8155b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8155b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8155b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8155b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8155b-123">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8155b-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8155b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8155b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8155b-125">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="8155b-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8155b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8155b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8155b-127"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8155b-127"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8155b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8155b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8155b-129">Estruturas de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8155b-129">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




