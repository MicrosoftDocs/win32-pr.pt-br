---
description: O Windows 7 apresenta bibliotecas, que fornecem aos usuários uma exibição única e coerente de seus arquivos, mesmo quando esses arquivos são armazenados em locais diferentes.
title: Bibliotecas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968246"
---
# <a name="windows-libraries"></a><span data-ttu-id="cdc70-103">Bibliotecas do Windows</span><span class="sxs-lookup"><span data-stu-id="cdc70-103">Windows Libraries</span></span>

<span data-ttu-id="cdc70-104">O Windows 7 apresenta bibliotecas, que fornecem aos usuários uma exibição única e coerente de seus arquivos, mesmo quando esses arquivos são armazenados em locais diferentes.</span><span class="sxs-lookup"><span data-stu-id="cdc70-104">Windows 7 introduces libraries, which provide users with a single, coherent view of their files even when those files are stored in different locations.</span></span> <span data-ttu-id="cdc70-105">As bibliotecas podem ser configuradas e organizadas por um usuário e uma biblioteca pode conter pastas que são encontradas no computador do usuário e também as pastas que foram compartilhadas em uma rede.</span><span class="sxs-lookup"><span data-stu-id="cdc70-105">Libraries can be configured and organized by a user and a library can contain folders that are found on the user's computer and also folders that have been shared over a network.</span></span> <span data-ttu-id="cdc70-106">As bibliotecas apresentam uma visão mais simples do sistema de armazenamento subjacente porque, para o usuário, os arquivos e as pastas em uma biblioteca são exibidos em uma única exibição, independentemente de onde estejam fisicamente armazenados.</span><span class="sxs-lookup"><span data-stu-id="cdc70-106">Libraries present a simpler view of the underlying storage system because, to the user, the files and folders in a library are displayed in single view, no matter where they are physically stored.</span></span>

<span data-ttu-id="cdc70-107">Os desenvolvedores que escrevem novos programas no Windows 7 são incentivados a usar bibliotecas como o meio pelo qual os usuários interagem com os arquivos usados pelo programa.</span><span class="sxs-lookup"><span data-stu-id="cdc70-107">Developers writing new programs in Windows 7 are encouraged to use libraries as the means through which the users interact with the files used by the program.</span></span> <span data-ttu-id="cdc70-108">O uso de bibliotecas em seu programa fornecerá aos usuários uma experiência mais limpa, mais fácil e consistente no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdc70-108">Using libraries in your program will provide users with a cleaner, easier, and more consistent experience in Windows 7.</span></span>

<span data-ttu-id="cdc70-109">Os desenvolvedores também devem examinar seus programas existentes e atualizá-los se necessário, para trabalhar com bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="cdc70-109">Developers should also review their existing programs, and update them if necessary, to work with libraries.</span></span> <span data-ttu-id="cdc70-110">Como as bibliotecas não fazem parte do sistema de arquivos, as APIs baseadas no sistema de arquivos não terão acesso a bibliotecas que o usuário possa ter configurado.</span><span class="sxs-lookup"><span data-stu-id="cdc70-110">Because libraries are not a part of the file system, file system-based APIs will not have access to any libraries that the user might have configured.</span></span>

<span data-ttu-id="cdc70-111">Os programas que atualmente permitem que os usuários armazenem seu conteúdo em pastas diferentes ou em computadores diferentes irão se beneficiar mais quando adicionam suporte à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cdc70-111">Programs that currently allow users to store their content in different folders or on different computers will benefit most when they add library support.</span></span> <span data-ttu-id="cdc70-112">As bibliotecas simplificam o gerenciamento de conteúdo em diferentes locais de armazenamento para o desenvolvedor e o usuário.</span><span class="sxs-lookup"><span data-stu-id="cdc70-112">Libraries simplify the management of content in diverse storage locations for the developer and the user.</span></span>

<span data-ttu-id="cdc70-113">Este guia descreve mais sobre quais bibliotecas do são, como os programas podem ser feitos para trabalhar com bibliotecas e algumas das maneiras como um programa pode usar bibliotecas para melhorar a experiência do usuário.</span><span class="sxs-lookup"><span data-stu-id="cdc70-113">This guide describes more about what libraries are, how programs can be made to work with libraries, and some of the ways a program can use libraries to improve the user's experience.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdc70-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cdc70-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdc70-115">Sobre bibliotecas</span><span class="sxs-lookup"><span data-stu-id="cdc70-115">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="cdc70-116">Usando bibliotecas em seu programa</span><span class="sxs-lookup"><span data-stu-id="cdc70-116">Using Libraries in your Program</span></span>](library-be-library-aware.md)
</dt> <dt>

[<span data-ttu-id="cdc70-117">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="cdc70-117">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="cdc70-118">Links do Shell</span><span class="sxs-lookup"><span data-stu-id="cdc70-118">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="cdc70-119">Pastas conhecidas</span><span class="sxs-lookup"><span data-stu-id="cdc70-119">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="cdc70-120">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="cdc70-120">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
