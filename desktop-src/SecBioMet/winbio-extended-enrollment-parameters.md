---
title: WINBIO_EXTENDED_ENROLLMENT_PARAMETERS (adaptador \_ Winbio.h)
description: Contém informações adicionais de que um adaptador de mecanismo precisa para criar um modelo de registro.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS estrutura Windows API do Biometric Framework
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS de estrutura Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55173b5badfb8764cfc9c681f4ed92e2f0d1c50e5db09075185af9e5db2e6433
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910485"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>Estrutura DE \_ \_ PARÂMETROS DE \_ REGISTRO ESTENDIDO WINBIO

A **estrutura PARÂMETROS DE \_ REGISTRO \_ ESTENDIDO \_ WINBIO** contém informações adicionais de que um adaptador de mecanismo precisa para criar um modelo de registro.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tamanho**
</dt> <dd>

O tamanho (em bytes) da estrutura **\_ \_ \_ PARÂMETROS DE REGISTRO ESTENDIDO WINBIO.**

</dd> <dt>

**Subfactor**
</dt> <dd>

Um dos valores [**de \_ \_ Constantes WINBIO BIOMETRIC SUBTYPE**](winbio-biometric-subtype-constants.md) que fornece informações adicionais sobre o registro.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Windows Biometric Framework passa essa estrutura para o [**método EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante uma operação de registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ adapter.h (inclua Adaptador \_ winbio.h)</dt> </dl> |



 

 





