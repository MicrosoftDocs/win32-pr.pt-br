---
description: Tratamento de erros no CRM COM+
ms.assetid: 9de31fb5-31e9-494a-b61f-87bcff0d5085
title: Tratamento de erros no CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aba2b5c4541485433a85fe01fee7870c2e43f62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457057"
---
# <a name="error-handling-in-the-com-crm"></a>Tratamento de erros no CRM COM+

Aplicativos de servidor COM+ implementam uma política de FailFast. Se um erro interno sério for detectado, o processo do aplicativo do servidor será encerrado e gravará uma mensagem de erro no log de eventos do Windows. Isso permite a detecção rápida de problemas e é possível devido à proteção dos dados do aplicativo por processamento de transações. Sempre verifique o log de eventos do Windows em busca de erros do CRM, seja durante o desenvolvimento ou durante a implantação final.

Erros básicos no uso de interfaces do CRM, como argumentos inválidos ou erros de sequência (por exemplo, tentar gravar um registro de log antes de registrar o compensador de CRM), retornar códigos de erro e não devem disparar FailFast. Para o desenvolvimento de CRM, você pode optar por definir a chave do registro VTRACE1 (consulte [configurações do registro do com+ CRM](com--crm-registry-settings.md)), que faz com que uma mensagem apareça na janela de saída do depurador para cada erro.

Também podem ocorrer erros transitórios. Esses erros geralmente são causados por condições de tempo e resultam em um código de erro retornado. O desenvolvedor de CRM deve garantir que essas condições de erro sejam tratadas. Por exemplo, ao gravar um registro de log, a transação pode abortar devido a um tempo limite. O método, em seguida, retorna um erro, que o chamador deve verificar e tratar adequadamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



