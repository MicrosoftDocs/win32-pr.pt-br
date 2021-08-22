---
description: Define ou obtém um valor booliana que indica se uma entrada de log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Propriedade DiskQuotaControl.LogQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5f10710c5a16feb946caa78394d5e57e5d7d4884a50d45dc3e37291f40e7d283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455876"
---
# <a name="diskquotacontrollogquotalimit-property"></a>Propriedade DiskQuotaControl.LogQuotaLimit

Define ou obtém um valor booliana que indica se uma entrada de log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Sintaxe


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade será definida como **TRUE se** uma entrada de log de eventos do sistema for feita quando o usuário exceder seu limite de cota ou **FALSE** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




