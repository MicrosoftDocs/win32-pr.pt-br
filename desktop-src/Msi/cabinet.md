---
description: O tipo de dados de gabinete deve ser usado na coluna de gabinete da tabela de mídia.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828041"
---
# <a name="cabinet"></a><span data-ttu-id="742f4-103">Gabinete</span><span class="sxs-lookup"><span data-stu-id="742f4-103">Cabinet</span></span>

<span data-ttu-id="742f4-104">O tipo de dados de gabinete deve ser usado na coluna de gabinete da [tabela de mídia](media-table.md).</span><span class="sxs-lookup"><span data-stu-id="742f4-104">The Cabinet data type must be used in the Cabinet column of the [Media table](media-table.md).</span></span>

<span data-ttu-id="742f4-105">Se o nome do gabinete for precedido pelo sinal de número, o gabinete será armazenado como um fluxo de dados dentro do pacote.</span><span class="sxs-lookup"><span data-stu-id="742f4-105">If the cabinet name is preceded by the number sign, the cabinet is stored as a data stream inside the package.</span></span> <span data-ttu-id="742f4-106">A cadeia de caracteres que segue o \# é um [identificador](identifier.md) para este fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="742f4-106">The character string which follows the \# is an [Identifier](identifier.md) for this data stream.</span></span> <span data-ttu-id="742f4-107">Observe que, se o gabinete for armazenado como um fluxo de dados, o nome de um gabinete diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="742f4-107">Note that if the cabinet is stored as a data stream, the name of a cabinet is case-sensitive.</span></span>

<span data-ttu-id="742f4-108">Se o nome do gabinete não for precedido pelo sinal numérico \# , o gabinete será armazenado em um arquivo separado localizado na raiz da árvore de origem especificada pela tabela de [diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="742f4-108">If the cabinet name is not preceded by the number sign \#, the cabinet is stored in a separate file located at the root of the source tree specified by the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="742f4-109">O arquivo de gabinete deve usar a sintaxe de nome de arquivo curto que consiste em um nome de oito caracteres, um ponto e uma extensão de três caracteres.</span><span class="sxs-lookup"><span data-stu-id="742f4-109">The cabinet file must use the short file name syntax consisting of an eight character name, a period, and a three character extension.</span></span> <span data-ttu-id="742f4-110">O tipo de dados Cabinet não pode usar a \| sintaxe curta longa para nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="742f4-110">The Cabinet data type cannot use the short\|longname syntax for file names.</span></span> <span data-ttu-id="742f4-111">Se o arquivo de gabinete for armazenado como um arquivo separado, o nome do arquivo de gabinete não diferenciará maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="742f4-111">If the cabinet file is stored as a separate file, the name of the cabinet file is not case-sensitive.</span></span>

<span data-ttu-id="742f4-112">Para conservar o espaço em disco, o instalador remove todos os gabinetes inseridos no arquivo. msi antes de armazenar em cache o pacote de instalação no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="742f4-112">To conserve disk space, the installer removes any cabinets embedded in the .msi file before caching the installation package on the user's computer.</span></span>

<span data-ttu-id="742f4-113">Consulte [incluindo um arquivo de gabinete em uma instalação](including-a-cabinet-file-in-an-installation.md).</span><span class="sxs-lookup"><span data-stu-id="742f4-113">See [Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).</span></span>

 

 



