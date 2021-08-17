---
description: Visão geral da Biblioteca Gerenciada e observações sobre como usar a Biblioteca Gerenciada da plataforma de Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Usando a biblioteca gerenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1241787b680045d6c84b440717ced5426e4352d8c280ef58c1bb7f75c9fc66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449237"
---
# <a name="using-the-managed-library"></a>Usando a biblioteca gerenciada

O Common Language Runtime é a base do Microsoft .NET Framework. Você pode pensar no Common Language Runtime como um agente que gerencia o código em tempo de execução, fornecendo serviços principais, como gerenciamento de memória, gerenciamento de threads e remoção, além de impor a segurança de código estrita. Na verdade, o conceito de gerenciamento de código é um princípio fundamental do Common Language Runtime. O código destinado ao Common Language Runtime é conhecido como código gerenciado. O código que não tem como destino o Common Language Runtime é conhecido como código nativo.

A biblioteca de classes framework é uma coleção abrangente e orientada a objeto de classes reutilizáveis que você pode usar para desenvolver aplicativos que vão de aplicativos tradicionais de linha de comando ou GUI (interface gráfica do usuário) a aplicativos com base nas inovações mais recentes fornecidas pelo ASP.NET e serviços Web.

A Biblioteca Gerenciada de Tablet PC contém um conjunto de objetos gerenciados que estende o Framework para fornecer suporte para entrada e saída de manuscrito no Tablet PC, bem como intercâmbio de dados com outros computadores.

## <a name="exceptions"></a>Exceções

Os objetos de biblioteca gerenciada na API do Tablet PC quebram as implementações da biblioteca COM. Quando o objeto ou controle da biblioteca COM subjacente retornar um erro, a API gerenciada lançará uma exceção Marshal.ThrowExceptionForHR que fornece os detalhes sobre a exceção COM interna. Você pode consultar os valores HRESULT na Referência da Biblioteca COM para obter detalhes sobre os possíveis erros que podem ser retornados.

## <a name="object-comparison"></a>Comparação de objetos

Para todos os objetos na biblioteca Gerenciada da Plataforma de Tablet PC, [**Equals**](/previous-versions/windows/) não é substituído para comparar corretamente dois objetos que são os mesmos. A API (interface de programação de aplicativo) gerenciada não dá suporte à comparação de objetos quanto à igualdade, seja por meio da função **Equals** ou pelo operador equals (==).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Associação à versão mais recente Microsoft.Ink.dll

O assembly Microsoft.Ink.dll mais recente é uma substituição compatível para Microsoft.Ink.dll versão 1.0 e Microsoft.Ink.15.dll. Na maioria dos casos, você não precisa fazer nenhuma alteração em seus aplicativos distribuídos com os assemblies mais antigos. No entanto, em alguns casos, você precisa instruir o carregador do Common Language Runtime a usar a DLL (biblioteca de vínculo dinâmico) mais nova onde quer que as DLLs mais antigas tenham sido referenciadas.

A única vez que você precisa se vincular explicitamente ao novo assembly usando a técnica a seguir é se o aplicativo usa um componente que faz referência ao assembly versão 1.0 ou 1.5 em combinação com um componente que faz referência a um assembly de versão mais recente, como 1.7, e se esses componentes podem trocar dados.

A melhor maneira de instruir o carregador do Common Language Runtime a usar a DLL mais nova é redirecionar versões de assembly no nível do aplicativo. Você pode especificar que seu aplicativo use a versão mais recente do assembly colocando informações de associação de assembly no arquivo de configuração do aplicativo. Para obter mais informações sobre como redirecionar versões de assembly no nível do aplicativo, consulte [Redirecionando](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue)versões de assembly , especificamente a seção "Especificando a associação de assembly em arquivos de configuração".

