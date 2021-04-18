---
description: Cada pipe nomeado tem um nome exclusivo que o distingue de outros pipes nomeados na lista de sistemas de objetos nomeados. Um servidor de pipe especifica um nome para o pipe ao chamar a função CreateNamedPipe para criar uma ou mais instâncias de um pipe nomeado.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Nomes de pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796282"
---
# <a name="pipe-names"></a><span data-ttu-id="0786e-104">Nomes de pipe</span><span class="sxs-lookup"><span data-stu-id="0786e-104">Pipe Names</span></span>

<span data-ttu-id="0786e-105">Cada pipe nomeado tem um nome exclusivo que o distingue de outros pipes nomeados na lista de objetos nomeados do sistema.</span><span class="sxs-lookup"><span data-stu-id="0786e-105">Each named pipe has a unique name that distinguishes it from other named pipes in the system's list of named objects.</span></span> <span data-ttu-id="0786e-106">Um servidor de pipe especifica um nome para o pipe ao chamar a função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para criar uma ou mais instâncias de um pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="0786e-106">A pipe server specifies a name for the pipe when it calls the [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) function to create one or more instances of a named pipe.</span></span> <span data-ttu-id="0786e-107">Os clientes de pipe especificam o nome do pipe quando chamam a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para se conectar a uma instância do pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="0786e-107">Pipe clients specify the pipe name when they call the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function to connect to an instance of the named pipe.</span></span>

<span data-ttu-id="0786e-108">Use o seguinte formulário ao especificar o nome de um pipe na função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :</span><span class="sxs-lookup"><span data-stu-id="0786e-108">Use the following form when specifying the name of a pipe in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea), or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function:</span></span>

<span data-ttu-id="0786e-109">\\\\*Nome do Server* \\ \\*pipeName* do pipe</span><span class="sxs-lookup"><span data-stu-id="0786e-109">\\\\*ServerName*\\pipe\\*PipeName*</span></span>

<span data-ttu-id="0786e-110">em que *ServerName* é o nome de um computador remoto ou um ponto, para especificar o computador local.</span><span class="sxs-lookup"><span data-stu-id="0786e-110">where *ServerName* is either the name of a remote computer or a period, to specify the local computer.</span></span> <span data-ttu-id="0786e-111">A cadeia de caracteres do nome do pipe especificada por *pipeName* pode incluir qualquer caractere diferente de uma barra invertida, incluindo números e caracteres especiais.</span><span class="sxs-lookup"><span data-stu-id="0786e-111">The pipe name string specified by *PipeName* can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="0786e-112">A cadeia de caracteres do nome do pipe inteiro pode ter até 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0786e-112">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="0786e-113">Os nomes dos pipes não diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="0786e-113">Pipe names are not case-sensitive.</span></span>

<span data-ttu-id="0786e-114">O servidor de pipe não pode criar um pipe em outro computador, portanto, [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) deve usar um ponto para o nome do servidor, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="0786e-114">The pipe server cannot create a pipe on another computer, so [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) must use a period for the server name, as shown in the following example.</span></span>

<span data-ttu-id="0786e-115">\\\\.\\ \\*pipeName* do pipe</span><span class="sxs-lookup"><span data-stu-id="0786e-115">\\\\.\\pipe\\*PipeName*</span></span>

<span data-ttu-id="0786e-116">Um servidor de pipe pode fornecer o nome do pipe para seus clientes de pipe, para que eles possam se conectar ao pipe.</span><span class="sxs-lookup"><span data-stu-id="0786e-116">A pipe server can provide the pipe name to its pipe clients, so they can connect to the pipe.</span></span> <span data-ttu-id="0786e-117">O cliente de pipe descobre o nome do pipe de alguma fonte persistente, como uma entrada de registro, um arquivo ou outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0786e-117">The pipe client discovers the pipe name from some persistent source, such as a registry entry, a file, or another application.</span></span> <span data-ttu-id="0786e-118">Caso contrário, os clientes devem saber o nome do pipe em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="0786e-118">Otherwise, the clients must know the pipe name at compile time.</span></span>

 

 
