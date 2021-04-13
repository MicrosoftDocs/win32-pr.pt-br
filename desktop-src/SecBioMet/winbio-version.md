---
title: Estrutura de WINBIO_VERSION (WinBio \_ Types. h)
description: Contém o número de versão do software de um componente do provedor de serviços biométrico.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_VERSION
- Ponteiro de estrutura de PWINBIO_VERSION Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455949"
---
# <a name="winbio_version-structure"></a>Estrutura de versão do WINBIO \_

A estrutura de **\_ versão do WINBIO** contém o número de versão do software de um componente do provedor de serviços biométricos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Membros

<dl> <dt>

**MajorVersion**
</dt> <dd>

Um **DWORD** que contém o número de versão principal.

</dd> <dt>

**MinorVersion**
</dt> <dd>

Um **DWORD** que contém o número de versão secundária.

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

[**\_esquema WINBIO BSP \_**](winbio-bsp-schema.md)
</dt> <dt>

[**\_esquema de unidade WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





