---
title: Acessando o controle de Visual Basic e outras linguagens de programação
description: Acessando o controle de Visual Basic e outras linguagens de programação
ms.assetid: 869b8eb1-1f40-4d87-8501-e41d6c0a3a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fe0c5e7548283a84edff1fb3ded488c1367087e12c15d1578629ce80b51297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976856"
---
# <a name="accessing-the-control-from-visual-basic-and-other-programming-languages"></a>Acessando o controle de Visual Basic e outras linguagens de programação

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Você também pode usar o controle do Microsoft Agent de Visual Basic outras linguagens de programação. Certifique-se de que o idioma seja totalmente compatível com a interface de controle ActiveX e siga suas convenções para adicionar e acessar ActiveX controles. Para acessar o controle, o Agent já deve estar instalado no sistema de destino.

Em seguida, você pode baixar o arquivo de gabinete de auto-instalação do Agent do site (usando a opção Salvar em vez de Executar). Você pode incluir esse arquivo em seu programa de instalação. Sempre que ele for executado, ele instalará automaticamente o Agent no sistema de destino. Para obter mais detalhes sobre a instalação, consulte o Contrato de licença de distribuição do Microsoft Agent. Não há suporte para a instalação além do uso do arquivo de gabinete de instalação automática do Agent, como a tentativa de copiar e registrar arquivos de componente do Agent. Isso garante uma instalação consistente e completa. Observe que o arquivo de auto-instalação do Microsoft Agent não será instalado no Microsoft Windows 2000 porque essa versão do sistema operacional já inclui sua própria versão do Agent.

Para instalar o Agent com êxito em um sistema de destino, você também deve garantir que o sistema de destino tenha uma versão recente do runtime do Microsoft Visual C++ (Msvcrt.dll), da ferramenta de registro da Microsoft (Regsvr32.dll) e das dlls do Microsoft COM. A maneira mais fácil de garantir que os componentes necessários estão no sistema de destino é exigir que o Microsoft Internet Explorer 3.02 ou posterior seja instalado. Como alternativa, você pode instalar os dois primeiros componentes que estão disponíveis como parte do Microsoft Visual C++. As dlls COM necessárias podem ser instaladas como parte da atualização do Microsoft DCOM, disponível no site da Microsoft. Você pode encontrar mais informações e informações de licenciamento para esses componentes no site da Microsoft.

Os componentes de linguagem do agente podem ser instalados da mesma maneira. Da mesma forma, você pode usar essa técnica para instalar o formato ACS dos caracteres da Microsoft disponíveis para distribuição no site do Microsoft Agent. Os arquivos de caractere são instalados automaticamente no \\ subdiretório Chars do Microsoft Agent.

Como os componentes do Microsoft Agent são projetados como componentes do sistema operacional, o Agent pode não ser desinstalado. Da mesma forma, em que o Agent já está instalado como parte do sistema operacional Windows, o gabinete de auto-instalação do Agent pode não ser instalado.

 

 




