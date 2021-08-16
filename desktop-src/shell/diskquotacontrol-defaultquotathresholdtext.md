---
description: Obtém o limite de cota padrão como uma cadeia de caracteres de texto.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Propriedade DiskQuotaControl.DefaultQuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8f16c32b46544d3966ae5e3a097576074d28bcfa40ce568cd591d37f9d3d0552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459899"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>Propriedade DiskQuotaControl.DefaultQuotaThresholdText

Obtém o limite de cota padrão como uma cadeia de caracteres de texto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Valor da propriedade

Um valor de cadeia de caracteres que contém o limite de cota padrão para o volume.

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

 

 




