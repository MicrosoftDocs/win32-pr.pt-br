---
title: Registrando um retorno de chamada no Visual Basic
description: Adicionar um retorno de chamada no Visual Basic é diferente do método usado no VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa754235458820a3c16eea73eec247aed90a103f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084748"
---
# <a name="registering-a-callback-in-visual-basic"></a><span data-ttu-id="b6bcb-103">Registrando um retorno de chamada no Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b6bcb-103">Registering a Callback in Visual Basic</span></span>

<span data-ttu-id="b6bcb-104">Adicionar um retorno de chamada no Visual Basic é diferente do método usado no VBScript.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-104">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="b6bcb-105">A função **GetRef** usada no VBScript é diferente da usada em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-105">The **GetRef** function used in VBScript is different than the one used in Visual Basic.</span></span> <span data-ttu-id="b6bcb-106">Portanto, um desenvolvedor deve criar um objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenha a função de retorno de chamada como o método padrão.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-106">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="b6bcb-107">Este tópico fornece as informações necessárias para desenvolver Visual Basic aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-107">This topic provides the necessary information to develop Visual Basic applications.</span></span>

<span data-ttu-id="b6bcb-108">**Para implementar esse retorno de chamada em um aplicativo**</span><span class="sxs-lookup"><span data-stu-id="b6bcb-108">**To implement this callback in an application**</span></span>

1.  <span data-ttu-id="b6bcb-109">Adicione referências a duas bibliotecas de objetos: TLBTypes. olb e VboostTypes6. olb.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-109">Add references to two object libraries: TLBTypes.olb and VboostTypes6.olb.</span></span> <span data-ttu-id="b6bcb-110">Essas bibliotecas de objetos são fornecidas com o código de exemplo do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-110">These object libraries are provided with the Control Point sample code.</span></span>
2.  <span data-ttu-id="b6bcb-111">Adicione uma referência a Cbklib. tlb.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-111">Add a reference to Cbklib.tlb.</span></span> <span data-ttu-id="b6bcb-112">Esse arquivo define a estrutura da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-112">This file defines the structure of the callback function.</span></span>

    <span data-ttu-id="b6bcb-113">O cbklib. tlb é criado usando o arquivo cbklib. idl que é incluído como parte do código de exemplo do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-113">The cbklib.tlb is created using the cbklib.idl file that is included as part of the Control Point sample code.</span></span> <span data-ttu-id="b6bcb-114">É recomendável que o nome desse arquivo seja alterado para funções de retorno de chamada que diferem na estrutura de seus parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-114">It is recommended that the name of this file change for callback functions that differ in the structure of their parameters.</span></span> <span data-ttu-id="b6bcb-115">Este exemplo usa MIDL para criar o arquivo de biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-115">This example uses MIDL to create the type library file.</span></span>

3.  <span data-ttu-id="b6bcb-116">Escreva a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-116">Write the callback function.</span></span> <span data-ttu-id="b6bcb-117">Os parâmetros são os mesmos do exemplo do VBScript no [registro de um retorno de chamada](registering-a-callback.md).</span><span class="sxs-lookup"><span data-stu-id="b6bcb-117">The parameters are the same as in the VBScript example in [Registering a Callback](registering-a-callback.md).</span></span> <span data-ttu-id="b6bcb-118">Este exemplo imprime uma cadeia de caracteres sempre que um evento chega.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-118">This example prints a string whenever an event arrives.</span></span>
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  <span data-ttu-id="b6bcb-119">Adicione a função de retorno de chamada ao objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , conforme mostrado no exemplo a seguir, ou em outro objeto, como [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), usando a biblioteca de tipos de retorno de chamada apropriada (cbklib. tbl).</span><span class="sxs-lookup"><span data-stu-id="b6bcb-119">Add the callback function to the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object, as shown in the following example, or in another object such as [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), using the appropriate callback type library (cbklib.tbl).</span></span>
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

