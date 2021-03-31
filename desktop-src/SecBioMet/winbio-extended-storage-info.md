---
title: Estrutura de WINBIO_EXTENDED_STORAGE_INFO (WinBio \_ Types. h)
description: Contém informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_STORAGE_INFO
- Ponteiro de estrutura de PWINBIO_EXTENDED_STORAGE_INFO Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2559717a2040cfb617e85e0a51495be1b5987
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918094"
---
# <a name="winbio_extended_storage_info-structure"></a>\_Estrutura de \_ informações de armazenamento ESTENDIdo WINBIO \_

Contém informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**GenericStorageCapabilities**
</dt> <dd>

Os recursos genéricos do componente de armazenamento que está conectado a uma unidade biométrica específica.

</dd> <dt>

**Fator**
</dt> <dd>

O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador de armazenamento. Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de **\_ \_ \_ informações de armazenamento estendida WINBIO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .

</dd> <dt>

**Específicas**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a um fator biométrico específico.

<dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada aos recursos faciais.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento facial do componente de armazenamento que está conectado a uma unidade biométrica específica.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de impressão digital.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento de impressão digital do componente de armazenamento que está conectado a uma unidade biométrica específica

</dd> </dl> </dd> <dt>

**Íris**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de íris.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento de íris do componente de armazenamento que está conectado a uma unidade biométrica específica

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Informações sobre as capacidades e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de voz.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento de voz do componente de armazenamento que está conectado a uma unidade biométrica específica

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_Constantes de tipo BIOMÉTRICO WINBIO \_**](winbio-biometric-type-constants.md)
</dt> <dt>

[**\_Constantes de recurso WINBIO**](winbio-capability-constants.md)
</dt> </dl>

 

 





