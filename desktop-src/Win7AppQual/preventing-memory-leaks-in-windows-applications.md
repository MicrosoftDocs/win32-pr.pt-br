---
description: Saiba como evitar vazamentos de memória em aplicativos do Windows para plataformas Windows 7 e Windows Server 2008 R2.
ms.assetid: c5dedcab-3e6f-433f-95de-d741321c683e
title: Evitando vazamentos de memória em aplicativos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973da19d075ac94824df340d1741fd9cefb3486
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104552864"
---
# <a name="preventing-memory-leaks-in-windows-applications"></a>Evitando vazamentos de memória em aplicativos do Windows

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  

## <a name="description"></a>Descrição

Vazamentos de memória são uma classe de bugs em que o aplicativo falha ao liberar memória quando não é mais necessário. Com o tempo, as perdas de memória afetam o desempenho do aplicativo específico, bem como o sistema operacional. Um grande vazamento pode resultar em tempos de resposta inaceitáveis devido à paginação excessiva. Eventualmente, o aplicativo, bem como outras partes do sistema operacional, apresentarão falhas.

O Windows liberará toda a memória alocada pelo aplicativo no término do processo, portanto, os aplicativos de curta execução não afetarão significativamente o desempenho geral do sistema. No entanto, vazamentos em processos de execução longa, como serviços ou pares de plug-ins do Explorer, podem afetar significativamente a confiabilidade do sistema e podem forçar o usuário a reinicializar o Windows para tornar o sistema utilizável novamente.

Os aplicativos podem alocar memória em seu nome por vários meios. Cada tipo de alocação pode resultar em um vazamento se não liberado após o uso. Aqui estão alguns exemplos de padrões de alocação comuns:

-   Memória de heap por meio da função [**HeapAlloc**](/windows/win32/api/heapapi/nf-heapapi-heapalloc) ou seu tempo de execução do C/C++ equivalentes **malloc** ou **New**
-   Alocações diretas do sistema operacional por meio da função [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) .
-   Os identificadores de kernel criados por meio de APIs do Kernel32, como [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea), [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)ou [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), mantêm a memória do kernel em nome do aplicativo
-   Os identificadores GDI e USER criados por meio de APIs user32 e GDI32 (por padrão, cada processo tem uma cota de identificadores 10.000)

## <a name="best-practices"></a>Práticas Recomendadas

O monitoramento do consumo de recursos do seu aplicativo ao longo do tempo é a primeira etapa na detecção e no diagnóstico de vazamentos de memória. Use o Gerenciador de tarefas do Windows e adicione as seguintes colunas: "tamanho da confirmação", "identificadores", "objetos do usuário" e "objetos GDI". Isso permitirá que você estabeleça uma linha de base para seu aplicativo e monitore o uso de recursos ao longo do tempo.

![Captura de tela que mostra a página ' processos ' no Gerenciador de tarefas do Windows.](images/preventingmemoryleaks-windowstaskmanager.gif)

As ferramentas da Microsoft a seguir fornecem informações mais detalhadas e podem ajudar a detectar e diagnosticar vazamentos para os vários tipos de alocação em seu aplicativo:

-   O monitor de desempenho e Monitor de Recursos fazem parte do Windows 7 e podem monitorar e usar o recurso de grafo ao longo do tempo
-   A versão mais recente do Application Verifier pode diagnosticar vazamentos de heap no Windows 7
-   UMDH, que faz parte das ferramentas de depuração para Windows, analisa as alocações de memória de heap para um determinado processo e pode ajudar a encontrar vazamentos e outros padrões de uso incomuns
-   Xperf é uma ferramenta de análise de desempenho sofisticada com suporte para rastreamentos de alocação de heap
-   O heap de depuração CRT rastreia as alocações de heap e pode ajudar a criar seus próprios recursos de depuração de heap

Determinadas práticas de codificação e design podem limitar o número de vazamentos em seu código.

