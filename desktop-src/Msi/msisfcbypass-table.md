---
description: A tabela MsiSFCBypass contém uma lista de arquivos que devem ignorar a proteção de arquivos do Windows quando os arquivos são instalados no Microsoft Windows me.
ms.assetid: 86de0dc1-ed8f-410c-a411-6c44c8e5c9fd
title: Tabela MsiSFCBypass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 707294e9461aaf321add8a3959682a0db555cc2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297116"
---
# <a name="msisfcbypass-table"></a><span data-ttu-id="46eda-103">Tabela MsiSFCBypass</span><span class="sxs-lookup"><span data-stu-id="46eda-103">MsiSFCBypass Table</span></span>

<span data-ttu-id="46eda-104">A tabela MsiSFCBypass contém uma lista de arquivos que devem ignorar a proteção de arquivos do Windows quando os arquivos são instalados no Microsoft Windows me.</span><span class="sxs-lookup"><span data-stu-id="46eda-104">The MsiSFCBypass Table contains a list of files that should bypass Windows File Protection when the files are installed on Microsoft Windows Me.</span></span>

<span data-ttu-id="46eda-105">A tabela MsiSFCBypass tem a seguinte coluna.</span><span class="sxs-lookup"><span data-stu-id="46eda-105">The MsiSFCBypass Table has the following column.</span></span>



| <span data-ttu-id="46eda-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="46eda-106">Column</span></span> | <span data-ttu-id="46eda-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="46eda-107">Type</span></span>                         | <span data-ttu-id="46eda-108">Chave</span><span class="sxs-lookup"><span data-stu-id="46eda-108">Key</span></span> | <span data-ttu-id="46eda-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="46eda-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="46eda-110">Arquivo\_</span><span class="sxs-lookup"><span data-stu-id="46eda-110">File\_</span></span> | [<span data-ttu-id="46eda-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="46eda-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="46eda-112">S</span><span class="sxs-lookup"><span data-stu-id="46eda-112">Y</span></span>   | <span data-ttu-id="46eda-113">N</span><span class="sxs-lookup"><span data-stu-id="46eda-113">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="46eda-114">Colunas</span><span class="sxs-lookup"><span data-stu-id="46eda-114">Columns</span></span>

<dl> <dt>

<span data-ttu-id="46eda-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Grupo\_</span><span class="sxs-lookup"><span data-stu-id="46eda-115"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="46eda-116">A chave estrangeira para a [tabela de arquivos](file-table.md) que especifica o arquivo que deve ignorar a proteção de arquivos do Windows quando o arquivo é instalado no Windows me.</span><span class="sxs-lookup"><span data-stu-id="46eda-116">The foreign key to the [File Table](file-table.md) that specifies the file that should bypass Windows File Protection when the file is installed on Windows Me.</span></span>

</dd> </dl>

 

 



