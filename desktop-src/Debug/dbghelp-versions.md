---
description: A biblioteca DbgHelp é implementada pelo DbgHelp.dll.
ms.assetid: 8ef1740d-c791-4fbd-8297-7207a987c09d
title: Versões do DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811e92ba88bf38cb46274e2d2c716a620ea83b16
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646210"
---
# <a name="dbghelp-versions"></a><span data-ttu-id="bed3b-103">Versões do DbgHelp</span><span class="sxs-lookup"><span data-stu-id="bed3b-103">DbgHelp Versions</span></span>

<span data-ttu-id="bed3b-104">A biblioteca DbgHelp é implementada pelo DbgHelp.dll.</span><span class="sxs-lookup"><span data-stu-id="bed3b-104">The DbgHelp library is implemented by DbgHelp.dll.</span></span> <span data-ttu-id="bed3b-105">Embora essa DLL esteja incluída em todas as versões com suporte do Windows, raramente é a versão mais atual do DbgHelp disponível.</span><span class="sxs-lookup"><span data-stu-id="bed3b-105">Although this DLL is included in all supported versions of Windows, it is rarely the most current version of DbgHelp available.</span></span> <span data-ttu-id="bed3b-106">Além disso, a versão do DbgHelp que acompanha o Windows reduziu a funcionalidade de outras versões – especificamente, ela não tem suporte para servidor de símbolos e servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="bed3b-106">Furthermore, the version of DbgHelp that ships in Windows has reduced functionality from the other releases-- specifically, it lacks support for Symbol Server and Source Server.</span></span>

<span data-ttu-id="bed3b-107">As versões mais atuais do DbgHelp.dll, SymSrv.dll e SrcSrv.dll estão disponíveis como parte do pacote de [ferramentas de depuração para Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) .</span><span class="sxs-lookup"><span data-stu-id="bed3b-107">The most current versions of DbgHelp.dll, SymSrv.dll, and SrcSrv.dll are available as a part of the [Debugging Tools For Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) package.</span></span> <span data-ttu-id="bed3b-108">As políticas de redistribuição para essas DLLs incluídas foram especificamente projetadas para facilitar o máximo possível para que as pessoas incluam esses arquivos em seus próprios pacotes e versões.</span><span class="sxs-lookup"><span data-stu-id="bed3b-108">The redistribution policies for these included DLLs were specifically designed to make it as easy as possible for people to include these files in their own packages and releases.</span></span>

> [!Caution]  
> <span data-ttu-id="bed3b-109">Os usuários nunca devem tentar instalar as [ferramentas de depuração para](https://developer.microsoft.com/windows/downloads/windows-10-sdk) versões do windows do DbgHelp.dll nos diretórios de sistema do Windows porque eles não são testados nesse cenário e provavelmente desestabilizam o sistema.</span><span class="sxs-lookup"><span data-stu-id="bed3b-109">Users should never attempt to install the [Debugging Tools For Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk) versions of DbgHelp.dll into the Windows system directories because they are untested in this scenario and likely to destabilize the system.</span></span> <span data-ttu-id="bed3b-110">Há versões separadas x64 e x86 do pacote de depuração e ambas são necessárias para as pessoas interessadas em dar suporte a ambas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="bed3b-110">There are separate X64 and X86 versions of the debugging package and both are necessary for people interested in supporting both platforms.</span></span>

<span data-ttu-id="bed3b-111">Para obter a versão mais recente do DbgHelp.dll, acesse [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) e baixe as ferramentas de depuração para Windows.</span><span class="sxs-lookup"><span data-stu-id="bed3b-111">To obtain the latest version of DbgHelp.dll, go to [https://developer.microsoft.com/windows/downloads/windows-10-sdk](https://developer.microsoft.com/windows/downloads/windows-10-sdk) and download Debugging Tools for Windows.</span></span> <span data-ttu-id="bed3b-112">Consulte [chamando a biblioteca dbghelp](calling-the-dbghelp-library.md) para obter informações sobre a instalação correta.</span><span class="sxs-lookup"><span data-stu-id="bed3b-112">Refer to [Calling the DbgHelp Library](calling-the-dbghelp-library.md) for information on proper installation.</span></span>

> [!Note]  
> <span data-ttu-id="bed3b-113">O arquivo de DbgHelp.dll fornecido no Windows não é redistribuível.</span><span class="sxs-lookup"><span data-stu-id="bed3b-113">The DbgHelp.dll file that ships in Windows is not redistributable.</span></span>

<span data-ttu-id="bed3b-114">Muitas versões do DbgHelp incluem funcionalidade adicional.</span><span class="sxs-lookup"><span data-stu-id="bed3b-114">Many versions of DbgHelp include additional functionality.</span></span> <span data-ttu-id="bed3b-115">Para garantir que a versão correta do DbgHelp esteja disponível para seu aplicativo, examine as informações de requisitos na documentação de referência da API específica.</span><span class="sxs-lookup"><span data-stu-id="bed3b-115">To ensure that the correct version of DbgHelp is available for your application, review the Requirements information in the specific API reference documentation.</span></span>
