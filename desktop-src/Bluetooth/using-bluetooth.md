---
title: Usando Bluetooth
description: Esta seção descreve as tarefas relacionadas à gravação de aplicativos baseados em Windows para Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642907"
---
# <a name="using-bluetooth"></a><span data-ttu-id="d8b7e-103">Usando Bluetooth</span><span class="sxs-lookup"><span data-stu-id="d8b7e-103">Using Bluetooth</span></span>

<span data-ttu-id="d8b7e-104">Esta seção descreve as tarefas relacionadas à gravação de aplicativos baseados em Windows para Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="d8b7e-105">O Bluetooth fornece definições de programação nos arquivos Ws2bth. h e BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="d8b7e-106">O arquivo Bthsdpdef. h deve ser incluído antes de BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="d8b7e-107">O arquivo Ws2bth. h deve ser incluído após o Winsock2. h para usar soquetes Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="d8b7e-108">Vincule somente a bthprops. lib e evite vincular a irprops. lib.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="d8b7e-109">Irprops. lib é fornecido apenas para fins de compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="d8b7e-110">Bthprops. lib está disponível no SDK do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="d8b7e-111">Você pode usar o SDK do Windows Vista para desenvolver aplicativos para o Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="d8b7e-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="d8b7e-112">O SDK do Windows Vista está disponível no [centro de download](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span><span class="sxs-lookup"><span data-stu-id="d8b7e-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="d8b7e-113">Todos os mecanismos padrão síncronos e sobrepostos para ler e gravar dados que atualmente têm suporte com outras famílias de endereços operam corretamente com a \_ família de endereços BTH de AF.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="d8b7e-114">Há um código de exemplo incluído no SDK que mostra um aplicativo simples de Bluetooth usando o Winsock 2,2 e o protocolo RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="d8b7e-115">O código-fonte do exemplo pode ser encontrado no local de instalação do SDK em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="d8b7e-116">Esta seção descreve os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-116">This section describes the following topics.</span></span>



| <span data-ttu-id="d8b7e-117">Seção</span><span class="sxs-lookup"><span data-stu-id="d8b7e-117">Section</span></span>                                                                                      | <span data-ttu-id="d8b7e-118">Conteúdo</span><span class="sxs-lookup"><span data-stu-id="d8b7e-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="d8b7e-119">Programação de Bluetooth com Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d8b7e-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="d8b7e-120">Explica como usar as interfaces do Windows Sockets para implementar uma rede Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d8b7e-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




