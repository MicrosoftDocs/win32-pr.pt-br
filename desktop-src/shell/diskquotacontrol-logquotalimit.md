---
description: Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Propriedade DiskQuotaControl. LogQuotaLimit
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
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967305"
---
# <a name="diskquotacontrollogquotalimit-property"></a>Propriedade DiskQuotaControl. LogQuotaLimit

Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade será definida como **true** se uma entrada do log de eventos do sistema for feita quando o usuário exceder seu limite de cota ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




