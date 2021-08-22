---
description: O tipo de dados de contexto de enumeração do SCE \_ \_ é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança. Ele é usado pela função de \_ informações de consulta PFSCE \_ para navegar pelo banco de dados de segurança.
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: SCE_ENUMERATION_CONTEXT (Scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b102c1eb2998f09dbe95c79c500e0bc66f4a790464071dbf9704a17a1348c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004994"
---
# <a name="sce_enumeration_context"></a>\_contexto de enumeração do SCE \_

O tipo de dados de **\_ \_ contexto de enumeração do SCE** é um identificador opaco fornecido pelo conjunto de ferramentas de configuração de segurança. Ele é usado pela função [**de \_ \_ informações de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar pelo banco de dados de segurança.


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_informações de consulta do PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

