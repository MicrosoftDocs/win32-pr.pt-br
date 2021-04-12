---
title: Sobre informações de versão
description: Este tópico discute as funções de informações de versão.
ms.assetid: 63fb6c0f-11b3-4d70-b1ba-56086cb02847
keywords:
- recursos, informações de versão
- informações de versão
- adicionando informações de versão
- conflitos de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25bf5c0914ba28b9a5178f99a94f83f57ac99550
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365909"
---
# <a name="about-version-information"></a><span data-ttu-id="7a56c-107">Sobre informações de versão</span><span class="sxs-lookup"><span data-stu-id="7a56c-107">About Version Information</span></span>

<span data-ttu-id="7a56c-108">Você pode usar as funções de informações de versão para determinar onde um arquivo deve ser instalado e identificar conflitos com os arquivos atualmente instalados.</span><span class="sxs-lookup"><span data-stu-id="7a56c-108">You can use the version information functions to determine where a file should be installed and identify conflicts with currently installed files.</span></span> <span data-ttu-id="7a56c-109">Essas funções permitem evitar os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="7a56c-109">These functions enable you to avoid the following problems:</span></span>

-   <span data-ttu-id="7a56c-110">Instalando versões mais antigas de componentes em versões mais recentes</span><span class="sxs-lookup"><span data-stu-id="7a56c-110">installing older versions of components over newer versions</span></span>
-   <span data-ttu-id="7a56c-111">alterando o idioma em um sistema de idioma misto sem notificação</span><span class="sxs-lookup"><span data-stu-id="7a56c-111">changing the language in a mixed-language system without notification</span></span>
-   <span data-ttu-id="7a56c-112">Instalando várias cópias de uma biblioteca em diretórios diferentes</span><span class="sxs-lookup"><span data-stu-id="7a56c-112">installing multiple copies of a library in different directories</span></span>
-   <span data-ttu-id="7a56c-113">copiando arquivos para diretórios de rede compartilhados por vários usuários</span><span class="sxs-lookup"><span data-stu-id="7a56c-113">copying files to network directories shared by multiple users</span></span>

<span data-ttu-id="7a56c-114">As funções de informações de versão permitem que os aplicativos consultem um recurso de versão para informações de arquivo e apresentem as informações em um formato não criptografado.</span><span class="sxs-lookup"><span data-stu-id="7a56c-114">The version information functions enable applications to query a version resource for file information and present the information in a clear format.</span></span> <span data-ttu-id="7a56c-115">Essas informações incluem a finalidade do arquivo, o autor, o número de versão e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="7a56c-115">This information includes the file's purpose, author, version number, and so on.</span></span>

<span data-ttu-id="7a56c-116">Você pode adicionar informações de versão a todos os arquivos que podem ter recursos do Windows, como DLLs, arquivos executáveis ou arquivos de fonte. Fon.</span><span class="sxs-lookup"><span data-stu-id="7a56c-116">You can add version information to any files that can have Windows resources, such as DLLs, executable files, or .fon font files.</span></span> <span data-ttu-id="7a56c-117">Para adicionar as informações, crie um [recurso VERSIONINFO](/windows/desktop/menurc/versioninfo-resource) e use o compilador de recurso para compilar o recurso.</span><span class="sxs-lookup"><span data-stu-id="7a56c-117">To add the information, create a [VERSIONINFO Resource](/windows/desktop/menurc/versioninfo-resource) and use the resource compiler to compile the resource.</span></span>

 

 