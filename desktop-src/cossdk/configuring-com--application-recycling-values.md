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
# <a name="configuring-com-application-recycling-values"></a><span data-ttu-id="7b7dc-103">Configurando valores de reciclagem de aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="7b7dc-103">Configuring COM+ Application Recycling Values</span></span>

<span data-ttu-id="7b7dc-104">Você pode usar os métodos a seguir para configurar valores de reciclagem de aplicativo para seu aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-104">You can use the following methods to configure application recycling values for your COM+ application.</span></span>

> [!Note]  
> <span data-ttu-id="7b7dc-105">Não é possível reciclar um aplicativo COM+ que foi configurado para ser executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-105">You cannot recycle a COM+ application that has been configured to run as a Windows service.</span></span> <span data-ttu-id="7b7dc-106">Além disso, os aplicativos de biblioteca têm as propriedades de reciclagem e pooling de seu processo de host.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-106">Also, library applications have the recycling and pooling properties of their host process.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="7b7dc-107">Ferramenta administrativa serviços de componentes</span><span class="sxs-lookup"><span data-stu-id="7b7dc-107">Component Services Administrative Tool</span></span>

<span data-ttu-id="7b7dc-108">Para configurar a reciclagem de aplicativos para um aplicativo COM+, use as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="7b7dc-108">To configure application recycling for a COM+ application, use the following steps:</span></span>

1.  <span data-ttu-id="7b7dc-109">Na árvore de console da ferramenta administrativa serviços de componentes, clique com o botão direito do mouse no aplicativo do servidor COM+ que você deseja reciclar e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-109">In the console tree of the Component Services administrative tool, right-click the COM+ server application you want to be recycled and then click **Properties**.</span></span>

2.  <span data-ttu-id="7b7dc-110">Na guia **& de reciclagem de Pooling** , insira valores para o **limite de tempo de vida (minutos)**, **limite de memória (KB)**, **tempo limite de expiração (minutos)**, **limite de chamada** e **limite de ativação**, dependendo dos critérios que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-110">On the **Pooling & Recycling** tab, enter values for **Lifetime Limit (minutes)**, **Memory Limit (KB)**, **Expiration Timeout (minutes)**, **Call Limit**, and **Activation Limit**, depending on the criteria you want to use.</span></span>

    -   <span data-ttu-id="7b7dc-111">O **limite de tempo de vida** indica o número máximo de minutos que um processo pode executar antes de ser reciclado.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-111">**Lifetime Limit** indicates the maximum number of minutes a process can run before it's recycled.</span></span> <span data-ttu-id="7b7dc-112">O intervalo válido é de 0 a 30.240 minutos (21 dias).</span><span class="sxs-lookup"><span data-stu-id="7b7dc-112">The valid range is 0 through 30,240 minutes (21 days).</span></span> <span data-ttu-id="7b7dc-113">O número padrão de minutos é 0.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-113">The default number of minutes is 0.</span></span>
    -   <span data-ttu-id="7b7dc-114">**Limite de memória** indica a quantidade máxima de uso de memória de processo (em kilobytes) antes de reciclar o processo.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-114">**Memory Limit** indicates the maximum amount of process memory usage (in kilobytes) before recycling the process.</span></span> <span data-ttu-id="7b7dc-115">Se o uso de memória do processo exceder o número especificado por mais de um minuto, o processo será reciclado.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-115">If the process's memory usage exceeds the specified number for longer than one minute, the process is recycled.</span></span> <span data-ttu-id="7b7dc-116">O intervalo válido é de 0 a 1.048.576 KB, e a quantidade padrão de uso de memória é 0 KB.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-116">The valid range is 0 through 1,048,576 KB, and the default amount of memory usage is 0 KB.</span></span>
    -   <span data-ttu-id="7b7dc-117">O **tempo limite de expiração** indica o número de minutos a aguardar, antes de ser forçado a desligar, para o lançamento de todas as referências externas a objetos no processo.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-117">**Expiration Timeout** indicates the number of minutes to wait, before being forcibly shut down, for the release of all external references to objects in the process.</span></span> <span data-ttu-id="7b7dc-118">O intervalo válido é de 1 a 1440 minutos (24 horas) e o tempo limite de expiração padrão é de 15 minutos.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-118">The valid range is 1 through 1440 minutes (24 hours), and the default expiration time-out is 15 minutes.</span></span> <span data-ttu-id="7b7dc-119">Esse valor é usado somente quando já está determinado que um processo será reciclado com base nos outros critérios.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-119">This value is used only when it is already determined that a process will be recycled based on the other criteria.</span></span>
    -   <span data-ttu-id="7b7dc-120">O **limite de chamada** indica o número máximo de chamadas que os objetos de aplicativo podem aceitar antes de reciclar o processo.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-120">**Call Limit** indicates the maximum number of calls that application objects can accept before recycling the process.</span></span> <span data-ttu-id="7b7dc-121">O intervalo válido é de 0 a 1.048.576 chamadas, e o número padrão de chamadas é 0.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-121">The valid range is 0 through 1,048,576 calls, and the default number of calls is 0.</span></span>
    -   <span data-ttu-id="7b7dc-122">**Limite de ativação** indica o número máximo de ativações de objeto de aplicativo a serem aceitas antes de reciclar o processo.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-122">**Activation Limit** indicates the maximum number of application object activations to accept before recycling the process.</span></span> <span data-ttu-id="7b7dc-123">O intervalo válido é de 0 a 1.048.576 ativações e o número padrão de ativações é 0.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-123">The valid range is 0 through 1,048,576 activations, and the default number of activations is 0.</span></span>

    > [!Note]  
    > <span data-ttu-id="7b7dc-124">Quando o **limite de tempo de vida**, o **limite de memória**, o **limite de chamada** ou o valor de **limite de ativação** for definido como 0 (o valor padrão), a reciclagem do aplicativo para esse critério será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-124">When the **Lifetime Limit**, **Memory Limit**, **Call Limit**, or **Activation Limit** value is set to 0 (the default value), application recycling for that criterion is disabled.</span></span> <span data-ttu-id="7b7dc-125">Quando todos esses quatro critérios forem definidos como 0, a reciclagem do aplicativo será desabilitada para o aplicativo selecionado.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-125">When all four of these criteria are set to 0, application recycling is disabled for the selected application.</span></span>

     

