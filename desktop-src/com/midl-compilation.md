---
title: Compilação de MIDL
description: Compilação de MIDL
ms.assetid: 2797ee3b-82fd-4cb5-9e95-23b2f2a8f011
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281fa66ec1b8f997dd58fc55a67c19a801d2d36
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454371"
---
# <a name="midl-compilation"></a><span data-ttu-id="7fdd6-103">Compilação de MIDL</span><span class="sxs-lookup"><span data-stu-id="7fdd6-103">MIDL Compilation</span></span>

<span data-ttu-id="7fdd6-104">Dado um arquivo IDL, como [example2. idl](anatomy-of-an-idl-file.md), que define uma ou mais interfaces com e uma biblioteca de tipos, o compilador MIDL (Midl.exe) gera os arquivos descritos na tabela a seguir como a saída padrão.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-104">Given an IDL file, such as [Example2.idl](anatomy-of-an-idl-file.md), that defines one or more COM interfaces and a type library, the MIDL compiler (Midl.exe) generates the files described in the following table as the default output.</span></span>



| <span data-ttu-id="7fdd6-105">Nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="7fdd6-105">Filename</span></span>                 | <span data-ttu-id="7fdd6-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fdd6-106">Description</span></span>                                                                                                                                                                                           |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdd6-107">Example2. h</span><span class="sxs-lookup"><span data-stu-id="7fdd6-107">Example2.h</span></span><br/>    | <span data-ttu-id="7fdd6-108">O arquivo de cabeçalho, que contém definições de tipo e declarações de função para todas as interfaces definidas no arquivo IDL, bem como declarações de encaminhamento para rotinas que os stubs chamam.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-108">The header file, containing type definitions and function declarations for all of the interfaces defined in the IDL file as well as forward declarations for routines that the stubs call.</span></span><br/> |
| <span data-ttu-id="7fdd6-109">Example2 \_ p. c</span><span class="sxs-lookup"><span data-stu-id="7fdd6-109">Example2\_p.c</span></span><br/> | <span data-ttu-id="7fdd6-110">O arquivo de proxy/stub, que inclui os pontos de entrada substitutos para clientes e para servidores.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-110">The proxy/stub file, which includes the surrogate entry points both for clients and for servers.</span></span><br/>                                                                                           |
| <span data-ttu-id="7fdd6-111">Example2 \_ i. c</span><span class="sxs-lookup"><span data-stu-id="7fdd6-111">Example2\_i.c</span></span><br/> | <span data-ttu-id="7fdd6-112">O arquivo de ID de interface, que define o GUID para cada interface especificada no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-112">The interface ID file, which defines the GUID for every interface specified in the IDL file.</span></span><br/>                                                                                               |
| <span data-ttu-id="7fdd6-113">Example2. tlb</span><span class="sxs-lookup"><span data-stu-id="7fdd6-113">Example2.tlb</span></span><br/>  | <span data-ttu-id="7fdd6-114">Um arquivo de documento composto que contém informações sobre tipos e objetos.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-114">A compound document file that contains information about types and objects.</span></span><br/>                                                                                                                |
| <span data-ttu-id="7fdd6-115">Dlldata. c</span><span class="sxs-lookup"><span data-stu-id="7fdd6-115">Dlldata.c</span></span><br/>     | <span data-ttu-id="7fdd6-116">Contém os dados necessários para criar uma DLL de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-116">Contains the data you need to create a proxy/stub DLL.</span></span><br/>                                                                                                                                     |



 

<span data-ttu-id="7fdd6-117">Você usa o arquivo de cabeçalho e todos os arquivos. c para [criar uma DLL de proxy](building-and-registering-a-proxy-dll.md) que pode dar suporte à interface quando usada por aplicativos cliente e por servidores de objetos.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-117">You use the header file and all of the .c files to [create a proxy DLL](building-and-registering-a-proxy-dll.md) that can support the interface when used both by client applications and by object servers.</span></span> <span data-ttu-id="7fdd6-118">Você usa o arquivo de cabeçalho de interface (example2. h) e o arquivo de ID de interface (example2 \_ i. c) ao criar o arquivo executável para um aplicativo cliente que usa a interface.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-118">You use the interface header file (Example2.h) and the interface ID (Example2\_i.c) file when creating the executable file for a client application that uses the interface.</span></span> <span data-ttu-id="7fdd6-119">Você pode optar por incluir o arquivo de biblioteca de tipos como um recurso em seu EXE ou DLL, ou pode enviá-lo como um arquivo separado.</span><span class="sxs-lookup"><span data-stu-id="7fdd6-119">You can choose to include the type library file as a resource in your EXE or DLL, or you can ship it as a separate file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fdd6-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fdd6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fdd6-121">Arquivos gerados para uma interface COM</span><span class="sxs-lookup"><span data-stu-id="7fdd6-121">Files Generated for a COM Interface</span></span>](/windows/desktop/Midl/files-generated-for-a-com-interface)
</dt> <dt>

[<span data-ttu-id="7fdd6-122">Opções do compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="7fdd6-122">MIDL Compiler Options</span></span>](midl-compiler-options.md)
</dt> </dl>

 

