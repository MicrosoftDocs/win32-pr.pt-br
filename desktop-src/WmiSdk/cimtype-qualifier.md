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
ms.openlocfilehash: 86fad829bf1b2391a9bc97d5c6281a67cadae7d03672e8a6eb8093b7ff6152b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131668"
---
# <a name="cimtype-qualifier"></a>Qualificador CIMType

O **qualificador CIMType** contém texto que descreve o tipo de uma propriedade.

Esse texto pode ser o tipo MOF, como "string" e "sint32" ou o tipo CIM, como "CIM \_ STRING" e "CIM \_ SINT32". Há uma correspondência um-para-um entre o qualificador **CIMType** e o tipo da propriedade usada no parâmetro *pvtType* do método [**IWbemClassObject::Get.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)

As duas exceções são:

-   [*Propriedades de*](gloss-r.md)referência , que têm o tipo **CIM \_ REFERENCE**, que contém o valor "REF:classname". O valor classname descreve o tipo de classe da propriedade de referência.
-   Propriedades do objeto inserido, que têm o **tipo DE \_ OBJETO CIM.**

No entanto, observe que o qualificador **CIMType** pode e deve ser usado para digitar uma propriedade de referência mais exatamente. Por exemplo, se a propriedade sempre se referir a instâncias da classe [**\_ LogicalDisk win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) seu qualificador **CIMType** deverá ser definido como:


```mof
"ref:Win32_LogicalDisk"
```



Por padrão, o **qualificador CIMType** de uma propriedade de referência tem o tipo **ref**.

Assim como nas propriedades de referência, o qualificador **CIMType** deve ser usado para digitar uma propriedade de objeto inserido mais exatamente com a seguinte sintaxe:


```mof
"object:EmbedClass"
```



Como o WMI permite mais tipos do que pode ser expresso por constantes padrão com o prefixo de VT, o qualificador CIMType pode ajudar a \_ interpretar valores de tipo.  O **qualificador CIMType** é adicionado automaticamente. Para obter mais informações, consulte [Tipos de dados MOF](mof-data-types.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores WMI Padrão**](standard-wmi-qualifiers.md)
</dt> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

