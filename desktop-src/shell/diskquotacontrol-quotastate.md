---
description: Define ou Obtém o estado das cotas de disco do volume.
title: Propriedade DiskQuotaControl. Quotastate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461260"
---
# <a name="diskquotacontrolquotastate-property"></a>Propriedade DiskQuotaControl. Quotastate

Define ou Obtém o estado das cotas de disco do volume.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ser definida como um dos valores a seguir.



| Estado          | Valor | Descrição               |
|----------------|-------|---------------------------|
| dqStateDisable | 0     | As cotas de disco estão desabilitadas. |
| dqStateTrack   | 1     | As cotas de disco estão desabilitadas. |
| dqStateEnforce | 2     | Impor o limite de cota.      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




