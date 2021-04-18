---
description: As seguintes considerações de Threading do Tablet PC são específicas para a biblioteca gerenciada.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Considerações sobre Threading de biblioteca gerenciada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764405"
---
# <a name="managed-library-threading-considerations"></a>Considerações sobre Threading de biblioteca gerenciada

As seguintes considerações de Threading do Tablet PC são específicas para a biblioteca gerenciada.

-   [Segurança de thread](#thread-safety)
-   [Aplicativos STA e MTA](#sta-and-mta-applications)
-   [Considerações de threading de Windows Forms](#windows-forms-threading-considerations)
-   [Considerações da área de transferência](#clipboard-considerations)
-   [Exceções nos manipuladores de eventos](#exceptions-within-event-handlers)
-   [Descartando objetos e controles](#disposing-objects-and-controls)
-   [APIs do StylusInput](#stylusinput-apis)

## <a name="thread-safety"></a>Thread-Safety

As classes de biblioteca gerenciada da plataforma do Tablet PC não são geralmente thread-safe. As coleções a seguir são thread-safe no nível do membro; no entanto, essas coleções não garantem que um enumerador seja protegido se outro thread operar na coleção simultaneamente:

-   [CursorButtons](/previous-versions/ms839506(v=msdn.10))
-   [Cursores](/previous-versions/ms839493(v=msdn.10))
-   [DivisionUnits](/previous-versions/ms837954(v=msdn.10))
-   [RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))
-   [Reconhecedores](/previous-versions/ms828520(v=msdn.10))
-   [Tablet](/previous-versions/ms827599(v=msdn.10))

## <a name="sta-and-mta-applications"></a>Aplicativos STA e MTA

Os aplicativos gerenciados criados usando os assistentes contidos no Microsoft Visual Studio .NET são STA (single-threaded apartment) por padrão. Você pode alterar o apartamento para seu aplicativo definindo o thread STA ou o atributo de thread MTA (multithreaded apartment) no ponto de entrada do seu aplicativo.

Se seu aplicativo for executado em um MTA, você deverá escrever código de thread-safe; no entanto, ao fazer isso, você pode melhorar certos problemas de desempenho de manipulação de eventos.

Para obter mais informações sobre o thread STA e os atributos de thread MTA, consulte [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) Class e [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.

## <a name="windows-forms-threading-considerations"></a>Considerações de threading de Windows Forms

Os controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) estendem os controles Windows Forms. Os controles de Windows Forms usam o modelo STA (single-threaded apartment) porque Windows Forms se baseiam em janelas nativas do Win32 que são inerentemente de thread único. No código gerenciado, os controles de tinta devem ser criados no mesmo thread que o thread principal para o formulário.

Em um aplicativo STA, determinados eventos acontecem em um thread que não seja o thread da interface do usuário do aplicativo. Ao chamar qualquer Windows Forms objeto ou controle, incluindo os controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) e [InkEdit](/previous-versions/ms552265(v=vs.100)) , de dentro de um manipulador de eventos do Tablet PC, use o método herdado [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) do objeto ou do controle. A propriedade [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , herdada da classe Control, pode ser usada para determinar se isso é necessário.

Por exemplo, no manipulador de eventos a seguir para o evento de [reconhecimento](/previous-versions/ms829424(v=msdn.10)) , a propriedade [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) é testada e, se for **true**, o manipulador de eventos será invocado novamente a partir do thread da interface do usuário.


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



Se você colocar um [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) no awebpagein em um navegador (consulte [controles da Web](web-controls.md)), ele será executado como um aplicativo Sta. Para aplicativos Smart Client (consulte [Sem implantação de toque](no-touch-deployment.md)), o desenvolvedor tem total controle sobre o [seja ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1). (O padrão é geralmente STA, mas pode ser MTA, dependendo da sua versão do CLR.) Para problemas de Threading que envolvem o [**RealTimeStylus**](realtimestylus-class.md), consulte [considerações de threading para as APIs StylusInput](threading-considerations-for-the-stylusinput-apis.md).

Para obter mais informações sobre como chamar Windows Forms de um aplicativo MTA, consulte [exemplo de controle de Windows Forms multithread](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).

## <a name="clipboard-considerations"></a>Considerações da área de transferência

O objeto [Clipboard](../dataxchg/clipboard.md) funciona apenas de um thread STA. Ao tentar copiar ou colar da área de transferência de um thread que não seja STA, você obtém um [ThreadStateException](/previous-versions/windows/). Se seu aplicativo for MTA, crie um thread STA para manipular as chamadas de método da área de transferência e alguns dos outros aspectos da interface do usuário do seu aplicativo.

## <a name="exceptions-within-event-handlers"></a>Exceções nos manipuladores de eventos

Não é possível acionar exceções de dentro de manipuladores de eventos do Tablet PC. Por exemplo, se um delegado de manipulador de eventos para um objeto ou uma coleção do Tablet PC tiver três manipuladores registrados e o primeiro lançar uma exceção, a seguinte sequência ocorrerá:

1.  O primeiro manipulador é encerrado.
2.  A exceção é perdida.
3.  Os manipuladores restantes não são invocados.

## <a name="disposing-objects-and-controls"></a>Descartando objetos e controles

Para evitar um vazamento de memória, você deve chamar explicitamente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) em qualquer objeto do Tablet PC ou controle ao qual um manipulador de eventos foi anexado antes que o objeto ou controle saia do escopo.

Para melhorar o desempenho em seu aplicativo, descarte manualmente qualquer objeto ou controle do Tablet PC que implemente o método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) quando o objeto ou o controle não for mais necessário.

## <a name="stylusinput-apis"></a>APIs do StylusInput

Para obter informações sobre considerações de threading para o objeto [**RealTimeStylus**](realtimestylus-class.md) e as APIs (interfaces de programação de aplicativo) do StylusInput, consulte [considerações de threading para as APIs do StylusInput](threading-considerations-for-the-stylusinput-apis.md).

 

 
