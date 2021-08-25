---
description: Define ou obtém o limite de cota padrão.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Propriedade DiskQuotaControl.DefaultQuotaThreshold
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
ms.openlocfilehash: 46d44f2e2df24c5ee1cbf646643810e09d007eb15ba6c9a352eb492dfb104752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943106"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>Propriedade DiskQuotaControl.DefaultQuotaThreshold

Define ou obtém o limite de cota padrão.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Valor da propriedade

Um **valor** inteiro definido como o limite de aviso padrão para novos usuários, em bytes.

## <a name="remarks"></a>Comentários

O limite de cota padrão é aplicado automaticamente aos novos usuários do volume. Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **TRUE,** o sistema gerará uma entrada de log de eventos. Por exemplo, se o limite padrão for 10,0 MB, o valor da propriedade será "10,0 MB". Se o volume não tiver nenhum limite padrão, a propriedade será definida como "Sem Limite" ou o equivalente localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




