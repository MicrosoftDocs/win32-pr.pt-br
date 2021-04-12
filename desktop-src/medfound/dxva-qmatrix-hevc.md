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
# <a name="dxva_qmatrix_hevc-structure"></a>Estrutura de HEVC de DXVA \_ Qmatrix \_

Define uma matriz de quantização.

## <a name="syntax"></a>Sintaxe


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



## <a name="members"></a>Membros

<dl> <dt>

**ucScalingLists0 \[ 6 \] \[ 16\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento de 4x4, correspondente a DimensionID \[ 0 \] \[ matrixid \] \[ i \] na especificação de HEVC, em que matrixid está no intervalo de 0 a 5, inclusive, e estou no intervalo de 0 a 15, inclusive.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento de 8x8, correspondente a DimensionID \[ 1 \] \[ matrixid \] \[ i \] na especificação de HEVC, em que matrixid está no intervalo de 0 a 5, inclusive, e estou no intervalo de 0 a 63, inclusive.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento de 8x8, correspondente à redimensionable \[ 2 \] \[ matrixid \] \[ i \] na especificação HEVC, em que matrixid está no intervalo de 0 a 5, inclusive, e estou no intervalo de 0 a 63, inclusive.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento de 8x8, correspondente à redimensional \[ 3 \] \[ matrixid \] \[ i \] na especificação HEVC, em que matrixid está no intervalo de 0 a 1, inclusive, e estou no intervalo de 0 a 63, inclusive.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contém o valor de DC da lista de dimensionamento para o tamanho de 16x16 com sizeid igual a 2 e correspondente à lista de dimensionamento \_ \_ DC \_ Coef \_ minus8 \[ sizeid − 2 \] \[ matrixid \] + 8 com sizeid igual a 2 e matrixid no intervalo de 0 a 5, inclusive, na especificação HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contém o valor de DC da lista de dimensionamento para o tamanho de 32x32 com sizeid igual a 3 e correspondente à lista de dimensionamento \_ \_ DC \_ Coef \_ minus8 \[ sizeid − 2 \] \[ matrixid \] + 8 com sizeid igual a 3 e matrixid no intervalo de 0 a 1, inclusive, na especificação HEVC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




