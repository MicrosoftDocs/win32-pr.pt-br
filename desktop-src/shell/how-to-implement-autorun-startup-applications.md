---
description: Essencialmente, não há nenhuma restrição sobre como escrever um aplicativo de inicialização AutoRun.
ms.assetid: 6D95E5F0-8D93-47A8-9D8C-49CBDCA150A7
title: Como implementar aplicativos de inicialização AutoRun
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b553e102f574835103898b17558541000633412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921674"
---
# <a name="how-to-implement-autorun-startup-applications"></a>Como implementar aplicativos de inicialização AutoRun

Essencialmente, não há nenhuma restrição sobre como escrever um aplicativo de inicialização AutoRun. Você pode implementar o aplicativo de inicialização para fazer aquilo que achar necessário para instalar, desinstalar, configurar ou executar o aplicativo. No entanto, as dicas a seguir fornecem algumas diretrizes para implementar um aplicativo de inicialização de execução automática eficaz.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Certifique-se de que os usuários recebam comentários o mais rápido possível depois de inserir um disco de AutoRun na unidade. Os aplicativos de inicialização devem ser pequenos programas carregados rapidamente. Eles devem identificar claramente o aplicativo e fornecer uma maneira fácil de cancelar a operação.

### <a name="step-2"></a>Etapa 2:

Verifique se o programa já está instalado. Caso contrário, a próxima etapa provavelmente será o procedimento de instalação. O aplicativo de inicialização pode aproveitar o tempo que o usuário gasta lendo a caixa de diálogo iniciando outro thread para começar a carregar o código de instalação. Quando o usuário clicar em **OK**, seu programa de instalação já estará parcialmente se não estiver totalmente carregado. Essa abordagem reduz significativamente a percepção do usuário da quantidade de tempo que leva para carregar seu aplicativo.

> [!Note]  
> Normalmente, a parte inicial do aplicativo de inicialização apresenta aos usuários uma interface do usuário, como uma caixa de diálogo, perguntando como eles gostariam de continuar.

 

### <a name="step-3"></a>Etapa 3:

Inicie outro thread para começar a carregar o código do aplicativo para reduzir o tempo de espera do usuário. Se o aplicativo já tiver sido instalado, o usuário provavelmente inseriu o disco para executar o aplicativo.

### <a name="step-4"></a>Etapa 4:

Use as seguintes dicas para minimizar o uso do disco rígido:

-   Mantenha o número de arquivos que devem estar no disco rígido para um mínimo. Eles devem ser restritos a arquivos que são essenciais para executar o programa ou que levaria um tempo muito grande para ler a partir da mídia.
-   Em muitos casos, a instalação de arquivos não essenciais no disco rígido não é necessária, mas pode fornecer benefícios como o aumento do desempenho. Dê ao usuário a opção de decidir como fazer a compensação entre os custos e os benefícios do armazenamento de disco rígido.
-   Forneça uma maneira de desinstalar todos os componentes que foram colocados no disco rígido.
-   Se o seu aplicativo armazenar dados em cache, conceda a ele algum controle sobre ele. Inclua opções no aplicativo de inicialização, como definir um limite na quantidade máxima de dados em cache que serão armazenados no disco rígido ou fazer com que o aplicativo descarte todos os dados armazenados em cache quando ele for encerrado.

### <a name="step-5"></a>Etapa 5:

Desabilite o autorun, se necessário. O AutoRun pode ser suprimido programaticamente ou totalmente desabilitado com o registro, mesmo quando uma mídia tem um arquivo autorun. inf. Consulte [Habilitando e desabilitando o autorun](autoplay-reg.md) para obter mais informações.

 

 



