---
description: O qualificador CIMType contém texto que descreve o tipo de uma propriedade.
ms.assetid: ae65d4c7-2150-489b-a368-fb38c0d1b3be
ms.tgt_platform: multiple
title: Qualificador CIMType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIMType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 522f7b3e7f5691e9552dce15b958fdb635fcae06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091788"
---
# <a name="cimtype-qualifier"></a>Qualificador CIMType

O qualificador **CIMType** contém texto que descreve o tipo de uma propriedade.

Esse texto pode ser o tipo MOF, como "String" e "sint32" ou o tipo CIM, como " \_ cadeia de caracteres CIM" e "CIM \_ sint32". Há uma correspondência um-para-um entre o qualificador **CIMType** e o tipo da propriedade usada no parâmetro *PvtType* do método [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .

As duas exceções são:

-   [*Propriedades de referência*](gloss-r.md), que têm a **\_ referência** de tipo CIM, que contém o valor "Ref: ClassName". O valor de ClassName descreve o tipo de classe da propriedade de referência.
-   Propriedades de objeto inserido, que têm o tipo de **\_ objeto CIM** .

Observe, no entanto, que o qualificador **CIMType** pode e deve ser usado para digitar uma propriedade de referência com mais precisão. Por exemplo, se a propriedade sempre se referir a instâncias da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , seu qualificador **CIMType** deverá ser definido como:


```mof
"ref:Win32_LogicalDisk"
```



Por padrão, o qualificador **CIMType** de uma propriedade de referência tem o tipo **ref**.

Assim como nas propriedades de referência, o qualificador **CIMType** deve ser usado para digitar uma propriedade de objeto inserido mais exatamente com a seguinte sintaxe:


```mof
"object:EmbedClass"
```



Como o WMI permite mais tipos do que podem ser expressos por constantes padrão com o \_ prefixo VT, o qualificador **CIMType** pode ajudar a interpretar valores de tipo. O qualificador **CIMType** é adicionado automaticamente. Para obter mais informações, consulte [MOF Data Types](mof-data-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores WMI padrão**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

