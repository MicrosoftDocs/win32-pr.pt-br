---
title: Estrutura de WINBIO_EXTENDED_SENSOR_INFO (WinBio \_ Types. h)
description: Contém informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_SENSOR_INFO
- Ponteiro de estrutura de PWINBIO_EXTENDED_SENSOR_INFO Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918095"
---
# <a name="winbio_extended_sensor_info-structure"></a>\_Estrutura de \_ informações do sensor ESTENDIdo WINBIO \_

Contém informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**GenericSensorCapabilities**
</dt> <dd>

Os recursos genéricos do componente de sensor que está conectado a uma unidade biométrica específica.

</dd> <dt>

**Fator**
</dt> <dd>

O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador do sensor. Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de **\_ \_ \_ informações do sensor estendido WINBIO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .

</dd> <dt>

**Específicas**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a um fator biométrico específico.

<dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada aos recursos faciais.

<dl> <dt>

**Quadros**
</dt> <dd>

O tamanho do quadro da câmera, indicado como um comprimento e uma largura em pixels pelos membros **direito** e **inferior** da estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . O ponto (0, 0) representa o canto superior esquerdo do quadro.

</dd> <dt>

**FrameOffset**
</dt> <dd>

O deslocamento do quadro da câmera para a face da câmera de vídeo, em pixels. Um valor de (0, 0) indica que o quadro da câmera para a face e a câmera de vídeo se sobrepõem completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

A orientação preferida para a câmera.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a padrões de impressão digital.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

**Íris**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a padrões de íris.

<dl> <dt>

**Quadros**
</dt> <dd>

O tamanho do quadro da câmera, indicado como um comprimento e uma largura em pixels pelos membros **direito** e **inferior** da estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) . O ponto (0, 0) representa o canto superior esquerdo do quadro.

</dd> <dt>

**FrameOffset**
</dt> <dd>

O deslocamento do quadro da câmera da íris da câmera de vídeo, em pixels. Um valor de (0, 0) indica que o quadro da câmera para a íris e a câmera de vídeo se sobrepõem completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

A orientação preferida para a câmera.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do sensor para uma unidade biométrica relacionada a padrões de voz.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Constantes de recurso WINBIO**](winbio-capability-constants.md)
</dt> <dt>

[**\_Constantes de tipo BIOMÉTRICO WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes de orientação de WINBIO \_**](winbio-orientation-constants.md)
</dt> </dl>

 