-   Use ponteiros inteligentes no código C++ para alocações de heap, bem como para recursos do Win32, como o **identificador** de kernel s. A biblioteca padrão C++ fornece a **classe \_ PTR automática** para alocações de heap. Para outros tipos de alocação, você precisará escrever suas próprias classes. A biblioteca do ATL fornece um conjunto avançado de classes para o gerenciamento automático de recursos para objetos de heap e identificadores de kernel
-   Use recursos intrínsecos do compilador como **\_ com \_ PTR \_ t** para encapsular os ponteiros de interface com em "apontadores inteligentes" e auxiliar com a contagem de referência. Há classes semelhantes para outros tipos de dados COM: **\_ BSTR \_ t** e **\_ Variant \_ t**
-   Monitore seu uso de memória incomum do código .NET. O código gerenciado não é imune a vazamentos de memória. Consulte ["rastrear vazamentos de memória gerenciada"](/archive/blogs/ricom/) sobre como encontrar vazamentos de GC
-   Esteja atento aos padrões de vazamento no código do lado do cliente Web. Referências circulares entre objetos COM e mecanismos de script como JScript podem causar grandes vazamentos em aplicativos Web. ["Compreendendo e resolvendo os padrões de vazamento do Internet Explorer"](/previous-versions/ms976398(v=msdn.10)) tem mais informações sobre esses tipos de vazamentos. Você pode usar o detector de vazamento de memória do JavaScript para depurar vazamentos de memória em seu código. Embora o Windows Internet Explorer 8, que é fornecido com o Windows 7, reduz a maioria desses problemas, os navegadores mais antigos ainda são vulneráveis a esses bugs
-   Evite usar vários caminhos de saída de uma função. Alocações atribuídas a variáveis no escopo de função devem ser liberadas em um bloco específico no final da função
-   Não use exceções em seu código sem liberar todas as variáveis locais em funções. Se você usar exceções nativas, libere todas as suas alocações dentro do \_ \_ bloco finally. Se você usar exceções do C++, todas as alocações de heap e de identificador precisam ser encapsuladas em ponteiros inteligentes
-   Não descartar ou reinicializar um objeto [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) sem chamar a função [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

## <a name="links-to-resources"></a>Links para recursos

*Padrões comuns de alocação:*

-   [**Função de alocação de heap**](/windows/win32/api/heapapi/nf-heapapi-heapalloc)
-   [**Função de alocação de memória**](https://msdn.microsoft.com/library/6ewkz86d(v=VS.71).aspx)
-   [**Novo operador (C++)**](https://msdn.microsoft.com/library/kewsb8ba(v=VS.71).aspx)
-   [**Função de alocação virtual**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)
-   [Objetos kernel](../sysinfo/kernel-objects.md)
-   [Identificadores de objeto GDI](../sysinfo/gdi-objects.md)
-   [Identificadores de objeto da interface do usuário](../sysinfo/user-objects.md)

*Ferramentas da Microsoft:*

-   [Application Verifier](application-verifier.md)
-   [Ferramentas de Depuração para Windows](/windows-hardware/drivers/debugger/)
-   [Heap de despejo do modo de usuário](/windows-hardware/drivers/debugger/umdh)
-   [Ferramenta de captura, processamento e análise de rastreamento](https://msdn.microsoft.com/performance/cc825801.aspx)
-   [Heap de depuração CRT](/visualstudio/debugger/crt-debug-heap-details?view=vs-2015)

*Links adicionais:*

-   [**\_classe PTR automaticamente**](https://msdn.microsoft.com/library/ew3fk483(v=VS.71).aspx)
-   [Classes de memória Active Template Library (ATL)](https://msdn.microsoft.com/library/44yh1z4f(v=VS.71).aspx)
-   [**\_\_objeto PTR \_ t**](https://msdn.microsoft.com/library/417w8b3b(v=VS.71).aspx)
-   [**\_\_classe-t BSTR**](https://msdn.microsoft.com/library/zthfhkd6(v=VS.71).aspx)
-   [**\_\_classe variante YT**](https://msdn.microsoft.com/library/x295h94e(v=VS.71).aspx)
-   ["Rastreando vazamentos de memória gerenciada"](/archive/blogs/ricom/)
-   ["Compreendendo e resolvendo os padrões de vazamento do Internet Explorer"](/previous-versions/ms976398(v=msdn.10))
-   ["Detector de vazamento de memória do JavaScript"](/archive/blogs/gpde/new-javascript-memory-leak-detector-from-our-team)
-   [Mitigação de vazamento de memória circular (em navegadores):](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd361842(v=vs.85))
-   [**Instrução try-finally**](https://msdn.microsoft.com/library/yb3kz605(v=VS.71).aspx)
-   [**Estrutura PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)
-   [**Função PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)

 

 