<span data-ttu-id="b6bcb-120">No exemplo a seguir, o objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) é passado para a função.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-120">In the following example, the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object is passed to the function.</span></span> <span data-ttu-id="b6bcb-121">A função de retorno de chamada é adicionada como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-121">The callback function is then added as the parameter.</span></span>


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a><span data-ttu-id="b6bcb-122">Bibliotecas de objetos usadas no código de exemplo</span><span class="sxs-lookup"><span data-stu-id="b6bcb-122">Object Libraries Used in the Sample Code</span></span>

<span data-ttu-id="b6bcb-123">Os exemplos anteriores e o código de exemplo do ponto de controle usam algumas das seguintes bibliotecas de objetos:</span><span class="sxs-lookup"><span data-stu-id="b6bcb-123">The previous examples and the Control Point sample code use some of the following object libraries:</span></span>

1.  <span data-ttu-id="b6bcb-124">TLBTypes. olb – essa biblioteca define alguns tipos de biblioteca e interfaces de tipo que são usados no código de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-124">TLBTypes.olb — This library defines some of the type library types and interfaces that are used in the sample code.</span></span> <span data-ttu-id="b6bcb-125">Ele define algumas das funções a serem usadas em Visual Basic, como [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), que já estão disponíveis em C ou C++.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-125">It defines some of the functions to be used in Visual Basic, such as [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), that are already available in C or C++.</span></span>
2.  <span data-ttu-id="b6bcb-126">VboostTypes6. olb – essa biblioteca define alguns tipos base que são usados em TLBTypes. olb e FunctionDelegator. bas. Mais informações sobre o TLBTypes podem ser encontradas no livro *Advanced Visual Basic 6: Power Techniques for cotidiano Programs*, by Matthew Curland (Addison-Wesley, julho de 2000, ISBN: 0-201-70712-8).</span><span class="sxs-lookup"><span data-stu-id="b6bcb-126">VboostTypes6.olb — This library defines some base types which are used in TLBTypes.olb and FunctionDelegator.bas. Further information regarding TLBTypes can be found in the book *Advanced Visual Basic 6: Power Techniques for Everyday Programs*, by Matthew Curland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span></span> <span data-ttu-id="b6bcb-127">(Este livro pode não estar disponível em alguns idiomas e países.)</span><span class="sxs-lookup"><span data-stu-id="b6bcb-127">(This book may not be available in some languages and countries.)</span></span>

<span data-ttu-id="b6bcb-128">O código de exemplo do ponto de controle e as bibliotecas a seguir estão relacionados a esta seção e são necessários para implementar esse retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b6bcb-128">The Control Point sample code and the following libraries are related to this section and are needed to implement this callback.</span></span> <span data-ttu-id="b6bcb-129">Eles podem ser encontrados com o código de exemplo do ponto de controle:</span><span class="sxs-lookup"><span data-stu-id="b6bcb-129">They can be found with the Control Point sample code:</span></span>

-   <span data-ttu-id="b6bcb-130">Cbklib. idl</span><span class="sxs-lookup"><span data-stu-id="b6bcb-130">Cbklib.idl</span></span>
-   <span data-ttu-id="b6bcb-131">Cbklib. tlb</span><span class="sxs-lookup"><span data-stu-id="b6bcb-131">Cbklib.tlb</span></span>
-   <span data-ttu-id="b6bcb-132">VboostTypes6. olb</span><span class="sxs-lookup"><span data-stu-id="b6bcb-132">VboostTypes6.olb</span></span>
-   <span data-ttu-id="b6bcb-133">TLBTypes. olb</span><span class="sxs-lookup"><span data-stu-id="b6bcb-133">TLBTypes.olb</span></span>
-   <span data-ttu-id="b6bcb-134">FunctionDelegator. bas</span><span class="sxs-lookup"><span data-stu-id="b6bcb-134">FunctionDelegator.bas</span></span>

 

 