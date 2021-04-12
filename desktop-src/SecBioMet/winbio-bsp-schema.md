---
title: Estrutura de WINBIO_BSP_SCHEMA (WinBio \_ Types. h)
description: Descreve os recursos de um provedor de serviços biométricos.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BSP_SCHEMA
- Ponteiro de estrutura de PWINBIO_BSP_SCHEMA Windows Biometric Framework API
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
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455199"
---
# <a name="winbio_bsp_schema-structure"></a>\_Estrutura de \_ esquema WINBIO BSP

A estrutura de **\_ \_ esquema WINBIO BSP** descreve os recursos de um provedor de serviços biométricos. Essa estrutura é usada pela função [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .

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

O tipo de medição biométrica usada por este dispositivo. Atualmente, ela deve ser uma **\_ \_ impressão digital do tipo WINBIO**.

</dd> <dt>

**BspId**
</dt> <dd>

Um valor que identifica exclusivamente esse componente de provedor de serviços biométricos.

</dd> <dt>

**Descrição**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em **nulo** que contém uma descrição do provedor de serviços biométricos.

</dd> <dt>

**Fornecedor**
</dt> <dd>

Uma cadeia de caracteres Unicode terminada em **nulo** que contém o nome do fornecedor que fornece o provedor de serviços biométricos.

</dd> <dt>

**Versão**
</dt> <dd>

Uma estrutura de [**\_ versão do WINBIO**](winbio-version.md) contém a versão de software do componente do provedor de serviços biométricos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





