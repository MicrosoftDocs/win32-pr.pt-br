---
description: Você pode filtrar as instâncias de uma classe de exibição de junção atribuindo uma consulta WQL ao qualificador PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Qualificador PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: be491c0bfefe77c2bf016789786212047d5ca8d00570c84057b8e8e346fb382e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317020"
---
# <a name="postjoinfilter-qualifier"></a>Qualificador PostJoinFilter

Você pode filtrar as instâncias de uma classe de exibição de junção atribuindo uma consulta WQL ao qualificador **PostJoinFilter** . O valor da consulta WQL é aplicado às instâncias da classe de exibição de junção. Você pode usar esse qualificador para restringir as instâncias de sua classe de exibição àquelas que atendem a condições específicas. A consulta WQL a seguir filtra instâncias de uma classe de junção chamada com base em instâncias do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



Há várias restrições ao uso deste qualificador:

-   **PostJoinFilter** só está disponível para unir classes de exibição.
-   O nome da classe e os nomes de propriedade especificados na consulta referem-se às propriedades da classe View, não à classe Source.
-   Nenhuma exclusão de propriedades é permitida; somente `SELECT *` consultas de tipo são permitidas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Qualificadores específicos para o provedor de exibição**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

