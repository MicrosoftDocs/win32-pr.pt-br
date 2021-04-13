---
description: O programa de FhManagew.exe exclui versões de arquivo que excedem uma idade especificada do dispositivo de destino do histórico de arquivos atribuído no momento.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457005"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="b116d-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="b116d-103">FhManagew.exe</span></span>

<span data-ttu-id="b116d-104">O programa de FhManagew.exe exclui versões de arquivo que excedem uma idade especificada do dispositivo de destino do histórico de arquivos atribuído no momento.</span><span class="sxs-lookup"><span data-stu-id="b116d-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="b116d-105">Este programa está disponível no Windows 8 e no Windows Server 2012 e posterior.</span><span class="sxs-lookup"><span data-stu-id="b116d-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="b116d-106">Para executar este programa, vá para o menu **Iniciar** , clique em **executar** e digite o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="b116d-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="b116d-107">**FhManagew.exe-idade de limpeza** </span><span class="sxs-lookup"><span data-stu-id="b116d-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b116d-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="b116d-108">Parameter</span></span></th>
<th><span data-ttu-id="b116d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="b116d-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b116d-110"><span id="age"></span><span id="AGE"></span><em>idade</em></span><span class="sxs-lookup"><span data-stu-id="b116d-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="b116d-111">Esse parâmetro especifica a idade mínima, em dias, das versões de arquivo que podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="b116d-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="b116d-112">Uma versão de arquivo será excluída se as duas condições a seguir forem verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="b116d-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="b116d-113">A versão do arquivo é mais antiga que a idade especificada.</span><span class="sxs-lookup"><span data-stu-id="b116d-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="b116d-114">O arquivo não está mais incluído no escopo de proteção ou há uma versão mais recente do mesmo arquivo no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="b116d-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="b116d-115">Se o parâmetro <em>age</em> for definido como zero, todas as versões de arquivo serão excluídas, exceto para a versão mais recente de cada arquivo presente atualmente no escopo de proteção.</span><span class="sxs-lookup"><span data-stu-id="b116d-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b116d-116">Para suprimir toda a saída deste programa, use a opção de linha de comando **-Quiet** da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b116d-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="b116d-117"> *Idade* da limpeza **deFhManagew.exe-Quiet**</span><span class="sxs-lookup"><span data-stu-id="b116d-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="b116d-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b116d-118">Examples</span></span>



| <span data-ttu-id="b116d-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b116d-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="b116d-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b116d-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b116d-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-limpeza 30**</span><span class="sxs-lookup"><span data-stu-id="b116d-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="b116d-122">Exclua todas as versões de arquivo com mais de um mês.</span><span class="sxs-lookup"><span data-stu-id="b116d-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="b116d-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-limpeza 365-Quiet**</span><span class="sxs-lookup"><span data-stu-id="b116d-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="b116d-124">Exclua todas as versões de arquivo com mais de um ano e omita todas as saídas.</span><span class="sxs-lookup"><span data-stu-id="b116d-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




