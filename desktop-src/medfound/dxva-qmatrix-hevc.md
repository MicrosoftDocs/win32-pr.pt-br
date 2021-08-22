---
description: Define uma matriz de quantização.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC estrutura (Dxva.h)
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
ms.openlocfilehash: 5d71b392d41c123eb0106d08f1a75d2a5147977b106c811e0bf0786ab2acff2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974585"
---
# <a name="dxva_qmatrix_hevc-structure"></a>Estrutura DXVA \_ Qmatrix \_ HEVC

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

Contém as listas de dimensionamento para o processo de dimensionamento 4x4, correspondente a ScalingList 0 MatrixID i na especificação HEVC, em que MatrixID está no intervalo de 0 a 5, inclusive, e i está no intervalo de \[ \] \[ \] \[ \] 0 a 15, inclusive.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento 8x8, correspondente a ScalingList 1 MatrixID i na especificação HEVC, em que MatrixID está no intervalo de 0 a 5, inclusive, e i está no intervalo de \[ \] \[ \] \[ \] 0 a 63, inclusive.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento 8x8, correspondente a ScalingList 2 MatrixID i na especificação HEVC, em que MatrixID está no intervalo de 0 a 5, inclusive, e i está no intervalo de \[ \] \[ \] \[ \] 0 a 63, inclusive.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contém as listas de dimensionamento para o processo de dimensionamento 8x8, correspondente a ScalingList 3 MatrixID i na especificação HEVC, em que MatrixID está no intervalo de 0 a 1, inclusive, e i está no intervalo de \[ \] \[ \] \[ \] 0 a 63, inclusive.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contém o valor dc da lista de dimensionamento para tamanho 16x16 com sizeID igual a 2 e correspondente à lista de dimensionamento \_ \_ do coef dc \_ \_ minus8 \[ sizeID − 2 matrixID +8 com sizeID igual a 2 e matrixID no intervalo de \] \[ \] 0 a 5, inclusive, na especificação HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contém o valor dc da lista de dimensionamento para tamanho 32x32 com sizeID igual a 3 e correspondente à lista de dimensionamento dc \_ \_ \_ coef \_ \[ minus8 sizeID − 2 matrixID +8 com sizeID igual a 3 e matrixID no intervalo de \] \[ \] 0 a 1, inclusive, na especificação HEVC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[estruturas Media Foundation dados](media-foundation-structures.md)
</dt> </dl>

 

 




