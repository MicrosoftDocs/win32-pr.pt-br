---
title: Limpeza do diretório virtual
description: O BITS estende os diretórios virtuais do IIS para dar suporte a carregamentos.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917472"
---
# <a name="virtual-directory-cleanup"></a>Limpeza do diretório virtual

O BITS estende os diretórios virtuais do IIS para dar suporte a carregamentos. Cada diretório virtual tem uma propriedade de tempo limite de sessão (a propriedade de metabase [BITSSessionTimeout](bits-iis-extension-properties.md) do IIS) que especifica o período de tempo no qual o cliente do bits deve fazer o progresso no carregamento do arquivo. Se nenhum progresso for feito durante esse período (o temporizador é redefinido quando o andamento for feito), o BITS fechará a sessão. O tempo limite da sessão padrão é de 14 dias.

O BITS adiciona um item de trabalho à [Agendador de tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cada diretório virtual que você criar e habilitar. O item de trabalho exclui os recursos associados às sessões fechadas. Por padrão, a limpeza ocorre a cada 12 horas. Se dois diretórios virtuais apontarem para o mesmo diretório físico, o processo de limpeza iniciado por um dos diretórios excluirá os recursos associados a todas as sessões fechadas no diretório físico.

Use a guia extensão BITS ou as interfaces [Agendador de tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page) para alterar o agendamento de limpeza conforme apropriado para seu aplicativo. Você também pode chamar o método [**IBITSExtensionSetup:: GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) para recuperar um ponteiro de interface para a tarefa de limpeza associada ao diretório virtual.

> [!Note]  
> Se o Agendador de Tarefas for desabilitado depois que o diretório virtual for habilitado, o processo de limpeza do diretório virtual não funcionará.

 

 

 