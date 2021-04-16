---
title: Estrutura de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS ( \_ adaptador WINBIO. h)
description: Contém informações adicionais que um adaptador de mecanismo precisa para criar um modelo de registro.
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
- Ponteiro de estrutura de PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS Windows Biometric Framework API
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
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454796"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>\_Estrutura de \_ parâmetros de registro ESTENDIdo WINBIO \_

A estrutura de **\_ \_ \_ parâmetros de registro estendido WINBIO** contém informações adicionais que um adaptador de mecanismo precisa para criar um modelo de registro.

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

O tamanho (em bytes) da estrutura **de \_ \_ \_ parâmetros de registro estendido do WINBIO** .

</dd> <dt>

**Subfator**
</dt> <dd>

Um dos valores [**\_ \_ constantes do subtipo WINBIO Biometric**](winbio-biometric-subtype-constants.md) que fornece informações adicionais sobre o registro.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Windows Biometric Framework passa essa estrutura para o método [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) durante uma operação de registro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                     |
| parâmetro<br/>                   | <dl> <dt>\_Adaptador WinBio. h (inclui o \_ adaptador WinBio. h)</dt> </dl> |



 

 





