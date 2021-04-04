---
title: Estrutura de WINBIO_EXTENDED_ENGINE_INFO (WinBio \_ Types. h)
description: Contém informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica.
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_ENGINE_INFO
- Ponteiro de estrutura de PWINBIO_EXTENDED_ENGINE_INFO Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824781"
---
# <a name="winbio_extended_engine_info-structure"></a>\_Estrutura de \_ informações do mecanismo estendido do WINBIO \_

Contém informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**GenericEngineCapabilities**
</dt> <dd>

Os recursos genéricos do componente do mecanismo que está conectado a uma unidade biométrica específica.

</dd> <dt>

**Fator**
</dt> <dd>

O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador do mecanismo. Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de **\_ \_ \_ informações do mecanismo estendido WINBIO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .

</dd> <dt>

**Específicas**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a um fator biométrico específico.

<dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada aos recursos faciais.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> </dl> </dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a padrões de impressão digital.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

O número de exemplos bons necessários para criar um novo modelo de impressão digital.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

O número total de boas amostras necessárias para criar um novo modelo de impressão digital.

</dd> <dt>

**Centraliza**
</dt> <dd>

O número de exemplos bons para o centro da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**TopEdge**
</dt> <dd>

O número de exemplos bons para a borda superior da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**BottomEdge**
</dt> <dd>

O número de exemplos bons para a borda inferior da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**LeftEdge**
</dt> <dd>

O número de exemplos bons para a borda esquerda da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**RightEdge**
</dt> <dd>

O número de exemplos bons para a borda direita da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> </dl> </dd> </dl> </dd> <dt>

**Íris**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a padrões de íris.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> </dl> </dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador do mecanismo para uma unidade biométrica relacionada a padrões de voz.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

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
</dt> </dl>

 

 