Você precisará criar um arquivo de configuração no mesmo diretório que o arquivo executável. O arquivo de configuração deve ter o mesmo nome que o executável, seguido pela extensão .config arquivo. Por exemplo, para um aplicativo, MyApp.exe, o arquivo de configuração deve ser o MyApp.exe.config arquivo. O arquivo de configuração usa [um elemento bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) para forçar que todas as versões anteriores sejam mapeadas para a versão mais recente, conforme mostrado no exemplo a seguir:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Para obter mais informações sobre arquivos de configuração, incluindo exemplos de como construir o linguagem XML (XML) para o arquivo de configuração, consulte [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) e [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

Os aplicativos criados com o Microsoft Windows XP Tablet PC Edition Development Kit 1.7 e versões posteriores são automaticamente vinculados à nova versão do assembly Microsoft.Ink. Para obter mais informações sobre a associação de [assembly, consulte Como o runtime localiza assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> Usar a política de aplicativo para se vincular ao assembly atualizado não funciona para aplicativos que usam a classe [Divider](/previous-versions/ms583616(v=vs.100)) ou a [classe PenInputPanel.](/previous-versions/aa514041(v=msdn.10)) Os aplicativos que usam qualquer uma dessas classes devem continuar a usar Microsoft.Ink.15.dll ou recompilar após referenciar o assembly atualizado.

 

## <a name="working-with-events"></a>Trabalhando com eventos

Se o código em um manipulador de eventos para qualquer um dos objetos gerenciados lançar uma exceção, a exceção não será entregue ao usuário. Para garantir que as exceções sejam entregues, use blocos try-catch em seus manipuladores de eventos para eventos gerenciados.

## <a name="managing-forms"></a>Gerenciando formulários

A [classe Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e suas classes base não definem um finalizador. Para limpar seus recursos em um formulário, escreva uma subclasse que fornece um finalizador (por exemplo, o destruidor C usando o ~) que chama \# [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1). Para fazer a limpeza, o finalizador substitui Dispose e, em seguida, chama a classe base Dispose. Não se refira a outros objetos que exigem o método [Finalize](/previous-versions/windows/) no método Dispose quando o parâmetro booliana for **FALSE,** porque esses objetos podem já ter sido finalizados. Para obter mais informações sobre como liberar recursos, [consulte Finalizar métodos e destruidores](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Formulários e RecognizerContext

[Os eventos RecognizerContext](/previous-versions/ms552546(v=vs.100)) são executados em um thread diferente do thread em que o formulário está. Os controles Windows Forms são vinculados a um thread específico e não são thread-safe. Portanto, você deve usar um dos métodos de invocação do controle para fazer marshal da chamada para o thread adequado. Quatro métodos em um controle são thread-safe: [os](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1)métodos Invoke , [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)e [CreateGraphics.](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) Para todas as outras chamadas de método, use um desses métodos de invocação ao chamar de um thread diferente. Para obter mais informações sobre como usar esses métodos, consulte [Manipulando controles de threads](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>Aguardando eventos

O ambiente do tablet pc é multithreaded. Use a função [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) em vez de outros métodos de espera para permitir que chamadas COM (Component Object Model) re-insuperantes entrem em seu MTA (multithreaded apartment) enquanto seu aplicativo está aguardando um evento.

## <a name="using-ink-strokes-collections"></a>Usando coleções de traços de tinta

As instâncias [de coleções strokes](/previous-versions/ms552701(v=vs.100)) obtidas de um [objeto Ink](/previous-versions/aa515768(v=msdn.10)) não são coletadas como lixo. Para evitar uma perda de memória, sempre que você está trabalhando com uma dessas coleções, use a instrução "using", conforme mostrado abaixo.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Descartar objetos e controles gerenciados

Para evitar uma perda de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer objeto ou controle tablet pc ao qual um manipulador de eventos foi anexado antes que o objeto ou controle saia do escopo.

Para melhorar o desempenho do aplicativo, descarte manualmente os seguintes objetos, controles e coleção quando eles não são mais necessários.

-   [Divisor](/previous-versions/ms583616(v=vs.100))
-   [Tinta](/previous-versions/aa515768(v=msdn.10))
-   [Inkcollector](/previous-versions/ms583683(v=vs.100))
-   [Inkedit](/previous-versions/ms552265(v=vs.100))
-   [Inkoverlay](/previous-versions/ms552322(v=vs.100))
-   [Inkpicture](/previous-versions/aa514604(v=msdn.10))
-   [Peninputpanel](/previous-versions/aa514041(v=msdn.10))
-   [Recognizercontext](/previous-versions/ms552546(v=vs.100))
-   [Traços](/previous-versions/ms552701(v=vs.100))

O exemplo C \# a seguir demonstra alguns cenários em que o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) é usado.


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 