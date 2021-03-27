---
description: Define ou Obtém o limite de cota padrão.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Propriedade DiskQuotaControl. DefaultQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967311"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>Propriedade DiskQuotaControl. DefaultQuotaThreshold

Define ou Obtém o limite de cota padrão.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Valor da propriedade

Um valor **inteiro** que é definido como o limite de aviso padrão para novos usuários, em bytes.

## <a name="remarks"></a>Comentários

O limite de cota padrão é aplicado automaticamente a novos usuários do volume. Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **true**, o sistema gerará uma entrada de log de eventos. Por exemplo, se o limite padrão for 10,0 MB, o valor da propriedade será "10,0 MB". Se o volume não tiver um limite padrão, a propriedade será definida como "sem limite" ou o equivalente localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




