---
title: WINBIO_PRESENCE_PROPERTIES Union (tipos de WinBio \_ . h)
description: Contém valores biométricos que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.
ms.assetid: 596CAA7F-35D2-442A-8041-BA1010DF5BAD
keywords:
- API de Windows Biometric Framework de União de WINBIO_PRESENCE_PROPERTIES
- PWINBIO_PRESENCE_PROPERTIES o ponteiro de União Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_PROPERTIES
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0568008b870953c34205706acc90cb22a2c0e92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454795"
---
# <a name="winbio_presence_properties-union"></a>União de propriedades de \_ presença de WINBIO \_

Contém valores biométricos que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.

## <a name="syntax"></a>Sintaxe


```C++
typedef union _WINBIO_PRESENCE_PROPERTIES {
  struct {
    RECT BoundingBox;
    LONG Distance;
  } FacialFeatures;
  struct {
    RECT  EyeBoundingBox_1;
    RECT  EyeBoundingBox_2;
    POINT PupilCenter_1;
    POINT PupilCenter_2;
    LONG  Distance;
  } Iris;
} WINBIO_PRESENCE_PROPERTIES, *PWINBIO_PRESENCE_PROPERTIES;
```



## <a name="members"></a>Membros

<dl> <dt>

**FacialFeatures**
</dt> <dd>

Valores para o local dos recursos faciais que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.

<dl> <dt>

**BoundingBox**
</dt> <dd>

A posição dentro do quadro da câmera da face da pessoa, em pixels. O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição. Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera. Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.

</dd> <dt>

**Distância**
</dt> <dd>

A distância entre o local real da face e a distância focal ideal para a face. Esse valor varia de-100 a 100. 0 indica a distância ideal, os valores positivos indicam que o local real da face está muito distante, e os valores negativos indicam que o local real está muito próximo.

</dd> </dl> </dd> <dt>

**Íris**
</dt> <dd>

Valores para o local da íris que o Windows Biometric Framework usado para determinar se um indivíduo estava presente.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels. Se o sistema de reconhecimento de íris estiver monitorando apenas um olho, essa posição será da íris desse olho. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será da íris do olho no quadro da câmera. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho correto do indivíduo.

O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição. Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera. Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels. Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio. Se o sistema de reconhecimento de íris estiver monitorando os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho à esquerda do indivíduo.

O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição. Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera. Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

A posição do centro de um dos Pupils do indivíduo a ser registrado. Se o sistema de reconhecimento de íris estiver monitorando apenas um dos olhos, essa posição será do centro da pupilidade desse olho. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será do centro da Pupil do olho no quadro da câmera. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro do Pupil do lado direito do indivíduo.

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

A posição do centro de um dos Pupils do indivíduo a ser registrado. Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro dos Pupil do lado esquerdo do indivíduo.

</dd> <dt>

**Distância**
</dt> <dd>

A distância entre o local real da íris e a distância focal ideal para a íris. Esse valor varia de-100 a 100. 0 indica a distância ideal, os valores positivos indicam que o local real da íris está muito distante, e os valores negativos indicam que o local real está muito próximo.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



 

 





