---
description: Normalmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável.
ms.assetid: 610e5cd3-9dc3-462c-98f8-6a63874464f8
title: Arquivos de Símbolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964fbe0ab5f07a6c3d7cfa08b057550e1cc2c74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088956"
---
# <a name="symbol-files"></a><span data-ttu-id="19cc8-103">Arquivos de Símbolo</span><span class="sxs-lookup"><span data-stu-id="19cc8-103">Symbol Files</span></span>

<span data-ttu-id="19cc8-104">Normalmente, as informações de depuração são armazenadas em um arquivo de símbolo separado do executável.</span><span class="sxs-lookup"><span data-stu-id="19cc8-104">Normally, debugging information is stored in a symbol file separate from the executable.</span></span> <span data-ttu-id="19cc8-105">A implementação dessas informações de depuração mudou ao longo dos anos, e a documentação a seguir fornecerá orientações sobre essas várias implementações.</span><span class="sxs-lookup"><span data-stu-id="19cc8-105">The implementation of this debugging information has changed over the years, and the following documentation will provide guidance regarding these various implementations.</span></span>

## <a name="pdb-files"></a><span data-ttu-id="19cc8-106">arquivos PDB</span><span class="sxs-lookup"><span data-stu-id="19cc8-106">PDB files</span></span>

<span data-ttu-id="19cc8-107">Todas as versões modernas dos compiladores da Microsoft armazenam informações de depuração sobre um executável compilado em um arquivo de *banco de dados de programa* separado (. pdb).</span><span class="sxs-lookup"><span data-stu-id="19cc8-107">All modern versions of the Microsoft compilers store debugging information about a compiled executable in a separate *program database* (.pdb) file.</span></span> <span data-ttu-id="19cc8-108">Esse arquivo é comumente chamado de *PDB*.</span><span class="sxs-lookup"><span data-stu-id="19cc8-108">This file is commonly referred to as a *PDB*.</span></span> <span data-ttu-id="19cc8-109">Os dados são armazenados em um arquivo separado do executável para ajudar a limitar o tamanho do executável, economizando espaço de armazenamento em disco e reduzindo o tempo necessário para carregar os dados.</span><span class="sxs-lookup"><span data-stu-id="19cc8-109">The data is stored in a separate file from the executable to help limit the size of the executable, saving disk storage space and reducing the time it takes to load the data.</span></span> <span data-ttu-id="19cc8-110">Essa metodologia também permite que o executável seja distribuído sem revelar essas informações significativas, o que pode facilitar a engenharia reversa do programa.</span><span class="sxs-lookup"><span data-stu-id="19cc8-110">This methodology also allows the executable to be distributed without disclosing this significant information which could make the program easier to reverse engineer.</span></span>

<span data-ttu-id="19cc8-111">Para criar um PDB, compile o arquivo executável com informações de depuração de acordo com as instruções para suas ferramentas de Build.</span><span class="sxs-lookup"><span data-stu-id="19cc8-111">To create a PDB, build your executable file with debugging information according to the directions for your build tools.</span></span>

<span data-ttu-id="19cc8-112">A API DbgHelp é capaz de usar PDBs para obter as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="19cc8-112">The DbgHelp API is able to use PDBs to obtain the following information.</span></span>

-   <span data-ttu-id="19cc8-113">públicos e exportações</span><span class="sxs-lookup"><span data-stu-id="19cc8-113">publics and exports</span></span>
-   <span data-ttu-id="19cc8-114">símbolos globais</span><span class="sxs-lookup"><span data-stu-id="19cc8-114">global symbols</span></span>
-   <span data-ttu-id="19cc8-115">símbolos locais</span><span class="sxs-lookup"><span data-stu-id="19cc8-115">local symbols</span></span>
-   <span data-ttu-id="19cc8-116">dados de tipo</span><span class="sxs-lookup"><span data-stu-id="19cc8-116">type data</span></span>
-   <span data-ttu-id="19cc8-117">arquivos de origem</span><span class="sxs-lookup"><span data-stu-id="19cc8-117">source files</span></span>
-   <span data-ttu-id="19cc8-118">números de linha</span><span class="sxs-lookup"><span data-stu-id="19cc8-118">line numbers</span></span>

## <a name="dbg-files-and-embedded-debug-information"></a><span data-ttu-id="19cc8-119">Arquivos DBG e informações de depuração inseridas</span><span class="sxs-lookup"><span data-stu-id="19cc8-119">DBG files and embedded debug information</span></span>

<span data-ttu-id="19cc8-120">Versões anteriores do conjunto de ferramentas da Microsoft usavam para inserir as informações de depuração no executável, no entanto, normalmente seriam removidas para um arquivo separado com uma extensão. dbg.</span><span class="sxs-lookup"><span data-stu-id="19cc8-120">Previous versions of the Microsoft toolset used to embed the debugging information in the executable, however it would normally be stripped out into a separate file with a .dbg extension.</span></span> <span data-ttu-id="19cc8-121">Isso normalmente é conhecido como um arquivo *DBG* .</span><span class="sxs-lookup"><span data-stu-id="19cc8-121">This is commonly known as a *DBG* file.</span></span> <span data-ttu-id="19cc8-122">Os arquivos DBG usam o mesmo formato de arquivo PE como executáveis.</span><span class="sxs-lookup"><span data-stu-id="19cc8-122">DBG files use the same PE file format as executables.</span></span>

<span data-ttu-id="19cc8-123">O suporte de API do DbgHelp para DBGs e informações de depuração incorporadas é limitado e inclui o seguinte.</span><span class="sxs-lookup"><span data-stu-id="19cc8-123">The DbgHelp API support for DBGs and embedded debugging information is limited and includes the following.</span></span>

-   <span data-ttu-id="19cc8-124">públicos e exportações</span><span class="sxs-lookup"><span data-stu-id="19cc8-124">publics and exports</span></span>
-   <span data-ttu-id="19cc8-125">símbolos globais</span><span class="sxs-lookup"><span data-stu-id="19cc8-125">global symbols</span></span>

 

 



