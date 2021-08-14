---
description: Essencialmente, não há restrições sobre como gravar um aplicativo de inicialização de AutoRun.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Como implementar aplicativos de inicialização de execução automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5c31f57c8a972ee6b138b55c09c432d9cf8fc1a9f33644c92c95229c344893
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350766"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Como implementar aplicativos de inicialização de execução automática

Essencialmente, não há restrições sobre como gravar um aplicativo de inicialização de AutoRun. Você pode implementar o aplicativo de inicialização para fazer o que achar necessário para instalar, desinstalar, configurar ou executar seu aplicativo. No entanto, as dicas a seguir fornecem algumas diretrizes para implementar um aplicativo de inicialização AutoRun eficaz.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Certifique-se de que os usuários recebam comentários assim que possível depois de inserirem um disco AutoRun na unidade. Os aplicativos de inicialização devem ser pequenos programas que são carregados rapidamente. Eles devem identificar claramente o aplicativo e fornecer uma maneira fácil de cancelar a operação.

### <a name="step-2"></a>Etapa 2:

Verifique se o programa já está instalado. Caso não seja, a próxima etapa provavelmente será o procedimento de instalação. O aplicativo de inicialização pode aproveitar o tempo que o usuário gasta lendo a caixa de diálogo iniciando outro thread para começar a carregar o código de instalação. Quando o usuário clicar em **OK,** seu programa de instalação já estará parcialmente se não estiver totalmente carregado. Essa abordagem reduz significativamente a percepção do usuário da quantidade de tempo necessário para carregar seu aplicativo.

> [!Note]  
> Normalmente, a parte inicial do aplicativo de inicialização apresenta aos usuários uma interface do usuário, como uma caixa de diálogo, perguntando como eles querem continuar.

 

### <a name="step-3"></a>Etapa 3:

Inicie outro thread para começar a carregar o código do aplicativo para reduzir o tempo de espera para o usuário. Se o aplicativo já tiver sido instalado, o usuário provavelmente inseriu o disco para executar o aplicativo.

### <a name="step-4"></a>Etapa 4:

Use as seguintes dicas para minimizar o uso do disco rígido:

-   Mantenha o número de arquivos que devem estar no disco rígido para um mínimo. Eles devem ser restritos a arquivos essenciais para executar o programa ou que levariam muito tempo para serem lidos da mídia.
-   Em muitos casos, a instalação de arquivos não específicos no disco rígido não é necessária, mas pode fornecer benefícios como maior desempenho. Dê ao usuário a opção de decidir como fazer a troca entre os custos e os benefícios do armazenamento em disco rígido.
-   Forneça uma maneira de desinstalar todos os componentes que foram colocados no disco rígido.
-   Se o aplicativo armazenar dados em cache, dê ao usuário algum controle sobre eles. Inclua opções no aplicativo de inicialização, como definir um limite na quantidade máxima de dados armazenados em cache que serão armazenados no disco rígido ou fazer com que o aplicativo descarte todos os dados armazenados em cache quando terminar.

### <a name="step-5"></a>Etapa 5:

Desabilite a Autorun, se necessário. A AutoRun pode ser suprimida programaticamente ou desabilitada inteiramente com o Registro, mesmo quando uma mídia tem um arquivo Autorun.inf. Consulte [Habilitando e desabilitando a AutoRun](autoplay-reg.md) para obter mais informações.

 

 



