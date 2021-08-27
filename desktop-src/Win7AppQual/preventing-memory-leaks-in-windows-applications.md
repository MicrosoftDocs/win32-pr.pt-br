---
description: Saiba como evitar vazamentos de memória em Windows aplicativos para plataformas Windows 7 e Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Impedindo vazamentos de memória em Windows aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef336c52ff4869ae9947b898e8a42c480be58054315de0180ec6a18f8c917f51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994787"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Impedindo vazamentos de memória em Windows aplicativos

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** – Windows 7  
**Servidores** – Windows Server 2008 R2  

## <a name="description"></a>Descrição

Vazamentos de memória são uma classe de bugs em que o aplicativo falha ao liberar memória quando não é mais necessário. Ao longo do tempo, os vazamentos de memória afetam o desempenho do aplicativo específico, bem como do sistema operacional. Uma grande perda pode resultar em tempos de resposta inaceitáveis devido à pa paging excessiva. Eventualmente, o aplicativo, bem como outras partes do sistema operacional, terão falhas.

Windows liberará toda a memória alocada pelo aplicativo na terminação do processo, portanto, aplicativos de execução curta não afetarão significativamente o desempenho geral do sistema. No entanto, vazamentos em processos de execução longa, como serviços ou até mesmo plug-ins do Explorer, podem afetar muito a confiabilidade do sistema e podem forçar o usuário a reinicializar Windows para tornar o sistema acessível novamente.

Os aplicativos podem alocar memória em seu nome por vários meios. Cada tipo de alocação pode resultar em um vazamento se não for liberado após o uso. Aqui estão alguns exemplos de padrões de alocação comuns:

-   Memória de heap por meio [**da função HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) ou seus equivalentes de runtime C/C++ **malloc** ou **new**
-   Alocações diretas do sistema operacional por meio [**da função VirtualAlloc.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   Os alças de kernel criados por meio de APIs kernel32, como [**CreateFile,**](/windows/win32/api/fileapi/nf-fileapi-createfilea) [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)ou [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)resdam a memória do kernel em nome do aplicativo
-   Alças GDI e USER criadas por meio de APIs User32 e Gdi32 (por padrão, cada processo tem uma cota de 10.000 alças)

## <a name="best-practices"></a>Práticas Recomendadas

Monitorar o consumo de recursos do aplicativo ao longo do tempo é a primeira etapa para detectar e diagnosticar vazamentos de memória. Use Windows Gerenciador de Tarefas e adicione as seguintes colunas: "Tamanho da Confirmação", "Alças", "Objetos de Usuário" e "Objetos GDI". Isso permitirá que você estabeleça uma linha de base para seu aplicativo e monitore o uso de recursos ao longo do tempo.

![Captura de tela que mostra a página "Processos" Windows Gerenciador de Tarefas.](images/preventingmemoryleaks-windowstaskmanager.gif)

As seguintes ferramentas da Microsoft fornecem informações mais detalhadas e podem ajudar a detectar e diagnosticar vazamentos para os vários tipos de alocação em seu aplicativo:

-   Monitor de Desempenho e Monitor de Recursos fazem parte do Windows 7 e podem monitorar e usar recursos de grafo ao longo do tempo
-   A versão mais recente do Application Verifier pode diagnosticar vazamentos de heap Windows 7
-   UMDH, que faz parte das Ferramentas de Depuração para Windows, analisa as alocações de memória de heap para um determinado processo e pode ajudar a encontrar vazamentos e outros padrões de uso incomuns
-   O Xperf é uma ferramenta de análise de desempenho sofisticada com suporte para rastreamentos de alocação de heap
-   O Heap de Depuração CRT rastreia alocações de heap e pode ajudar a criar seus próprios recursos de depuração de heap

Determinadas práticas de codificação e design podem limitar o número de vazamentos em seu código.

-   Use ponteiros inteligentes no código C++ tanto para alocações de heap quanto para recursos win32, como **HANDLE** de kernel. A biblioteca padrão C++ fornece a **classe \_ ptr** automática para alocações de heap. Para outros tipos de alocação, você precisará escrever suas próprias classes. A biblioteca atl fornece um conjunto rico de classes para o gerenciamento automático de recursos para objetos de heap e alças de kernel
-   Use recursos intrínsecos do compilador, como **\_ com \_ ptr \_ t,** para encapsular seus ponteiros de interface COM em "ponteiros inteligentes" e auxiliar na contagem de referências. Há classes semelhantes para outros tipos de dados COM: **\_ bstr \_ t** e **\_ variant \_ t**
-   Monitore o uso incomum de memória do código .NET. O código gerenciado não está sujeito a vazamentos de memória. Consulte ["Acompanhamento de vazamentos de memória gerenciada"](/archive/blogs/ricom/) sobre como localizar vazamentos de GC
-   Esteja ciente dos padrões de vazamento no código do lado do cliente da Web. Referências circulares entre objetos COM e mecanismos de script como JScript podem causar grandes vazamentos em aplicativos Web. ["Noções básicas e Internet Explorer padrões de vazamento"](/previous-versions/ms976398(v=msdn.10)) tem mais informações sobre esses tipos de vazamentos. Você pode usar o Detector de Vazamento de Memória javaScript para depurar vazamentos de memória em seu código. Embora Windows Internet Explorer 8, que está sendo Windows 7, reduz a maioria desses problemas, navegadores mais antigos ainda são vulneráveis a esses bugs
-   Evite usar vários caminhos de saída de uma função. As alocações atribuídas a variáveis no escopo da função devem ser liberadas em um bloco específico no final da função
-   Não use exceções em seu código sem liberar todas as variáveis locais em funções. Se você usar exceções nativas, livre todas as alocações dentro do \_ \_ bloco finally. Se você usar exceções do C++, todas as alocações de heap e de lidar precisarão ser envolvidas em ponteiros inteligentes
-   Não descartar ou reinicializar um objeto [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sem chamar a [**função PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Links para recursos

*Padrões comuns de alocação:*

-   [**Função de alocação de heap**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Função de alocação de memória**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**Operador New (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Função de alocação virtual**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Objetos kernel](../sysinfo/kernel-objects.md)
-   [Identificador de objeto GDI](../sysinfo/gdi-objects.md)
-   [Interface do Usuário identificador de objeto](../sysinfo/user-objects.md)

*Ferramentas da Microsoft:*

-   [Application Verifier](application-verifier.md)
-   [Ferramentas de Depuração para Windows](/windows-hardware/drivers/debugger/)
-   [Heap de despejo do modo de usuário](/windows-hardware/drivers/debugger/umdh)
-   [Ferramenta de Captura, Processamento e Análise de Rastreamento](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [Heap de depuração CRT](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Links adicionais:*

-   [**Classe \_ auto ptr**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [classes de memória Active Template Library (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_objeto \_ com ptr \_ t**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_Classe bstr \_ t**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_Classe \_ variant yt**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Acompanhamento de vazamentos de memória gerenciada"](/archive/blogs/ricom/)
-   ["Noções básicas e Internet Explorer padrões de vazamento"](/previous-versions/ms976398(v=msdn.10))
-   ["Detector de Vazamento de Memória javaScript"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Mitigação de vazamento de memória circular (em navegadores):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**Instrução try-finally**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**Estrutura PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**Função PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
