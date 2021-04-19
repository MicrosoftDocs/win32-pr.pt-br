---
title: Configuração do ambiente
description: O SDK (Software Development Kit) da plataforma instalado fornece um arquivo Setenv.bat localizado no diretório raiz do SDK da plataforma que você pode executar para configurar seu ambiente para a criação de aplicativos que usam o SDK da plataforma.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755302"
---
# <a name="environment-setup"></a><span data-ttu-id="6984a-103">Configuração do ambiente</span><span class="sxs-lookup"><span data-stu-id="6984a-103">Environment Setup</span></span>

<span data-ttu-id="6984a-104">O SDK (Software Development Kit) da plataforma instalado fornece um arquivo Setenv.bat localizado no diretório raiz do SDK da plataforma que você pode executar para configurar seu ambiente para a criação de aplicativos que usam o SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="6984a-104">The installed Platform Software Development Kit (SDK) provides a Setenv.bat file located in the root directory of the Platform SDK that you can run to set up your environment for building applications that use the Platform SDK.</span></span>

## <a name="settings-and-variables"></a><span data-ttu-id="6984a-105">Configurações e variáveis</span><span class="sxs-lookup"><span data-stu-id="6984a-105">Settings and Variables</span></span>

<span data-ttu-id="6984a-106">Você também pode configurar manualmente seu ambiente adicionando algo semelhante ao seguinte ao seu arquivo de Autoexec.bat.</span><span class="sxs-lookup"><span data-stu-id="6984a-106">You can also manually set up your environment by adding something like the following to your Autoexec.bat file.</span></span> <span data-ttu-id="6984a-107">Usando o Windows, você pode editar o arquivo de Autoexec.bat para incluir esses comandos.</span><span class="sxs-lookup"><span data-stu-id="6984a-107">Using Windows, you can edit the Autoexec.bat file to include these commands.</span></span> <span data-ttu-id="6984a-108">Usando o Windows Server 2003, o Windows XP, o Windows 2000 ou o Windows NT, você pode editar ou adicionar essas configurações às suas variáveis de ambiente usando a caixa de diálogo do sistema que pode ser executada no painel de controle.</span><span class="sxs-lookup"><span data-stu-id="6984a-108">Using Windows Server 2003, Windows XP, Windows 2000, or Windows NT, you can edit or add these settings to your environment variables using the System dialog that you can run from the Control Panel.</span></span>


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



<span data-ttu-id="6984a-109">Essas configurações são apropriadas para uma plataforma Intel 80386 ou posterior que executa o Windows me, o Windows 98 ou o Windows 95 com o Microsoft Visual C++ e o SDK da plataforma instalados.</span><span class="sxs-lookup"><span data-stu-id="6984a-109">These settings are appropriate for an Intel 80386 or later platform running Windows Me, Windows 98, or Windows 95 with both Microsoft Visual C++ and the Platform SDK installed.</span></span> <span data-ttu-id="6984a-110">Por exemplo, neste sistema, Visual C++ versão 5,0 é instalada no diretório C: \\ MSDEV</span><span class="sxs-lookup"><span data-stu-id="6984a-110">For example, on this system, Visual C++ version 5.0 is installed under the C:\\MSDEV directory.</span></span> <span data-ttu-id="6984a-111">O SDK da plataforma é instalado no diretório D: \\ MSSDK</span><span class="sxs-lookup"><span data-stu-id="6984a-111">The Platform SDK is installed under the D:\\MSSDK directory.</span></span> <span data-ttu-id="6984a-112">Sua configuração de disco pode ser diferente.</span><span class="sxs-lookup"><span data-stu-id="6984a-112">Your disk configuration may be different.</span></span> <span data-ttu-id="6984a-113">Os diretórios do Platform SDK (para este exemplo, aqueles com D: \\ MSSDK neles) são todos anteriores em cada sequência de caminho.</span><span class="sxs-lookup"><span data-stu-id="6984a-113">The Platform SDK directories (for this example, those with D:\\MSSDK in them) are all earlier in each path sequence.</span></span> <span data-ttu-id="6984a-114">Essa sequência pressupõe que as compilações de linha de comando devem ser executadas na janela de prompt de comando e que os arquivos de biblioteca. h include e. lib no SDK da plataforma sejam preferidos para essas compilações.</span><span class="sxs-lookup"><span data-stu-id="6984a-114">This sequence assumes that command line compilations are intended to be run in the Command Prompt window and that the .h include and .lib library files in the Platform SDK are preferred for those compilations.</span></span>

<span data-ttu-id="6984a-115">A variável de ambiente CPU é definida para controlar as compilações do Win32, dependendo da plataforma.</span><span class="sxs-lookup"><span data-stu-id="6984a-115">The CPU environment variable is defined to control the Win32 builds, depending on the platform.</span></span> <span data-ttu-id="6984a-116">Os valores possíveis atuais incluem i386, MIPS, alfa e PPC.</span><span class="sxs-lookup"><span data-stu-id="6984a-116">Current possible values include i386, MIPS, ALPHA, and PPC.</span></span> <span data-ttu-id="6984a-117">Para obter mais informações, consulte o arquivo Win32. Mak fornecido no SDK da plataforma no \\ \\ diretório MSSDK include.</span><span class="sxs-lookup"><span data-stu-id="6984a-117">For more information, see the Win32.mak file provided in the Platform SDK in the \\MSSDK\\INCLUDE directory.</span></span> <span data-ttu-id="6984a-118">Todos os exemplos de makefile de código do tutorial do COM incluem Win32. Mak.</span><span class="sxs-lookup"><span data-stu-id="6984a-118">All of the COM tutorial code sample makefiles include Win32.mak.</span></span>

 

 




