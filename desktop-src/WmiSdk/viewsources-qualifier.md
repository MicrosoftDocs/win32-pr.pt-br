---
description: Todas as classes de exibição devem ter um qualificador de matriz de cadeia de caracteres chamado ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Qualificador ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: b2a0cadf3e1469fbdaf347b269813e76b780348d28482a00b4de290aaf4e0f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120756"
---
# <a name="viewsources-qualifier"></a>Qualificador ViewSources

Todas as classes de exibição devem ter um qualificador de matriz de cadeia de caracteres chamado **ViewSources**. O qualificador **ViewSources** contém as consultas de origem que definem as instâncias de origem usadas na classe View. O valor do qualificador **ViewSources** é uma matriz de cadeia de caracteres que contém consultas [*linguagem WQL (WQL)*](gloss-w.md) . Você pode definir as classes de origem e restringir as instâncias de origem usadas pela sua classe de exibição com a[cláusula WHERE](where-clause.md) da [consulta com WQL](querying-with-wql.md)para criar uma exibição filtrada.

O [provedor de exibição](view-provider.md) corresponde às consultas de origem no qualificador **ViewSources** para os namespaces listados no [qualificador ViewSpaces](viewspaces-qualifier.md) na ordem em que as consultas e os namespaces são listados. O número de consultas de origem deve corresponder ao número de namespaces listados no qualificador ViewSpaces. A ordem na qual você lista as consultas de origem determina os namespaces dos quais as instâncias de origem são desenhadas.

O exemplo a seguir seleciona apenas as instâncias da classe **LocalDisk** em que o valor da propriedade **FileSystem** é "NTFS" e as instâncias da classe **RemoteDisk** em que o valor da propriedade **FreeSpace** é maior que 45 megabytes:


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> O número de consultas de origem que você pode definir para classes de exibição de junção depende do número de instâncias que essas consultas retornam e de quantas maneiras essas instâncias podem ser Unidas. O número de combinações possíveis de instâncias de origem para classes de exibição aumenta exponencialmente, portanto, mantenha as consultas de origem para as classes de exibição de junção o mais simples possível.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores específicos para o provedor de exibição**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




