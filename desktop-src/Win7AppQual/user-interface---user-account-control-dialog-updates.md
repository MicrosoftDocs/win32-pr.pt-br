---
description: Interface do usuário – atualizações da caixa de diálogo controle de conta de usuário
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Interface do usuário – atualizações da caixa de diálogo controle de conta de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7a7337c93410056b871a5893188fffc74ec759f8bebb0c1ef8392e17ba6409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328622"
---
# <a name="user-interface---user-account-control-dialog-updates"></a>Interface do usuário – atualizações da caixa de diálogo controle de conta de usuário

## <a name="affected-platforms"></a>Plataformas afetadas

**clientes** -Windows 7  
**servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -baixa  
**Frequência** -média  











## <a name="description"></a>Descrição

no Windows 7, nós padronizamos as opções da caixa de diálogo UAC. Anteriormente, os usuários tinham que selecionar entre várias opções, por exemplo, "continuar", "Cancelar" e assim por diante. Agora, todas as caixas de diálogo fornecem aos usuários um simples "Sim" ou "não". O layout da caixa de diálogo agora também mostra claramente o nome do programa, o editor e a origem.

## <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

os requisitos de desenvolvimento de aplicativos no Windows 7 para compatibilidade com o UAC são os mesmos que no Windows Vista. Windows os aplicativos compatíveis com o Vista irão interagir com o UAC no Windows 7 sem nenhuma modificação. consulte os tópicos de controle de conta de usuário no Windows o guia de *compatibilidade de aplicativos do Vista* para obter informações sobre como fazer com que os aplicativos Windows XP funcionem corretamente no Windows 7. embora as melhorias do UAC para o Windows 7 tenham impacto sobre a experiência do usuário, elas não afetarão a interface do aplicativo. No entanto, se houver qualquer conteúdo de ajuda vinculado às caixas de diálogo do UAC, talvez seja necessário atualizar as capturas de tela.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Windows Manual de compatibilidade de aplicativos vista](/previous-versions/bb757005(v=msdn.10))
-   [Download de Toolkit de compatibilidade de aplicativos](/windows-hardware/get-started/adk-install)
-   [Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))

> [!Note]  
> Esses recursos podem não estar disponíveis em alguns idiomas e países/regiões.

 

 

 
