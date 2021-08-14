---
title: Estrutura de WINBIO_VERSION (WinBio \_ Types. h)
description: Contém o número de versão do software de um componente do provedor de serviços biométrico.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_VERSION
- ponteiro de estrutura de PWINBIO_VERSION Windows Biometric Framework API
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
ms.openlocfilehash: de81dd3da7f37e473a65caaf3e4cd52c8fd2f6732dced45f43245cb4e4c5c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909111"
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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**\_esquema WINBIO BSP \_**](winbio-bsp-schema.md)
</dt> <dt>

[**\_esquema de unidade WINBIO \_**](winbio-unit-schema.md)
</dt> </dl>

 

 





