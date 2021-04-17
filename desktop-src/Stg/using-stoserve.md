---
title: Usando StoServe
description: StoServe é uma DLL que se destina principalmente a um servidor COM.
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754485"
---
# <a name="using-stoserve"></a><span data-ttu-id="1c0f8-103">Usando StoServe</span><span class="sxs-lookup"><span data-stu-id="1c0f8-103">Using StoServe</span></span>

<span data-ttu-id="1c0f8-104">**StoServe** é uma DLL que se destina principalmente a um servidor com.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-104">**StoServe** is a DLL that is intended primarily as a COM server.</span></span> <span data-ttu-id="1c0f8-105">Embora ele possa ser carregado implicitamente, vinculando-se ao seu associado. Arquivo LIB, normalmente é usado após uma chamada LoadLibrary explícita, geralmente de dentro da função COM [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span><span class="sxs-lookup"><span data-stu-id="1c0f8-105">Although it can be implicitly loaded by linking to its associated .LIB file, it is normally used after an explicit LoadLibrary call, usually from within the COM function [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject).</span></span> <span data-ttu-id="1c0f8-106">**StoServe** é um servidor em processo de registro automático.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-106">**StoServe** is a self-registering in-process server.</span></span>

<span data-ttu-id="1c0f8-107">Para usar o **StoServe**, um programa cliente não precisa incluir o StoServe. H ou link para STOSERVE. LIB.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-107">To use **StoServe**, a client program does not need to include STOSERVE.H or link to STOSERVE.LIB.</span></span> <span data-ttu-id="1c0f8-108">Um cliente COM do **StoServe** obtém acesso exclusivamente por meio do CLSID e dos serviços com do seu objeto.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-108">A COM client of **StoServe** obtains access solely through its object's CLSID and COM services.</span></span> <span data-ttu-id="1c0f8-109">Para **StoServe**, esse CLSID é CLSID \_ DllPaper (definido no arquivo PAPGUIDS. H no \\ diretório irmão Inc.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-109">For **StoServe**, that CLSID is CLSID\_DllPaper (defined in file PAPGUIDS.H in the \\INC sibling directory).</span></span> <span data-ttu-id="1c0f8-110">O exemplo de código [StoClien](structured-storage-client-sample--stoclien-.md) mostra como o cliente obtém esse acesso.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-110">The [StoClien](structured-storage-client-sample--stoclien-.md) code sample shows how the client obtains this access.</span></span>

<span data-ttu-id="1c0f8-111">O makefile que cria esse exemplo registra automaticamente o servidor no registro.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-111">The makefile that builds this sample automatically registers the server in the registry.</span></span> <span data-ttu-id="1c0f8-112">Você pode iniciar manualmente seu auto-registro emitindo o seguinte comando no prompt de comando no diretório **StoServe** :</span><span class="sxs-lookup"><span data-stu-id="1c0f8-112">You can manually initiate its self-registration by issuing the following command at the command prompt in the **StoServe** directory:</span></span>

<span data-ttu-id="1c0f8-113"> **registro** de NMAKE</span><span class="sxs-lookup"><span data-stu-id="1c0f8-113">**nmake** **register**</span></span>

<span data-ttu-id="1c0f8-114">Isso pressupõe que você tenha um ambiente de compilação configurado.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-114">This assumes that you have a compilation environment set up.</span></span> <span data-ttu-id="1c0f8-115">Caso contrário, você também pode invocar diretamente o comando REGISTER.EXE no prompt de comando enquanto estiver no diretório **StoServe**</span><span class="sxs-lookup"><span data-stu-id="1c0f8-115">If not, you can also directly invoke the REGISTER.EXE command at the command prompt while in the **StoServe** directory.</span></span>

<span data-ttu-id="1c0f8-116">**..\\ registrar \\register.exe** **stoserve.dll**</span><span class="sxs-lookup"><span data-stu-id="1c0f8-116">**..\\register\\register.exe** **stoserve.dll**</span></span>

<span data-ttu-id="1c0f8-117">Esses comandos de registro exigem uma compilação anterior do exemplo de registro nesta série, bem como uma compilação anterior do STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-117">These registration commands require a prior build of the REGISTER sample in this series, as well as a prior build of STOSERVE.DLL.</span></span>

<span data-ttu-id="1c0f8-118">Nesta série, os makefiles usam o utilitário REGISTER.EXE do exemplo de registro.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-118">In this series, the makefiles use the REGISTER.EXE utility from the REGISTER sample.</span></span> <span data-ttu-id="1c0f8-119">As versões recentes do SDK (Kit de desenvolvimento de software) de plataforma e Visual C++ incluem um utilitário, REGSVR32.EXE, que pode ser usado de forma semelhante para registrar servidores em processo e realizar marshaling de DLLs.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-119">Recent releases of the Platform Software Development Kit (SDK) and Visual C++ include a utility, REGSVR32.EXE, which can be used in a similar fashion to register in-process servers and marshaling DLLs.</span></span>

<span data-ttu-id="1c0f8-120">O **StoServe** usa muitos dos serviços e classes de utilitário fornecidos pelo APPUTIL.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-120">**StoServe** uses many of the utility classes and services provided by APPUTIL.</span></span> <span data-ttu-id="1c0f8-121">Para obter mais detalhes sobre o APPUTIL, estude o código-fonte da biblioteca APPUTIL no diretório APPUTIL irmão e APPUTIL.HTM no diretório principal do tutorial.</span><span class="sxs-lookup"><span data-stu-id="1c0f8-121">For more details on APPUTIL, study the APPUTIL library's source code in the sibling APPUTIL directory and APPUTIL.HTM in the main tutorial directory.</span></span>

 

 