---
title: Arquivos IDL
description: Arquivos IDL
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824011"
---
# <a name="idl-files"></a><span data-ttu-id="fd9d1-103">Arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="fd9d1-103">IDL Files</span></span>

<span data-ttu-id="fd9d1-104">COM usa o linguagem IDL da Microsoft (MIDL) para descrever objetos COM.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="fd9d1-105">MIDL é uma extensão da IDL para ambientes de computação distribuídos definidos pela Open Software Foundation, que foi desenvolvida para definir interfaces para chamadas de procedimento remotas em aplicativos cliente/servidor tradicionais.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="fd9d1-106">MIDL inclui a maioria dos atributos e instruções do ODL (linguagem de definição de objeto), a linguagem usada originalmente para gerar bibliotecas de tipos para automação OLE.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="fd9d1-107">Em C++ e Java, um desenvolvedor criando um objeto COM cria um arquivo IDL que o compilador MIDL processa para criar uma biblioteca de tipos ou um cabeçalho e arquivos de proxy, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="fd9d1-108">Uma *biblioteca de tipos* é um arquivo binário que descreve o objeto com ou interfaces com, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="fd9d1-109">Uma biblioteca de tipos é a versão compilada do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="fd9d1-110">No entanto, as bibliotecas de tipos dão suporte apenas à semântica ODL.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="fd9d1-111">Em particular, eles não podem representar todas as informações de um arquivo IDL relacionado a atributos IDL, como o \[ [**tamanho \_ é**](/windows/desktop/Midl/size-is) \] .</span><span class="sxs-lookup"><span data-stu-id="fd9d1-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="fd9d1-112">Você precisa criar e usar arquivos de proxy para arquivos IDL afetados pela perda de informações na biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="fd9d1-113">No Visual Basic, um desenvolvedor que cria um objeto COM não cria um arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="fd9d1-114">Em vez disso, Visual Basic coleta informações usando propriedades de classe e projeto e cria diretamente a biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="fd9d1-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 