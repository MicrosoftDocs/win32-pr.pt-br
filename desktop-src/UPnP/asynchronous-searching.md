---
title: Pesquisa assíncrona
description: O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas. As pesquisas assíncronas retornam o controle para o aplicativo de chamada imediatamente.
ms.assetid: 809cfb65-9d08-427b-90d9-b8a836176341
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57377eb8ae5a49fc9bafe81f90b9ee7c602ae4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916549"
---
# <a name="asynchronous-searching"></a><span data-ttu-id="fa7fc-104">Pesquisa assíncrona</span><span class="sxs-lookup"><span data-stu-id="fa7fc-104">Asynchronous Searching</span></span>

<span data-ttu-id="fa7fc-105">O objeto localizador de dispositivo permite pesquisas síncronas e assíncronas.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="fa7fc-106">As pesquisas assíncronas retornam o controle para o aplicativo de chamada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-106">Asynchronous searches return control to the calling application immediately.</span></span> <span data-ttu-id="fa7fc-107">Em seguida, o aplicativo é notificado sobre cada dispositivo individual conforme ele é encontrado, usando uma interface de retorno de chamada que o aplicativo registrou.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-107">Then, the application is notified about each individual device as it is found, using a callback interface that the application has registered.</span></span>

<span data-ttu-id="fa7fc-108">A pesquisa assíncrona é melhor para interfaces gráficas do usuário e aplicativos que executam monitoramento contínuo.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-108">Asynchronous searching is best for graphical user interfaces, and applications that perform continuous monitoring.</span></span>

<span data-ttu-id="fa7fc-109">A estrutura geral de uma pesquisa assíncrona é:</span><span class="sxs-lookup"><span data-stu-id="fa7fc-109">The general structure of an asynchronous search is:</span></span>

1.  <span data-ttu-id="fa7fc-110">Criar um objeto de pesquisa</span><span class="sxs-lookup"><span data-stu-id="fa7fc-110">Create a search object</span></span>
2.  <span data-ttu-id="fa7fc-111">Iniciar a pesquisa</span><span class="sxs-lookup"><span data-stu-id="fa7fc-111">Start the search</span></span>
3.  <span data-ttu-id="fa7fc-112">Receba notificações de retorno de chamada e execute as etapas de processamento apropriadas.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-112">Receive callback notifications and take the appropriate processing steps.</span></span>
4.  <span data-ttu-id="fa7fc-113">Quando a pesquisa não for mais necessária, cancele a pesquisa e libere os objetos associados.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-113">When the search is no longer needed, cancel the search and release the associated objects.</span></span>

> [!Note]  
> <span data-ttu-id="fa7fc-114">No código de retorno de chamada, um aplicativo não pode liberar o objeto sobre o qual está recebendo uma notificação, como um novo dispositivo, nem o aplicativo pode cancelar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-114">In the callback code, an application cannot release the object it is receiving notification about, such as a new device, nor can the application cancel the search.</span></span>

 

## <a name="c-example"></a><span data-ttu-id="fa7fc-115">Exemplo de C++</span><span class="sxs-lookup"><span data-stu-id="fa7fc-115">C++ Example</span></span>

<span data-ttu-id="fa7fc-116">Os aplicativos C++ devem implementar um objeto de retorno de chamada para passar para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-116">C++ applications must implement a callback object to pass to the search.</span></span> <span data-ttu-id="fa7fc-117">Consulte [pesquisando de forma assíncrona em C++](searching-asynchronously-in-c-.md) para ver o código de exemplo que ilustra essa ação.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-117">See [Searching Asynchronously in C++](searching-asynchronously-in-c-.md) for sample code that illustrates this action.</span></span>

## <a name="vbscript-example"></a><span data-ttu-id="fa7fc-118">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="fa7fc-118">VBScript Example</span></span>

<span data-ttu-id="fa7fc-119">O código VBScript deve passar o endereço da função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="fa7fc-119">VBScript code must pass the address of the callback function.</span></span>


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



 

 




