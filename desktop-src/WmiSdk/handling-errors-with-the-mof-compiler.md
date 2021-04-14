---
description: Se o compilador MOF não puder concluir a compilação de um arquivo MOF, o repositório do WMI poderá ser deixado em um estado indefinido.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Tratamento de erros com o compilador MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461334"
---
# <a name="handling-errors-with-the-mof-compiler"></a><span data-ttu-id="62749-103">Tratamento de erros com o compilador MOF</span><span class="sxs-lookup"><span data-stu-id="62749-103">Handling Errors with the MOF Compiler</span></span>

<span data-ttu-id="62749-104">Se o compilador MOF não puder concluir a compilação de um arquivo MOF, o repositório do WMI poderá ser deixado em um estado indefinido.</span><span class="sxs-lookup"><span data-stu-id="62749-104">If the MOF compiler cannot finish compiling a MOF file, the WMI repository may be left in an undefined state.</span></span> <span data-ttu-id="62749-105">Por exemplo, se você estiver Compilando um arquivo MOF e usar a opção de linha de comando **-Class: createonly** , a compilação será encerrada se uma classe especificada no arquivo MOF já existir.</span><span class="sxs-lookup"><span data-stu-id="62749-105">For example, if you are compiling a MOF file and you use the **-class:createonly** command-line switch, the compilation terminates if a class specified in the MOF file already exists.</span></span> <span data-ttu-id="62749-106">O compilador MOF armazena no repositório quaisquer classes ou instâncias que foram definidas até o ponto em que o compilador pára.</span><span class="sxs-lookup"><span data-stu-id="62749-106">The MOF compiler stores in the repository any classes or instances that were defined up to the point where the compiler stops.</span></span> <span data-ttu-id="62749-107">Em alguns casos, isso pode deixar o repositório WMI em uma condição indefinida.</span><span class="sxs-lookup"><span data-stu-id="62749-107">In some cases, this can leave the WMI repository in an undefined condition.</span></span>

<span data-ttu-id="62749-108">Nessa situação, talvez seja necessário parar o WMI, excluir o repositório WMI e fazer com que o WMI o recrie.</span><span class="sxs-lookup"><span data-stu-id="62749-108">In this situation, you may need to stop WMI, delete the WMI repository, and have WMI rebuild it.</span></span> <span data-ttu-id="62749-109">Todos os arquivos MOF que contêm o comando [**pragma AutoRecuperação**](pragma-autorecover.md) do [pré-processador](preprocessor-commands.md) são recriados quando o WMI é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="62749-109">All MOF files that contain the [**pragma autorecover**](pragma-autorecover.md) [preprocessor command](preprocessor-commands.md) are rebuilt when WMI is restarted.</span></span> <span data-ttu-id="62749-110">Você deve recompilar manualmente todos os arquivos MOF que não incluem uma `#pragma autorecover` instrução.</span><span class="sxs-lookup"><span data-stu-id="62749-110">You must manually recompile any MOF files that do not include a `#pragma autorecover` statement.</span></span>

<span data-ttu-id="62749-111">Para obter mais informações sobre como declarar classes e instâncias usando a sintaxe do MOF, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="62749-111">For more information about how to declare classes and instances using the MOF syntax, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62749-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62749-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62749-113">Compilando arquivos MOF</span><span class="sxs-lookup"><span data-stu-id="62749-113">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="62749-114">**Mofcomp**</span><span class="sxs-lookup"><span data-stu-id="62749-114">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="62749-115">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="62749-115">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



