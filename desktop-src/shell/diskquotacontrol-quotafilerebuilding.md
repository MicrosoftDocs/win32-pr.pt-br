---
description: Obtém um valor booliano que indica se o arquivo de cota do volume está sendo recriado no momento.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Propriedade DiskQuotaControl. QuotaFileRebuilding
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
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967388"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Propriedade DiskQuotaControl. QuotaFileRebuilding

Obtém um valor booliano que indica se o arquivo de cota do volume está sendo recriado no momento.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valor da propriedade

Essa propriedade será definida como **true** se o arquivo de cota estiver sendo recompilado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O arquivo de cota é recriado automaticamente quando as cotas são habilitadas no sistema ou quando uma ou mais entradas de usuário são marcadas para exclusão.

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

 

 




