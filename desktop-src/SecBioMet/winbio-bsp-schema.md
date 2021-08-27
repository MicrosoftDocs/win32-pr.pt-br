---
title: WINBIO_BSP_SCHEMA estrutura (Tipos \_ winbio.h)
description: Descreve os recursos de um provedor de serviços biométricos.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- WINBIO_BSP_SCHEMA estrutura Windows API do Biometric Framework
- PWINBIO_BSP_SCHEMA de estrutura Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff46f5484addb0221d9e441df73ecca3e8283da88ee7849e4362314aa1c375e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080776"
---
# <a name="winbio_bsp_schema-structure"></a>Estrutura WINBIO \_ BSP \_ SCHEMA

A **estrutura \_ WINBIO BSP \_ SCHEMA** descreve os recursos de um provedor de serviços biométricos. Essa estrutura é usada pela [**função WinBioEnumServiceProviders.**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a>Membros

<dl> <dt>

**BiometricFactor**
</dt> <dd>

O tipo de medida biométrica usada por este dispositivo. Atualmente, isso deve ser **IMPRESSÃO DIGITAL DO \_ TIPO \_ WINBIO.**

</dd> <dt>

**BspId**
</dt> <dd>

Um valor que identifica exclusivamente esse componente do provedor de serviços biométricos.

</dd> <dt>

**Descrição**
</dt> <dd>

Uma **cadeia de** caracteres Unicode terminada em NULL que contém uma descrição do provedor de serviços biométricos.

</dd> <dt>

**Fornecedor**
</dt> <dd>

Uma **cadeia de** caracteres Unicode terminada em NULL que contém o nome do fornecedor que fornece o provedor de serviços biométricos.

</dd> <dt>

**Versão**
</dt> <dd>

Uma [**estrutura WINBIO \_ VERSION**](winbio-version.md) contém a versão de software do componente do provedor de serviços biométricos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





