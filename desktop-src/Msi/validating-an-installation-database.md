---
description: Os autores de pacotes de instalação sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar a validação novamente sempre que fizerem alterações no pacote.
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: Validando um banco de dados de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826776"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="12ed3-103">Validando um banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="12ed3-103">Validating an Installation Database</span></span>

<span data-ttu-id="12ed3-104">Os autores de pacotes de instalação sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar a validação novamente sempre que fizerem alterações no pacote.</span><span class="sxs-lookup"><span data-stu-id="12ed3-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="12ed3-105">A validação examina o banco de dados em busca de erros que podem parecer válidos individualmente, mas que causam comportamento incorreto no contexto do banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="12ed3-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="12ed3-106">A tentativa de instalar um pacote que falha na validação pode danificar o sistema do usuário.</span><span class="sxs-lookup"><span data-stu-id="12ed3-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="12ed3-107">Consulte as seções [validação de pacote](package-validation.md) e [avaliadores de consistência internos-ICES](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="12ed3-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="12ed3-108">Você pode validar o pacote de exemplo usando [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md).</span><span class="sxs-lookup"><span data-stu-id="12ed3-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="12ed3-109">Para exibir a ajuda para Msival2.exe alterar os diretórios e inserir na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="12ed3-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="12ed3-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="12ed3-110">Msival2 -?</span></span>

<span data-ttu-id="12ed3-111">O arquivo. Cub Darice. Cub contém as ações personalizadas de ICE necessárias para Msival2.exe executar a validação.</span><span class="sxs-lookup"><span data-stu-id="12ed3-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="12ed3-112">Para validar o MNP2000.msi Enter</span><span class="sxs-lookup"><span data-stu-id="12ed3-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="12ed3-113">msival2 MNP2000.msi Darice. Cub</span><span class="sxs-lookup"><span data-stu-id="12ed3-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="12ed3-114">Para obter uma descrição das mensagens de erro e de aviso retornadas pela validação, consulte a [referência de Ice](ice-reference.md).</span><span class="sxs-lookup"><span data-stu-id="12ed3-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="12ed3-115">Corrija todos os erros no pacote e execute a validação novamente conforme necessário até que o pacote passe na validação sem erros.</span><span class="sxs-lookup"><span data-stu-id="12ed3-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="12ed3-116">Depois que o pacote passar na validação, você poderá instalar o pacote de exemplo clicando no ícone de MNP2000.msi ou na linha de comando usando as [Opções de linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="12ed3-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="12ed3-117">Isso conclui a instalação de exemplo.</span><span class="sxs-lookup"><span data-stu-id="12ed3-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="12ed3-118">Próximo exemplo</span><span class="sxs-lookup"><span data-stu-id="12ed3-118">Next example</span></span>

[<span data-ttu-id="12ed3-119">Um exemplo de atualização</span><span class="sxs-lookup"><span data-stu-id="12ed3-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



