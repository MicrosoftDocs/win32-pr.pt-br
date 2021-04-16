---
description: Cada propriedade em uma classe de exibição deve ter um qualificador de matriz de cadeia de caracteres chamado PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Qualificador PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765126"
---
# <a name="propertysources-qualifier"></a>Qualificador PropertySources

Cada propriedade em uma classe de exibição deve ter um qualificador de matriz de cadeia de caracteres chamado **PropertySources**. O qualificador **PropertySources** contém o nome da propriedade de classe de origem ou propriedades das quais essa propriedade de classe de exibição obtém dados. A ordem dos valores nessa matriz corresponde à ordem das classes de origem definidas para o [qualificador ViewSources](viewsources-qualifier.md). O exemplo a seguir mostra como definir uma propriedade para uma classe de exibição Union que é a União da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de dois computadores diferentes:


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



A primeira propriedade **DeviceID** corresponde à propriedade **DeviceID** da classe na primeira consulta de origem. A segunda propriedade **DeviceID** é a propriedade **DeviceID** da classe na segunda consulta de origem.

Ao definir propriedades para classes de exibição de junção, você deve definir uma propriedade de exibição separada para cada uma das propriedades de classe de origem, a menos que as propriedades de classe de origem sejam a base da classe de exibição de junção. O exemplo a seguir cria propriedades em uma classe de exibição de junção em propriedades semelhantes da classe de origem da [**\_ impressora Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e da classe de origem [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Se as duas classes de origem estiverem sendo Unidas por uma propriedade comum, você só poderá definir uma única propriedade de classe de exibição porque o valor de ambas as propriedades da classe de origem é sempre o mesmo. O exemplo a seguir mostra como unir a classe de [**\_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) e o [**\_ PrinterConfiguration do Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) por um valor de propriedade comum:


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores específicos para o provedor de exibição**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

