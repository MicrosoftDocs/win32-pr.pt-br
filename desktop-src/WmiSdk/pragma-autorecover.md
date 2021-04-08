---
description: Adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma AutoRecuperação
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922417"
---
# <a name="pragma-autorecover"></a><span data-ttu-id="10985-103">pragma AutoRecuperação</span><span class="sxs-lookup"><span data-stu-id="10985-103">pragma autorecover</span></span>

<span data-ttu-id="10985-104">O comando **pragma autocover** pré-processador adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório.</span><span class="sxs-lookup"><span data-stu-id="10985-104">The **pragma autorecover** preprocessor command adds a MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="10985-105">A lista de arquivos MOF de **recuperação automática** está armazenada nesta chave do registro:</span><span class="sxs-lookup"><span data-stu-id="10985-105">The list of **autorecover** MOF files is stored in this registry key:</span></span>

<span data-ttu-id="10985-106">**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AutoRecuperação MOFs**</span><span class="sxs-lookup"><span data-stu-id="10985-106">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**autorecover mofs**</span></span>

<span data-ttu-id="10985-107">O WMI verifica a integridade do repositório do WMI quando o sistema operacional inicia o WMI.</span><span class="sxs-lookup"><span data-stu-id="10985-107">WMI checks the integrity of the WMI repository when the operating system starts WMI.</span></span> <span data-ttu-id="10985-108">Se o repositório estiver danificado, o WMI recompilará automaticamente o repositório e recompilará todos os arquivos MOF listados nessa chave no registro.</span><span class="sxs-lookup"><span data-stu-id="10985-108">If the repository is damaged, WMI automatically rebuilds the repository and recompiles any MOF files listed in this key in the registry.</span></span>

<span data-ttu-id="10985-109">O seguinte descreve a sintaxe para o comando pragma Recover:</span><span class="sxs-lookup"><span data-stu-id="10985-109">The following describes the syntax for the pragma autorecover command:</span></span>


```mof
#pragma autorecover
```



<span data-ttu-id="10985-110">No entanto, você deve observar as seguintes restrições ao usar este comando:</span><span class="sxs-lookup"><span data-stu-id="10985-110">However, you must observe the following restrictions when using this command:</span></span>

-   <span data-ttu-id="10985-111">O WMI não pode recuperar arquivos MOF localizados em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="10985-111">WMI cannot recover MOF files located on a remote computer.</span></span>

    <span data-ttu-id="10985-112">Portanto, os arquivos MOF listados nesta chave do registro devem residir no computador local.</span><span class="sxs-lookup"><span data-stu-id="10985-112">Therefore, the MOF files listed in this registry key must reside on the local computer.</span></span>

-   <span data-ttu-id="10985-113">Você não pode especificar as opções de linha de comando que o compilador MOF usa quando o WMI recupera um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="10985-113">You cannot specify the command-line switches that the MOF compiler uses when WMI recovers a MOF file.</span></span>

    <span data-ttu-id="10985-114">Portanto, você deve incluir comandos [pragma](-pragma.md) no arquivo MOF que tornam as opções de linha de comando desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="10985-114">Therefore, you should include [pragma](-pragma.md) commands in your MOF file that make command-line switches unnecessary.</span></span> <span data-ttu-id="10985-115">O exemplo a seguir descreve uma opção de linha de comando comum que o WMI não usa ao recuperar um arquivo MOF desta chave do registro: **Mofcomp-N:root \\ Test mymof. mof**</span><span class="sxs-lookup"><span data-stu-id="10985-115">The following example describes a common command-line switch that WMI does not use when recovering a MOF file from this registry key: **mofcomp -N:Root\\Test mymof.mof**</span></span>

    <span data-ttu-id="10985-116">No entanto, você pode especificar o namespace usando um comando [pragma](-pragma.md) no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="10985-116">However, you can specify the namespace using a [pragma](-pragma.md) command in the MOF file.</span></span>

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a><span data-ttu-id="10985-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10985-117">Requirements</span></span>



| <span data-ttu-id="10985-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="10985-118">Requirement</span></span> | <span data-ttu-id="10985-119">Valor</span><span class="sxs-lookup"><span data-stu-id="10985-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="10985-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10985-120">Minimum supported client</span></span><br/> | <span data-ttu-id="10985-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10985-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="10985-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="10985-122">Minimum supported server</span></span><br/> | <span data-ttu-id="10985-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10985-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10985-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="10985-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10985-125">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="10985-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




