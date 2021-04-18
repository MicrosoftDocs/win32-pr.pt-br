---
description: Especifica o estado de integridade de um aplicativo.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: Enumeração de APPLICATION_STATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753298"
---
# <a name="application_state-enumeration"></a>Enumeração de estado do aplicativo \_

Especifica o estado de integridade de um aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**
</dt> <dd>

O estado do aplicativo é íntegro.

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**
</dt> <dd>

O estado do aplicativo é crítico.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar esse elemento de programação, os componentes de integração do Windows 8 devem ser instalados na máquina virtual em que o aplicativo está sendo executado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                      |
| Versão<br/>                  | Componentes de integração do Windows 8<br/>                                                           |
| INSERI<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Setapplicationstate**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




