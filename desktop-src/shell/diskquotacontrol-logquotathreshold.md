---
description: Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Propriedade DiskQuotaControl. LogQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967304"
---
# <a name="diskquotacontrollogquotathreshold-property"></a>Propriedade DiskQuotaControl. LogQuotaThreshold

Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade será definida como **true** se uma entrada do log de eventos do sistema for feita quando o usuário exceder seu limite de aviso de cota ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DefaultQuotaThreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaLimit**](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




