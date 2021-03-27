---
description: Obtém o limite de cota padrão como uma cadeia de texto.
title: Propriedade DiskQuotaControl. DefaultQuotaLimitText
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
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090017"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>Propriedade DiskQuotaControl. DefaultQuotaLimitText

Obtém o limite de cota padrão como uma cadeia de texto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Valor da propriedade

Um valor de cadeia de caracteres que contém o limite de cota padrão para novos usuários do volume. Por exemplo, se a cota padrão for de 10,5 MB, o valor da propriedade será "10,5 MB". Se o volume não tiver nenhuma cota padrão, a propriedade será definida como "sem limite" ou o equivalente localizado.

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

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




