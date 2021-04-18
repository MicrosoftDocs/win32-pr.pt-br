---
description: ICE44 valida que as caixas de diálogo NewDialog, SpawnDialog e SpawnWaitDialog de referência de ControlEvents são válidas na tabela de diálogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766872"
---
# <a name="ice44"></a>ICE44

ICE44 valida que as caixas de diálogo [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)e [SpawnWaitDialog](spawnwaitdialog-controlevent.md) de referência de ControlEvents são válidas na [tabela de diálogo](dialog-table.md).

## <a name="result"></a>Resultado

ICE44 posta uma mensagem de erro se houver um evento de controle de diálogo que não faça referência a uma caixa de diálogo listada na tabela de diálogo.

## <a name="example"></a>Exemplo

ICE44 relataria os erros a seguir para o exemplo mostrado.



| Erro de ICE44                                                                                                                               | Descrição                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de controle para o controle ' Dialog1 '. ' Control1 ' é do tipo SpawnDialog, mas seu argumento Dialog2 não é uma entrada válida na tabela de diálogo. | Há uma ação SpawnDialog, SpawnWaitDialog ou NewDialog que tem um argumento que não se refere a uma caixa de diálogo na tabela de diálogo. Para corrigir esse erro, adicione um argumento que seja uma chave na tabela de diálogo.<br/> |



 

[Tabela de diálogo](dialog-table.md) (parcial)



| caixa de diálogo  | Título |
|---------|-------|
| Dialog1 |       |



 

[Tabela ControlEvent,](controlevent-table.md) (parcial)



| caixa de diálogo\_ | controle\_ | Tipo        | Argumento |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




