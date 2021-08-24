---
description: Obtém um valor booliana que indica se o arquivo de cota para o volume está sendo reconstruído no momento.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Propriedade DiskQuotaControl.QuotaFileRebuilding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8e90d5d920392b9b518fed619aeb4f8c7b99d830fad9f6f901c59fe6128ca94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710516"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Propriedade DiskQuotaControl.QuotaFileRebuilding

Obtém um valor booliana que indica se o arquivo de cota para o volume está sendo reconstruído no momento.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade será definida como **TRUE se** o arquivo de cota estiver sendo reconstruído ou **FALSE** caso contrário.

## <a name="remarks"></a>Comentários

O arquivo de cota é reconstruído automaticamente quando as cotas são habilitadas no sistema ou quando uma ou mais entradas de usuário são marcadas para exclusão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




