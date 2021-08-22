---
title: Enumeração de MPSCAN_TYPE (MpClient. h)
description: Tipo de verificação executada.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- recursos do ambiente de Windows herdado de enumeração de MPSCAN_TYPE
- Windows recursos de ambiente herdados do ponteiro de enumeração PMPSCAN_TYPE
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56906bfc9ad57f93bac4c8b8c27360b5ade9592ac33efe39574fe8890299e13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747127"
---
# <a name="mpscan_type-enumeration"></a>\_Enumeração de tipo MPSCAN

Tipo de verificação executada.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**tipo de MPSCAN \_ \_ desconhecido**
</dt> <dd>

Somente para uso interno.

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ tipo \_ rápido**
</dt> <dd>

Verifica os processos em execução e vários pontos de ASEP no sistema em que o malware normalmente se oculta.

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN \_ tipo \_ completo**
</dt> <dd>

Executa uma verificação rápida seguida da verificação de todas as unidades fixas do sistema.

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_recurso de tipo MPSCAN \_**
</dt> <dd>

Examina recursos específicos, como arquivos ou pastas.

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**tipo de MPSCAN \_ \_ MaxValue**
</dt> <dd>

Valor máximo possível.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





