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
ms.openlocfilehash: cb2117237cd3072163447ee80895cbbb8bb854d7ad4424da83854b28ffa96196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090626"
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

 

 




