---
description: Msimerg.exe é um utilitário de linha de comando que usa MsiDatabaseMerge para mesclar um banco de dados de referência em um banco de dados base.
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922540"
---
# <a name="msimergexe"></a><span data-ttu-id="1a3e5-103">Msimerg.exe</span><span class="sxs-lookup"><span data-stu-id="1a3e5-103">Msimerg.exe</span></span>

<span data-ttu-id="1a3e5-104">Msimerg.exe é um utilitário de linha de comando que usa [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) para [mesclar](merges-and-transforms.md) um banco de dados de referência em um banco de dados base.</span><span class="sxs-lookup"><span data-stu-id="1a3e5-104">Msimerg.exe is a command line utility that uses [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to [merge](merges-and-transforms.md) a reference database into a base database.</span></span>

<span data-ttu-id="1a3e5-105">Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="1a3e5-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3e5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a3e5-106">Syntax</span></span>

<span data-ttu-id="1a3e5-107">**Msimerg** *{banco de dados base} {Reference Database}*</span><span class="sxs-lookup"><span data-stu-id="1a3e5-107">**Msimerg** *{base database}{reference database}*</span></span>

<span data-ttu-id="1a3e5-108">Se houver um conflito de mesclagem entre os dois bancos de dados, as informações de conflito serão colocadas na \_ tabela MergeErrors.</span><span class="sxs-lookup"><span data-stu-id="1a3e5-108">If there is a merge conflict between the two databases, the conflict information is placed in the \_MergeErrors table.</span></span>

## <a name="command-line-options"></a><span data-ttu-id="1a3e5-109">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="1a3e5-109">Command Line Options</span></span>

<span data-ttu-id="1a3e5-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1a3e5-110">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a3e5-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a3e5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a3e5-112">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="1a3e5-112">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="1a3e5-113">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="1a3e5-113">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



