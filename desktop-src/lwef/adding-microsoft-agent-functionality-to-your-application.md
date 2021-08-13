---
title: Adicionando a funcionalidade do Microsoft Agent ao seu aplicativo
description: Adicionando a funcionalidade do Microsoft Agent ao seu aplicativo
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf604a7e18d67865fb50981833ce808985e455118326c4f157258543e236dd05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753125"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a>Adicionando a funcionalidade do Microsoft Agent ao seu aplicativo

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Para acessar as interfaces de servidor do Microsoft Agent, o Agent já deve estar instalado no sistema de destino. Não há suporte para a instalação que não seja usar o arquivo executável de autoinstalação do agente, como a tentativa de copiar e registrar arquivos de componente do agente. Isso garante a instalação consistente e completa. observe que o arquivo de instalação automática do microsoft Agent não será instalado no microsoft Windows 2000 e em sistemas operacionais posteriores porque essas versões do sistema operacional já incluem sua própria versão do Agent.

para instalar com êxito o agente em um sistema de destino com um sistema operacional Microsoft Windows anterior, você também deve garantir que o sistema de destino tenha uma versão recente do Microsoft Visual C++ runtime (Msvcrt.dll), a Regsvr32.dll (ferramenta de registro da microsoft) e as dlls do microsoft COM. A maneira mais fácil de garantir que os componentes necessários estejam no sistema de destino é exigir que o Microsoft Internet Explorer 3, 2 ou posterior esteja instalado. Como alternativa, você pode instalar os dois primeiros componentes que estão disponíveis como parte do Microsoft Visual C++. As DLLs COM necessárias podem ser instaladas como parte da atualização DCOM da Microsoft, disponível no site da Microsoft. Você pode encontrar mais informações e informações de licenciamento para esses componentes no site da Microsoft.

Os componentes de idioma do agente podem ser instalados da mesma maneira. Da mesma forma, você pode usar essa técnica para instalar o formato do ACS dos caracteres da Microsoft disponíveis para distribuição no site do Microsoft Agent. Os arquivos de caractere são instalados automaticamente no subdiretório de caracteres do Microsoft Agent \\ .

Como os componentes do Microsoft Agent são projetados como componentes do sistema operacional, o Agent pode não ser desinstalado. da mesma forma, onde o agent já está instalado como parte do sistema operacional Windows, o gabinete de instalação automática do agente pode não ser instalado.

Uma vez instalado, para chamar as interfaces do agente, crie uma instância do servidor e solicite um ponteiro para uma interface específica que o servidor dá suporte usando a Convenção COM padrão. Em particular, a biblioteca COM fornece uma função de API, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), que cria uma instância do objeto e retorna um ponteiro para a interface solicitada do objeto. Solicite um ponteiro para a interface [**IAgent**](iagent.md) ou [**IAgentEx**](iagentex.md) em sua chamada **CoCreateInstance** ou em uma chamada subsequente para [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

O código a seguir ilustra isso em C/C++.


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



Se o servidor do Microsoft Agent estiver em execução, essa função se conectará ao servidor; caso contrário, ele inicia o servidor.

Observe que as interfaces de servidor do Microsoft Agent geralmente incluem interfaces estendidas que incluem um sufixo "ex". Essas interfaces são derivadas de e, portanto, incluem toda a funcionalidade do, suas contrapartes não-ex. Se você quiser usar qualquer um dos recursos estendidos, use as interfaces ex.

Funções que usam ponteiros para BSTRs alocam memória usando [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring). É responsabilidade do chamador liberar essa memória usando [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring).

 

 