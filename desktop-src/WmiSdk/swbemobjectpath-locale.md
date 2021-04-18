---
description: A propriedade locale do objeto SWbemObjectPath contém a localidade do caminho do objeto.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propriedade SWbemObjectPath. Locale (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781610"
---
# <a name="swbemobjectpathlocale-property"></a>Propriedade SWbemObjectPath. Locale

A propriedade **locale** do objeto [**SWbemObjectPath**](swbemobjectpath.md) contém a localidade do caminho do objeto.

Quando a propriedade **SWbemObjectPath. Locale** faz parte de um objeto [**SWbemObjectPath**](swbemobjectpath.md) autônomo, ela é de leitura/gravação e pode ser usada para definir o componente de localidade do moniker.

Quando a propriedade **SWbemObjectPath. Locale** é acessada como parte de uma propriedade [**\_ SWbemObject. Path**](swbemobject-path-.md) , ela é somente leitura e relata o valor da localidade usada na associação ao namespace do qual o objeto foi obtido.

Para identificadores de localidade da Microsoft, o formato da cadeia de caracteres é "MS \_ xxxx", onde xxxx é uma cadeia de caracteres no formato hexadecimal que indica o LCID. Por exemplo, o identificador de localidade inglês americano é "MS \_ 409".

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```VB
SWbemObjectPath.Locale As String
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
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                       |
| IID<br/>                      | ISWbemObjectPath de IID \_<br/>                                                        |



 

 




