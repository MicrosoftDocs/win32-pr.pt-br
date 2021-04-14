---
description: Ativando filas de componentes
ms.assetid: cfbf7c73-2521-40cf-8c6e-436f64c07e31
title: Ativando filas de componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13dadad287facd5555b4e1ed84fee9f764b1c32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370417"
---
# <a name="activating-component-queues"></a>Ativando filas de componentes

Fazer chamadas de método em um componente enfileirado não executa diretamente o método. Em vez disso, o [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) realiza marshaling e armazena chamadas de método e parâmetros em uma fila em que eles são recuperados e executados posteriormente pelo componente enfileirado. Ao contrário da ativação de um objeto DCOM remoto, o componente em fila não é instanciado quando um método é chamado. Essa é a ideia básica por trás do uso de componentes enfileirados – os componentes em fila não precisam ser instanciados ao mesmo tempo que o aplicativo de chamada.

> [!Note]  
> As descrições para ativar um aplicativo enfileirado pressupõem que o aplicativo está marcado como enfileirado e que a caixa de seleção do ouvinte está habilitada.

 

Você pode usar scripts para iniciar e parar um aplicativo enfileirado. Você pode colocar o script sob o controle do Agendador de tarefas para executá-lo conforme necessário. Por exemplo, o script pode ser executado na reinicialização do sistema se os aplicativos estiverem permanentemente disponíveis. Se o aplicativo for processar transações no modo de lote, o script poderá ser executado em um determinado momento por dia em conjunto com um script de desligamento para garantir que o processamento em lotes seja interrompido em um momento específico.

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para iniciar um aplicativo em fila, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, em **serviços de componentes**, abra a pasta **aplicativos com+** associada ao computador que você deseja gerenciar.

2.  Clique com o botão direito do mouse no aplicativo cuja fila você deseja ativar.

3.  Clique em **Iniciar**.

## <a name="visual-basic"></a>Visual Basic

Consulte o exemplo COMAdminCatalog. StartApplication.

## <a name="cc"></a>C/C++

Consulte o exemplo [**ICOMAdminCatalog:: StartApplication**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-startapplication) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o moniker da fila](using-the-queue-moniker.md)
</dt> </dl>

 

 



