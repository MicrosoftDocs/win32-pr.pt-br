---
title: Propriedade SystemMonitor. ReadOnly
description: Recupera ou define um valor que determina se um usuário pode modificar os valores de Propriedade do controle.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Propriedade ReadOnly do SysMon
- Propriedade ReadOnly SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, propriedade ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918408"
---
# <a name="systemmonitorreadonly-property"></a>Propriedade SystemMonitor. ReadOnly

Recupera ou define um valor que determina se um usuário pode modificar os valores de Propriedade do controle.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a>Valor da propriedade

True se você não quiser que o usuário modifique os valores de Propriedade do controle; caso contrário, false. O valor padrão é false, o que significa que os usuários podem modificar os valores de Propriedade do controle.

## <a name="remarks"></a>Comentários

Quando o valor dessa propriedade for true, as seguintes condições estarão em vigor:

-   O usuário não pode usar o menu de contexto.
-   Os seguintes botões da barra de ferramentas estão desabilitados:
    -   Novo conjunto de contadores
    -   Ver atividade atual
    -   Exibir dados do arquivo de log
    -   Adicionar
    -   Excluir
    -   Colar lista de contadores
    -   Propriedades

Observe que essa propriedade afeta apenas a capacidade do usuário de modificar valores de propriedade por meio da interface do usuário; ela não impede que você modifique programaticamente os valores ou contadores de propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





