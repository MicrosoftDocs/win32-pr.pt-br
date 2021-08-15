---
description: Obtém o limite de cota padrão como uma cadeia de caracteres de texto.
title: Propriedade DiskQuotaControl.DefaultQuotaLimitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 378d06286a0334cf6ca3056038f45be3a5919b4fd2aa88934957122bc751c141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094221"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>Propriedade DiskQuotaControl.DefaultQuotaLimitText

Obtém o limite de cota padrão como uma cadeia de caracteres de texto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Valor da propriedade

Um valor de cadeia de caracteres que contém o limite de cota padrão para novos usuários do volume. Por exemplo, se a cota padrão for de 10,5 MB, o valor da propriedade será "10,5 MB". Se o volume não tiver nenhuma cota padrão, a propriedade será definida como "Sem Limite" ou o equivalente localizado.

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

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




