---
description: ICE44 valida que as caixas de diálogo NewDialog, SpawnDialog e SpawnWaitDialog de referência de ControlEvents são válidas na tabela de diálogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ee7bb074ec2dcc395cdf17750e2ab1b0364026e0f949c9b9e3f2589a8b59261
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581006"
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

 

 




