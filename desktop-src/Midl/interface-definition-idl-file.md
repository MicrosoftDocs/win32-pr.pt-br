---
title: Arquivo de definição de interface (IDL)
description: Por convenção, o arquivo que contém as definições de interface e biblioteca de tipos é chamado de arquivo IDL e tem uma extensão de nome de arquivo. idl.
ms.assetid: 4df87df8-3206-4845-b5ab-d77ea443b9e3
keywords:
- MIDL de interfaces, arquivo IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950daa2c1841f6e4b3f015f14e373804fcd34b80
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640632"
---
# <a name="interface-definition-idl-file"></a><span data-ttu-id="6c8a7-104">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="6c8a7-104">Interface Definition (IDL) File</span></span>

<span data-ttu-id="6c8a7-105">Por convenção, o arquivo que contém as definições de interface e biblioteca de tipos é chamado de arquivo IDL e tem uma extensão de nome de arquivo. idl.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-105">By convention, the file that contains interface and type library definitions is called an IDL file, and has an .idl file name extension.</span></span> <span data-ttu-id="6c8a7-106">Na realidade, o compilador MIDL analisará um arquivo de definição de interface, independentemente de sua extensão.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-106">In reality, the MIDL compiler will parse an interface definition file regardless of its extension.</span></span> <span data-ttu-id="6c8a7-107">Uma interface é identificada pela [**interface**](interface.md)de palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-107">An interface is identified by the keyword [**interface**](interface.md).</span></span>

<span data-ttu-id="6c8a7-108">Cada interface consiste em um cabeçalho e um corpo.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-108">Each interface consists of a header and a body.</span></span> <span data-ttu-id="6c8a7-109">O cabeçalho da interface contém atributos que se aplicam à interface inteira.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-109">The interface header contains attributes that apply to the entire interface.</span></span> <span data-ttu-id="6c8a7-110">O corpo da interface contém as definições de interface restantes.</span><span class="sxs-lookup"><span data-stu-id="6c8a7-110">The body of the interface contains the remaining interface definitions.</span></span> <span data-ttu-id="6c8a7-111">Para obter uma visão geral de interfaces e arquivos IDL, consulte [o arquivo IDL (Interface Definition Language)](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span><span class="sxs-lookup"><span data-stu-id="6c8a7-111">For an overview of interfaces and IDL files, see [The Interface Definition Language (IDL) File](/windows/desktop/Rpc/the-interface-definition-language-idl-file).</span></span> <span data-ttu-id="6c8a7-112">Para obter um resumo dos atributos que podem ser usados em um cabeçalho de interface, consulte [atributos IDL](idl-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="6c8a7-112">For a summary of attributes that can be used in an interface header, see [IDL Attributes](idl-attributes.md).</span></span>

 

 