---
title: Enumeração de WINBIO_POLICY_SOURCE (WinBio \_ Types. h)
description: Lista as possíveis fontes de informações de política para a detecção de falsificação para fatores biométricos.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_POLICY_SOURCE
- PWINBIO_POLICY_SOURCE Windows Biometric Framework API do ponteiro de enumeração
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295901"
---
# <a name="winbio_policy_source-enumeration"></a>Enumeração de origem de \_ política WINBIO \_

Lista as possíveis fontes de informações de política para a detecção de falsificação para fatores biométricos.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**política de WINBIO \_ \_ desconhecida**
</dt> <dd>

A origem da política é desconhecida.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_padrão de política WINBIO \_**
</dt> <dd>

A política é a política padrão que o Windows Biometric Framework fornece.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO \_ política \_ local**
</dt> <dd>

A política que o usuário individual definiu para sua conta usando o aplicativo **configurações** . Essa política substitui a política padrão.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_administrador da política do WINBIO \_**
</dt> <dd>

Uma política de grupo que o administrador de ti definiu para a empresa. Os usuários individuais não podem substituir essa política.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_ação da \_ política antifalsificação do \_ WINBIO \_**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





