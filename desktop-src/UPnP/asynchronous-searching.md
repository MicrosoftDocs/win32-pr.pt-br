---
title: Pesquisa assíncrona
description: O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas. As pesquisas assíncronas retornam o controle para o aplicativo de chamada imediatamente.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3482e041798db929d1719e1a404823f161f9bf5b0e499f4eca1694df24b38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058134"
---
# <a name="asynchronous-searching"></a>Pesquisa assíncrona

O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas. As pesquisas assíncronas retornam o controle para o aplicativo de chamada imediatamente. Em seguida, o aplicativo é notificado sobre cada dispositivo individual conforme ele é encontrado, usando uma interface de retorno de chamada que o aplicativo registrou.

A pesquisa assíncrona é melhor para interfaces gráficas do usuário e aplicativos que executam monitoramento contínuo.

A estrutura geral de uma pesquisa assíncrona é:

1.  Criar um objeto de pesquisa
2.  Iniciar a pesquisa
3.  Receba notificações de retorno de chamada e execute as etapas de processamento apropriadas.
4.  Quando a pesquisa não for mais necessária, cancele a pesquisa e libere os objetos associados.

> [!Note]  
> No código de retorno de chamada, um aplicativo não pode liberar o objeto sobre o qual está recebendo uma notificação, como um novo dispositivo, nem o aplicativo pode cancelar a pesquisa.

 

## <a name="c-example"></a>Exemplo de C++

Os aplicativos C++ devem implementar um objeto de retorno de chamada para passar para a pesquisa. Consulte [pesquisando de forma assíncrona em C++](searching-asynchronously-in-c-.md) para ver o código de exemplo que ilustra essa ação.

## <a name="vbscript-example"></a>Exemplo de VBScript

O código VBScript deve passar o endereço da função de retorno de chamada.


```VB
Sub DeviceFinderCallback (device, UDN, calltype)

  select case calltype
    Case 0
      output = "Found: " & vbCrLf
      output = output & "DisplayName: " & device.FriendlyName & vbCrLf
      output = output & "Type: " & device.Type & vbCrLf
      output = output & "UDN: " & device.UniqueDeviceName & vbCrLf
      MsgBox output

    Case 1
      MsgBox "device removed: " & UDN

    Case 2
      MsgBox "search complete"

    end select
End Sub

Dim devicefinder
Dim findData

Set devicefinder = CreateObject("UPnP.UPnPDeviceFinder")

Sub StartFind()
  findData = devicefinder.CreateAsyncFind("upnp:rootdevice", 0, _
   GetRef("DeviceFinderCallback"))

  devicefinder.StartAsyncFind(findData)
End Sub

Sub StopFind()
  deviceFinder.CancelAsyncFind(findData)
End Sub
```



 

 




