---
title: Registrando um retorno de chamada no Visual Basic
description: adicionar um retorno de chamada no Visual Basic é diferente do método usado no VBScript.
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7145a6c6ef80ede3ea2fdb1fd62a2661142fb6f0a85454389fe1c09c117e5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126219"
---
# <a name="registering-a-callback-in-visual-basic"></a>Registrando um retorno de chamada no Visual Basic

adicionar um retorno de chamada no Visual Basic é diferente do método usado no VBScript. A função **GetRef** usada no VBScript é diferente da usada em Visual Basic. Portanto, um desenvolvedor deve criar um objeto [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que tenha a função de retorno de chamada como o método padrão. este tópico fornece as informações necessárias para desenvolver Visual Basic aplicativos.

**Para implementar esse retorno de chamada em um aplicativo**

1.  Adicione referências a duas bibliotecas de objetos: TLBTypes. olb e VboostTypes6. olb. Essas bibliotecas de objetos são fornecidas com o código de exemplo do ponto de controle.
2.  Adicione uma referência a Cbklib. tlb. Esse arquivo define a estrutura da função de retorno de chamada.

    O cbklib. tlb é criado usando o arquivo cbklib. idl que é incluído como parte do código de exemplo do ponto de controle. É recomendável que o nome desse arquivo seja alterado para funções de retorno de chamada que diferem na estrutura de seus parâmetros. Este exemplo usa MIDL para criar o arquivo de biblioteca de tipos.

3.  Escreva a função de retorno de chamada. Os parâmetros são os mesmos do exemplo do VBScript no [registro de um retorno de chamada](registering-a-callback.md). Este exemplo imprime uma cadeia de caracteres sempre que um evento chega.
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

    

4.  Adicione a função de retorno de chamada ao objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) , conforme mostrado no exemplo a seguir, ou em outro objeto, como [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), usando a biblioteca de tipos de retorno de chamada apropriada (cbklib. tbl).
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

    

No exemplo a seguir, o objeto [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) é passado para a função. A função de retorno de chamada é adicionada como o parâmetro.


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>Bibliotecas de objetos usadas no código de exemplo

Os exemplos anteriores e o código de exemplo do ponto de controle usam algumas das seguintes bibliotecas de objetos:

1.  TLBTypes. olb – essa biblioteca define alguns tipos de biblioteca e interfaces de tipo que são usados no código de exemplo. ele define algumas das funções a serem usadas em Visual Basic, como [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), que já estão disponíveis em C ou C++.
2.  VboostTypes6. olb – essa biblioteca define alguns tipos base que são usados em TLBTypes. olb e FunctionDelegator. bas. mais informações sobre o TLBTypes podem ser encontradas no livro *Advanced Visual Basic 6: Power techniques for cotidiano programs*, by Matthew Curland (Addison-Wesley, julho de 2000, ISBN: 0-201-70712-8). (Este livro pode não estar disponível em alguns idiomas e países.)

O código de exemplo do ponto de controle e as bibliotecas a seguir estão relacionados a esta seção e são necessários para implementar esse retorno de chamada. Eles podem ser encontrados com o código de exemplo do ponto de controle:

-   Cbklib. idl
-   Cbklib. tlb
-   VboostTypes6. olb
-   TLBTypes. olb
-   FunctionDelegator. bas

 

 