3.  <span data-ttu-id="7b7dc-126">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-126">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="7b7dc-127">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="7b7dc-127">Visual Basic</span></span>

<span data-ttu-id="7b7dc-128">A função a seguir no Microsoft Visual Basic demonstra como você pode definir os valores de reciclagem do aplicativo para qualquer aplicativo do servidor COM+ que você escolher.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-128">The following function in Microsoft Visual Basic demonstrates how you can set the application recycling values for any COM+ server application that you choose.</span></span> <span data-ttu-id="7b7dc-129">Para usá-lo de Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-129">To use it from Visual Basic, add a reference to the COM+ Admin Type Library.</span></span>


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



<span data-ttu-id="7b7dc-130">Para usar a função, forneça um valor de cadeia de caracteres para o nome do aplicativo e os valores inteiros para as configurações de reciclagem de aplicativo desejadas.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-130">To use the function, provide a string value for the application name and integer values for the desired application recycling settings.</span></span> <span data-ttu-id="7b7dc-131">O código de Visual Basic a seguir mostra como definir o valor de **RecycleLifetimeLimit** como 5, o valor de **RecycleMemoryLimit** como 10, o valor de **RecycleCallLimit** como 9, o valor de **RecycleActivationLimit** como 100 e o valor de **RecycleExpirationTimeout** como 15.</span><span class="sxs-lookup"><span data-stu-id="7b7dc-131">The following Visual Basic code shows how to set the **RecycleLifetimeLimit** value to 5, the **RecycleMemoryLimit** value to 10, the **RecycleCallLimit** value to 9, the **RecycleActivationLimit** value to 100, and the **RecycleExpirationTimeout** value to 15.</span></span>


```VB
Sub Main()
    If Not SetMyApplicationRecycling("MyApp", 5, 10, 9, 100, 15) Then
        MsgBox "SetMyApplicationRecycling failed."
    End If
End Sub

```



## <a name="related-topics"></a><span data-ttu-id="7b7dc-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b7dc-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7dc-133">Conceitos de reciclagem de aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="7b7dc-133">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



