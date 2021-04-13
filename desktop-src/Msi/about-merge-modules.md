---
description: Módulos de mesclagem são essencialmente arquivos. msi simplificados, que é a extensão de nome de arquivo para um pacote de instalação Windows Installer. Um módulo de mesclagem padrão tem uma extensão de nome de arquivo. msm.
ms.assetid: 580fe58a-4636-4f9a-a68d-4fd0e281e949
title: Sobre módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70d416b89f0979d5651480a05052e95b4d32e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296683"
---
# <a name="about-merge-modules"></a><span data-ttu-id="f0f7a-104">Sobre módulos de mesclagem</span><span class="sxs-lookup"><span data-stu-id="f0f7a-104">About Merge Modules</span></span>

<span data-ttu-id="f0f7a-105">Módulos de mesclagem são essencialmente arquivos. msi simplificados, que é a extensão de nome de arquivo para um pacote de instalação Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-105">Merge modules are essentially simplified .msi files, which is the file name extension for a Windows Installer installation package.</span></span> <span data-ttu-id="f0f7a-106">Um módulo de mesclagem padrão tem uma extensão de nome de arquivo. msm.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-106">A standard merge module has an .msm file name extension.</span></span>

<span data-ttu-id="f0f7a-107">Um módulo de mesclagem não pode ser instalado sozinho porque não tem algumas tabelas de banco de dados vitais que estão presentes em um banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-107">A merge module cannot be installed alone because its lacks some vital database tables that are present in an installation database.</span></span> <span data-ttu-id="f0f7a-108">Os módulos de mesclagem também contêm tabelas adicionais que são exclusivas a si mesmas.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-108">Merge modules also contain additional tables that are unique to themselves.</span></span> <span data-ttu-id="f0f7a-109">Para instalar as informações entregues por um módulo de mesclagem com um aplicativo, o módulo deve primeiro ser mesclado no arquivo. msi do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-109">To install the information delivered by a merge module with an application, the module must first be merged into the application's .msi file.</span></span>

<span data-ttu-id="f0f7a-110">Um módulo de mesclagem consiste nas seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="f0f7a-110">A merge module consists of the following parts:</span></span>

-   <span data-ttu-id="f0f7a-111">Um [banco de dados de módulo de mesclagem](merge-module-database.md) que contém as propriedades de instalação e a lógica de instalação sendo fornecida pelo módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-111">A [Merge Module Database](merge-module-database.md) containing the installation properties and setup logic being delivered by the merge module.</span></span>
-   <span data-ttu-id="f0f7a-112">Uma [referência de fluxo de informações resumidas do módulo de mesclagem](merge-module-summary-information-stream-reference.md) que descreve o módulo.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-112">A [Merge Module Summary Information Stream Reference](merge-module-summary-information-stream-reference.md) describing the module.</span></span>
-   <span data-ttu-id="f0f7a-113">Um arquivo de gabinete [MergeModule.CABinet](mergemodule-cabinet.md) armazenado como um fluxo dentro do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-113">A [MergeModule.CABinet](mergemodule-cabinet.md) cabinet file stored as a stream inside the merge module.</span></span> <span data-ttu-id="f0f7a-114">Esse gabinete contém todos os arquivos exigidos pelos componentes fornecidos pelo módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-114">This cabinet contains all the files required by the components delivered by the merge module.</span></span>

<span data-ttu-id="f0f7a-115">[Vários módulos de mesclagem de idiomas](multiple-language-merge-modules.md) podem fornecer componentes para um pacote de instalação em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-115">[Multiple language merge modules](multiple-language-merge-modules.md) can deliver components to an installation package in multiple languages.</span></span> <span data-ttu-id="f0f7a-116">Em um módulo de mesclagem de vários idiomas, o banco de dados contém as propriedades de instalação e a lógica para mais de um idioma e o MergeModule.CABgabinete inet inclui todos os arquivos necessários para instalar os componentes com todos os idiomas com suporte no módulo.</span><span class="sxs-lookup"><span data-stu-id="f0f7a-116">In a multiple language merge module the database contains the installation properties and logic for more than one language and the MergeModule.CABinet cabinet includes all the files necessary to install components with all the languages supported by the module.</span></span>

 

 



