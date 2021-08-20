---
title: WINBIO_EXTENDED_STORAGE_INFO estrutura (Tipos \_ winbio.h)
description: Contém informações sobre os recursos e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica.
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO estrutura Windows API do Biometric Framework
- PWINBIO_EXTENDED_STORAGE_INFO de estrutura Windows API do Biometric Framework
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
ms.openlocfilehash: 3e8a9f133baf77a77d3db33001e996accc9574f86ad708037900a5db7c0c5e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910377"
---
# <a name="winbio_extended_storage_info-structure"></a>Estrutura DE \_ INFORMAÇÕES DE ARMAZENAMENTO ESTENDIDO \_ \_ WINBIO

Contém informações sobre os recursos e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica.

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

O tipo de unidade biométrica para a qual essa estrutura contém informações sobre os recursos e os requisitos de registro do adaptador de armazenamento. Por exemplo, se o  valor do membro Factor for WINBIO TYPE FINGERPRINT , a estrutura **WINBIO \_ EXTENDED \_ STORAGE \_** **\_ \_ INFO** se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **Specifc.Fingerprint.**

</dd> <dt>

**Específico**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a um fator biométrico específico.

<dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informações sobre os recursos e requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a recursos faciais.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento facial do componente de armazenamento que está conectado a uma unidade biométrica específica.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada a padrões de impressão digital.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento de impressão digital do componente de armazenamento conectado a uma unidade biométrica específica

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada aos padrões de íris.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento de íris do componente de armazenamento que está conectado a uma unidade biométrica específica

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Informações sobre os recursos e os requisitos de registro do adaptador de armazenamento para uma unidade biométrica relacionada aos padrões de voz.

<dl> <dt>

**Funcionalidades**
</dt> <dd>

Os recursos de reconhecimento de voz do componente de armazenamento conectado a uma unidade biométrica específica

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h para aplicativos cliente ou \_ adaptadores Winbio.h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Constantes \_ DE TIPO \_ BIOMÉTRICO WINBIO**](winbio-biometric-type-constants.md)
</dt> <dt>

[**Constantes \_ WINBIO CAPABILITY**](winbio-capability-constants.md)
</dt> </dl>

 

 





