---
title: Acessando o controle de Visual Basic e outras linguagens de programação
description: Acessando o controle de Visual Basic e outras linguagens de programação
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45854b55b3826354543411c44dcd21d9f1d77e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796066"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Acessando o controle de Visual Basic e outras linguagens de programação

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Você também pode usar o controle do Microsoft Agent de Visual Basic e outras linguagens de programação. Verifique se o idioma dá suporte total à interface do controle ActiveX e siga suas convenções para adicionar e acessar controles ActiveX. Para acessar o controle, o Agent já deve estar instalado no sistema de destino.

Em seguida, você pode baixar o arquivo de gabinete de auto-instalação do agente do site (usando a opção salvar em vez de executar). Você pode incluir esse arquivo em seu programa de instalação de instalação. Sempre que for executado, ele instalará automaticamente o agente no sistema de destino. Para obter mais detalhes sobre a instalação, consulte o contrato de licença de distribuição do Microsoft Agent. Não há suporte para a instalação que não seja usar o arquivo de gabinete de auto-instalação do agente, como a tentativa de copiar e registrar arquivos de componente do agente. Isso garante a instalação consistente e completa. Observe que o arquivo de instalação automática do Microsoft Agent não será instalado no Microsoft Windows 2000 porque essa versão do sistema operacional já inclui sua própria versão do Agent.

Para instalar o agente em um sistema de destino com êxito, você também deve garantir que o sistema de destino tenha uma versão recente do tempo de execução de Microsoft Visual C++ (Msvcrt.dll), a Regsvr32.dll (ferramenta de registro da Microsoft) e as DLLs do Microsoft COM. A maneira mais fácil de garantir que os componentes necessários estejam no sistema de destino é exigir que o Microsoft Internet Explorer 3, 2 ou posterior esteja instalado. Como alternativa, você pode instalar os dois primeiros componentes que estão disponíveis como parte do Microsoft Visual C++. As DLLs COM necessárias podem ser instaladas como parte da atualização DCOM da Microsoft, disponível no site da Microsoft. Você pode encontrar mais informações e informações de licenciamento para esses componentes no site da Microsoft.

Os componentes de idioma do agente podem ser instalados da mesma maneira. Da mesma forma, você pode usar essa técnica para instalar o formato do ACS dos caracteres da Microsoft disponíveis para distribuição no site do Microsoft Agent. Os arquivos de caractere são instalados automaticamente no subdiretório de caracteres do Microsoft Agent \\ .

Como os componentes do Microsoft Agent são projetados como componentes do sistema operacional, o Agent pode não ser desinstalado. Da mesma forma, onde o Agent já está instalado como parte do sistema operacional Windows, o gabinete de instalação automática do agente pode não ser instalado.

 

 




