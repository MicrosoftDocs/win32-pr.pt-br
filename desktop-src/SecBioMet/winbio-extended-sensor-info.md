---
title: WINBIO_EXTENDED_SENSOR_INFO estrutura (Tipos \_ winbio.h)
description: Contém informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica.
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO estrutura Windows API do Biometric Framework
- PWINBIO_EXTENDED_SENSOR_INFO de estrutura Windows API do Biometric Framework
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
ms.openlocfilehash: dd8c323b4f4e3847c399e314da22048f658fb68c3b07ecf82f71ce0ed327c368
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910414"
---
# <a name="winbio_extended_sensor_info-structure"></a>Estrutura WINBIO \_ EXTENDED \_ SENSOR \_ INFO

Contém informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica.

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

O tipo de unidade biométrica para a qual essa estrutura contém informações sobre os recursos e os requisitos de registro do adaptador de sensor. Por exemplo, se o  valor do membro Factor for **WINBIO \_ TYPE \_ FINGERPRINT**, a estrutura **WINBIO \_ EXTENDED SENSOR \_ \_ INFO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **Specifc.Fingerprint.**

</dd> <dt>

**Específico**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica relacionada a um fator biométrico específico.

<dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica relacionada a recursos faciais.

<dl> <dt>

**FrameSize**
</dt> <dd>

O tamanho do quadro da câmera, indicado como um  comprimento e largura em pixels pelos membros direito e **inferior** da [**estrutura RECT.**](/previous-versions//dd162897(v=vs.85)) O ponto (0, 0) representa o canto superior esquerdo do quadro.

</dd> <dt>

**FrameOffset**
</dt> <dd>

O deslocamento do quadro da câmera para o rosto da câmera de vídeo, em pixels. Um valor de (0, 0) indica que o quadro da câmera para o rosto e a câmera de vídeo se sobrepõem completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

A orientação preferencial para a câmera.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica relacionada a padrões de impressão digital.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica relacionada aos padrões de íris.

<dl> <dt>

**FrameSize**
</dt> <dd>

O tamanho do quadro da câmera, indicado como um  comprimento e largura em pixels pelos membros direito e **inferior** da [**estrutura RECT.**](/previous-versions//dd162897(v=vs.85)) O ponto (0, 0) representa o canto superior esquerdo do quadro.

</dd> <dt>

**FrameOffset**
</dt> <dd>

O deslocamento do quadro da câmera para a íris da câmera de vídeo, em pixels. Um valor de (0, 0) indica que o quadro da câmera para a íris e a câmera de vídeo se sobrepõem completamente.

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

A orientação preferencial para a câmera.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de sensor para uma unidade biométrica relacionada aos padrões de voz.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h para aplicativos cliente ou \_ adaptadores Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Constantes \_ WINBIO CAPABILITY**](winbio-capability-constants.md)
</dt> <dt>

[**Constantes \_ DE TIPO \_ BIOMÉTRICO WINBIO**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes \_ DE ORIENTAÇÃO WINBIO**](winbio-orientation-constants.md)
</dt> </dl>

 

