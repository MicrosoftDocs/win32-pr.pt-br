---
description: As considerações de threading do tablet tablet a seguir são específicas para a Biblioteca Gerenciada.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considerações sobre threading de biblioteca gerenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60908618fe3b566a552167f3448ee1d4269f9246c7b08f9bb1acf3269cf2ae77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031704"
---
# <a name="managed-library-threading-considerations"></a>Considerações sobre threading de biblioteca gerenciada

As considerações de threading do tablet tablet a seguir são específicas para a Biblioteca Gerenciada.

-   [Thread-Safety](#thread-safety)
-   [Aplicativos STA e MTA](#sta-and-mta-applications)
-   [Windows Considerações sobre threading de formulários](#windows-forms-threading-considerations)
-   [Considerações sobre área de transferência](#clipboard-considerations)
-   [Exceções em manipuladores de eventos](#exceptions-within-event-handlers)
-   [Descartar objetos e controles](#disposing-objects-and-controls)
-   [StylusInput APIs](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

As classes de Biblioteca Gerenciada da Plataforma de Tablet PC geralmente não são thread-safe. As coleções a seguir são thread-safe no nível do membro; no entanto, essas coleções não garantem que um enumerador seja protegido se outro thread operar na coleção simultaneamente:

-   [Cursorbuttons](/previous-versions/ms839506(v=msdn.10))
-   [Cursores](/previous-versions/ms839493(v=msdn.10))
-   [Divisionunits](/previous-versions/ms837954(v=msdn.10))
-   [Recognitionalternates](/previous-versions/ms830115(v=msdn.10))
-   [Reconhecedores](/previous-versions/ms828520(v=msdn.10))
-   [Comprimidos](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Aplicativos STA e MTA

Aplicativos gerenciados criados usando os assistentes contidos Microsoft Visual Studio .NET são STA (single-threaded apartment) por padrão. Você pode alterar o apartment para seu aplicativo definindo o thread STA ou o atributo de thread MTA (multithreaded apartment) no ponto de entrada do seu aplicativo.

Se o aplicativo for executado em um MTA, você deverá escrever código thread-safe; no entanto, ao fazer isso, você pode melhorar determinados problemas de desempenho de manipulação de eventos.

Para obter mais informações sobre os atributos de thread STA e MTA, consulte [classe STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) e [Classe MTAThreadAttribute.](/dotnet/api/system.mtathreadattribute?view=netcore-3.1)

## <a name="windows-forms-threading-considerations"></a>Windows Considerações sobre threading de formulários

Os [controles InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) estendem os Windows Forms. Windows Os controles de formulários usam o modelo STA (single-threaded apartment) porque Windows Forms são baseados em janelas win32 nativas inerentemente single threaded. No código gerenciado, os controles de tinta devem ser criados no mesmo thread que o thread principal para o formulário.

Em um aplicativo STA, determinados eventos ocorrem em um thread diferente do thread da interface do usuário do aplicativo. Ao chamar qualquer objeto ou controle Windows Forms, incluindo os controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit,](/previous-versions/ms552265(v=vs.100)) de dentro de um manipulador de eventos do tablet PC, use o método [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) herdado do objeto ou do controle. A [propriedade InvokeRequired,](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) herdada da classe Control, pode ser usada para determinar se isso é necessário.

Por exemplo, no manipulador de eventos a seguir para o evento [Recognition,](/previous-versions/ms829424(v=msdn.10)) a propriedade [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) é testada e, se **TRUE**, o manipulador de eventos é invocado do thread de interface do usuário.


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



Se você colocar um [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) em umawebpage em um navegador (consulte [Controles da Web),](web-controls.md)ele será executado como um aplicativo STA. Para aplicativos cliente inteligentes (consulte [Sem Implantação de Toque),](no-touch-deployment.md)o desenvolvedor tem controle total sobre [o ApartmentState.](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1) (O padrão geralmente é STA, mas pode ser MTA, dependendo da sua versão do CLR.) Para problemas de threading que envolvem [**a RealTimeStylus**](realtimestylus-class.md), consulte [Considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).

Para obter mais informações sobre como chamar Windows Forms de um aplicativo MTA, consulte [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Considerações sobre área de transferência

O [objeto Clipboard](../dataxchg/clipboard.md) funciona somente de um thread STA. Ao tentar copiar ou colar da Área de Transferência de um thread que não é STA, você obterá [um ThreadStateException](/previous-versions/windows/). Se o aplicativo for MTA, crie um thread STA para lidar com as chamadas de método da Área de Transferência e alguns dos outros aspectos da interface do usuário do seu aplicativo.

## <a name="exceptions-within-event-handlers"></a>Exceções em manipuladores de eventos

As exceções não podem ser lançadas de dentro de manipuladores de eventos do tablet PC. Por exemplo, se um delegado de manipulador de eventos para um objeto ou coleção de tablet pc tiver três manipuladores registrados e o primeiro lançar uma exceção, ocorrerá a seguinte sequência:

1.  O primeiro manipulador sai.
2.  A exceção é perdida.
3.  Os manipuladores restantes não são invocados.

## <a name="disposing-objects-and-controls"></a>Descartar objetos e controles

Para evitar uma perda de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer objeto ou controle tablet pc ao qual um manipulador de eventos foi anexado antes que o objeto ou controle saia do escopo.

Para melhorar o desempenho em seu aplicativo, descarte manualmente qualquer objeto ou controle do Tablet PC que implemente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) quando o objeto ou controle não for mais necessário.

## <a name="stylusinput-apis"></a>StylusInput APIs

Para obter informações sobre considerações de threading para o objeto [**RealTimeStylus**](realtimestylus-class.md) e as APIs (interfaces de programação de aplicativo) StylusInput, consulte Considerações de threading para as [APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
