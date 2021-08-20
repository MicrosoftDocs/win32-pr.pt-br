---
title: Limpeza de diretório virtual
description: O BITS estende os diretórios virtuais do IIS para dar suporte a uploads.
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce883bbd9f1af31bc7cafb10a2484f3a56ecbcffa7917a5a0e491a38da4701b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118422187"
---
# <a name="virtual-directory-cleanup"></a>Limpeza de diretório virtual

O BITS estende os diretórios virtuais do IIS para dar suporte a uploads. Cada diretório virtual tem uma propriedade de tempo-out de sessão (a propriedade de metabase [IIS BITSSessionTimeout)](bits-iis-extension-properties.md) que especifica o período de tempo em que o cliente BITS deve fazer progresso no carregamento do arquivo. Se nenhum progresso for feito durante esse período (o temporizador será redefinido quando o progresso for feito), o BITS fechará a sessão. O tempo de tempo de sessão padrão é de 14 dias.

O BITS adiciona um item de trabalho [ao Agendador de Tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page) para cada diretório virtual que você criar e habilitar. O item de trabalho exclui os recursos associados às sessões fechadas. Por padrão, a limpeza ocorre a cada 12 horas. Se dois diretórios virtuais apontarem para o mesmo diretório físico, o processo de limpeza iniciado por um dos diretórios excluirá os recursos associados a todas as sessões fechadas no diretório físico.

Use a guia Extensão bits ou as [interfaces Agendador de Tarefas](/windows/desktop/TaskSchd/task-scheduler-start-page) para alterar o agendamento de limpeza conforme apropriado para seu aplicativo. Você também pode chamar o método [**IBITSExtensionSetup::GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) para recuperar um ponteiro de interface para a tarefa de limpeza associada ao diretório virtual.

> [!Note]  
> Se o Agendador de Tarefas estiver desabilitado depois que o diretório virtual estiver habilitado, o processo de limpeza do diretório virtual não funcionará.

 

 

 