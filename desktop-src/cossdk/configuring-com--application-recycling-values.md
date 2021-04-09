---
description: Você pode usar os métodos a seguir para configurar valores de reciclagem de aplicativo para seu aplicativo COM+.
ms.assetid: 8f6a4879-cf4c-4171-8448-bc07371e038c
title: Configurando valores de reciclagem de aplicativo COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34c989d81f2e3486adb1d12ec76859a1d28f090
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089576"
---
# <a name="configuring-com-application-recycling-values"></a>Configurando valores de reciclagem de aplicativo COM+

Você pode usar os métodos a seguir para configurar valores de reciclagem de aplicativo para seu aplicativo COM+.

> [!Note]  
> Não é possível reciclar um aplicativo COM+ que foi configurado para ser executado como um serviço do Windows. Além disso, os aplicativos de biblioteca têm as propriedades de reciclagem e pooling de seu processo de host.

 

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para configurar a reciclagem de aplicativos para um aplicativo COM+, use as seguintes etapas:

1.  Na árvore de console da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo do servidor COM+ que você deseja reciclar e clique em **Propriedades**.

2.  Na guia **& de reciclagem de Pooling** , insira valores para o **limite de tempo de vida (minutos)**, **limite de memória (KB)**, **tempo limite de expiração (minutos)**, **limite de chamada** e **limite de ativação**, dependendo dos critérios que você deseja usar.

    -   O **limite de tempo de vida** indica o número máximo de minutos que um processo pode executar antes de ser reciclado. O intervalo válido é de 0 a 30.240 minutos (21 dias). O número padrão de minutos é 0.
    -   **Limite de memória** indica a quantidade máxima de uso de memória de processo (em kilobytes) antes de reciclar o processo. Se o uso de memória do processo exceder o número especificado por mais de um minuto, o processo será reciclado. O intervalo válido é de 0 a 1.048.576 KB, e a quantidade padrão de uso de memória é 0 KB.
    -   O **tempo limite de expiração** indica o número de minutos a aguardar, antes de ser forçado a desligar, para o lançamento de todas as referências externas a objetos no processo. O intervalo válido é de 1 a 1440 minutos (24 horas) e o tempo limite de expiração padrão é de 15 minutos. Esse valor é usado somente quando já está determinado que um processo será reciclado com base nos outros critérios.
    -   O **limite de chamada** indica o número máximo de chamadas que os objetos de aplicativo podem aceitar antes de reciclar o processo. O intervalo válido é de 0 a 1.048.576 chamadas, e o número padrão de chamadas é 0.
    -   **Limite de ativação** indica o número máximo de ativações de objeto de aplicativo a serem aceitas antes de reciclar o processo. O intervalo válido é de 0 a 1.048.576 ativações e o número padrão de ativações é 0.

    > [!Note]  
    > Quando o **limite de tempo de vida**, o **limite de memória**, o **limite de chamada** ou o valor de **limite de ativação** for definido como 0 (o valor padrão), a reciclagem do aplicativo para esse critério será desabilitada. Quando todos esses quatro critérios forem definidos como 0, a reciclagem do aplicativo será desabilitada para o aplicativo selecionado.

     

3.  Clique em **OK**.

## <a name="visual-basic"></a>Visual Basic

A função a seguir no Microsoft Visual Basic demonstra como você pode definir os valores de reciclagem do aplicativo para qualquer aplicativo do servidor COM+ que você escolher. Para usá-lo de Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+.


```VB
Function SetMyApplicationRecycling( _
  strApplicationName As String, _
  lngLifetimeLimit As Long, _
  lngMemoryLimit As Long, _
  lngCallLimit As Long, _
  lngActivationLimit As Long, _
  lngExpirationTimeout As Long _
) As Boolean  ' Return False if any errors occur.

    SetMyApplicationRecycling = False  ' Initialize the function.
    On Error GoTo My_Error_Handler  ' Initialize error handling.

    Dim objCatalog As COMAdmin.COMAdminCatalog
    Dim objAppCollection As COMAdmin.COMAdminCatalogCollection
    Dim objApplication As COMAdmin.COMAdminCatalogObject
    Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
    Set objAppCollection = objCatalog.GetCollection("Applications")
    objAppCollection.Populate
    For Each objApplication In objAppCollection
        With objApplication
            If .Name = strApplicationName Then
                .Value("RecycleLifetimeLimit") = lngLifetimeLimit
                .Value("RecycleMemoryLimit") = lngMemoryLimit
                .Value("RecycleCallLimit") = lngCallLimit
                .Value("RecycleActivationLimit") = lngActivationLimit
                .Value("RecycleExpirationTimeout") = lngExpirationTimeout
                MsgBox strApplicationName & _
                  " recycling values are now set to the following: " & _
                  vbNewLine & vbNewLine & _
                  "Lifetime Limit = " & lngLifetimeLimit & vbNewLine & _
                  "Memory Limit = " & lngMemoryLimit & vbNewLine & _
                  "Call Limit = " & lngCallLimit & vbNewLine & _
                  "Activation Limit = " & lngActivationLimit & vbNewLine _
                  & "Expiration Timeout = " & lngExpirationTimeout
                Exit For
            End If
        End With
    Next
    objAppCollection.SaveChanges
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
    SetMyApplicationRecycling = True  ' Successful end to procedure
    Exit Function
    
My_Error_Handler:  ' Replace with specific error handling.
    MsgBox "Error # " & Err.Number & " (Hex: " & Hex(Err.Number) _
      & ")" & vbNewLine & Err.Description
    Set objApplication = Nothing
    Set objAppCollection = Nothing
    Set objCatalog = Nothing
End Function

```



Para usar a função, forneça um valor de cadeia de caracteres para o nome do aplicativo e os valores inteiros para as configurações de reciclagem de aplicativo desejadas. O código de Visual Basic a seguir mostra como definir o valor de **RecycleLifetimeLimit** como 5, o valor de **RecycleMemoryLimit** como 10, o valor de **RecycleCallLimit** como 9, o valor de **RecycleActivationLimit** como 100 e o valor de **RecycleExpirationTimeout** como 15.


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de reciclagem de aplicativo COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



