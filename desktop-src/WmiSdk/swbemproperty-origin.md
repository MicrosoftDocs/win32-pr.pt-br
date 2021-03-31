---
description: A propriedade origin do objeto SWbemProperty recupera o nome da classe WMI na qual essa propriedade foi introduzida. Para classes com hierarquias de herança profundas, geralmente é desejável saber quais propriedades foram declaradas em quais classes.
ms.assetid: 25bc0303-43b8-42da-a194-82213c1009d9
ms.tgt_platform: multiple
title: Propriedade SWbemProperty. Origin (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.Origin
- ISWbemProperty.Origin
- ISWbemProperty.get_Origin
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f0aef6c1041e14d65ee3cbacaa40255421a1b064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169805"
---
# <a name="swbempropertyorigin-property"></a>Propriedade SWbemProperty. Origin

A propriedade **Origin** do objeto [**SWbemProperty**](swbemproperty.md) recupera o nome da classe WMI na qual essa propriedade foi introduzida. Para classes com hierarquias de herança profundas, geralmente é desejável saber quais propriedades foram declaradas em quais classes.

Se a propriedade for local (consulte [**SWbemQualifier. IsLocal**](swbemqualifier-islocal.md)), esse valor será o mesmo que a classe proprietária. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemProperty.Origin As String
```



## <a name="property-value"></a>Valor da propriedade

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | ISWbemProperty de IID \_<br/>                                                          |



 

 




