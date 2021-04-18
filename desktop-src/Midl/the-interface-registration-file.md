---
title: O arquivo de registro da interface
description: O arquivo de registro de interface coleta informações que ajudam no registro de interfaces COM empacotadas em um arquivo DLL ou EXE.
ms.assetid: 203303dc-121e-4bf4-b648-a35b956a56ee
keywords:
- arquivo de registro da interface MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd6f54f5e027a0ea25dc463772ec24ee5f7386
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758971"
---
# <a name="the-interface-registration-file"></a><span data-ttu-id="fadb3-104">O arquivo de registro da interface</span><span class="sxs-lookup"><span data-stu-id="fadb3-104">The Interface Registration File</span></span>

<span data-ttu-id="fadb3-105">O arquivo de registro de interface coleta informações que ajudam no registro de interfaces COM empacotadas em um arquivo DLL ou EXE.</span><span class="sxs-lookup"><span data-stu-id="fadb3-105">The interface registration file collects information that helps in the registration of COM interfaces packaged into a DLL or EXE file.</span></span> <span data-ttu-id="fadb3-106">O arquivo de registro da interface é diferente de outros arquivos gerados porque ele pode coletar informações da compilação de vários arquivos IDL diferentes.</span><span class="sxs-lookup"><span data-stu-id="fadb3-106">The interface registration file is different from other generated files because it can gather information from compiling several different IDL files.</span></span> <span data-ttu-id="fadb3-107">Cada compilador MIDL executado para interfaces COM procura um arquivo dlldata. c existente primeiro e, se o arquivo não for encontrado, um novo arquivo dlldata. c será criado.</span><span class="sxs-lookup"><span data-stu-id="fadb3-107">Each MIDL compiler run for COM interfaces looks for an existing dlldata.c file first, and if the file is not found, a new dlldata.c file is created.</span></span> <span data-ttu-id="fadb3-108">Se um arquivo dlldata. c for encontrado, as informações sobre o IDL atual serão adicionadas (se ausentes) ou substituídas.</span><span class="sxs-lookup"><span data-stu-id="fadb3-108">If a dlldata.c file is found, information about the current IDL is added (if absent) or replaced.</span></span>

<span data-ttu-id="fadb3-109">O arquivo de registro da interface é gerado com segurança ou atualizado em um ambiente multiprocessador, pois compilações de MIDL paralelas são impedidas de gravar no arquivo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="fadb3-109">The interface registration file is safely generated or updated in a multiprocessor environment because parallel MIDL compiles are prevented from writing to the file at the same time.</span></span> <span data-ttu-id="fadb3-110">Como qualquer arquivo dlldata. c pode ser marcado como somente leitura pelo ambiente de compilação ou pelo usuário, o compilador MIDL implementa uma abordagem de tempo limite para aguardar um arquivo que ele não pode abrir e emite uma mensagem de erro apropriada se o tempo limite expirar.</span><span class="sxs-lookup"><span data-stu-id="fadb3-110">Because any dlldata.c file can be marked as read-only by either the build environment or the user, the MIDL compiler implements a timeout approach to waiting on a file it cannot open, and issues an appropriate error message if the timeout expires.</span></span>

<span data-ttu-id="fadb3-111">O nome padrão para o arquivo de registro da interface gerado a partir de um arquivo de entrada é dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="fadb3-111">The default name for the interface registration file generated from an input file is dlldata.c.</span></span> <span data-ttu-id="fadb3-112">A opção de compilador [**/dlldata nomedearquivo**](-dlldata.md) MIDL pode ser usada para substituir o nome padrão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fadb3-112">The [**/dlldata**](-dlldata.md) MIDL compiler switch can be used to override the default name of the file.</span></span> <span data-ttu-id="fadb3-113">Substituir o nome padrão do arquivo de registro da interface é especialmente útil quando alguns arquivos IDL empacotados em um binário comum residem em diretórios diferentes.</span><span class="sxs-lookup"><span data-stu-id="fadb3-113">Overriding the default name of the interface registration file is especially useful when some IDL files packaged to a common binary reside in different directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fadb3-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fadb3-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fadb3-115">Criando e registrando uma DLL de proxy</span><span class="sxs-lookup"><span data-stu-id="fadb3-115">Building and Registering a Proxy DLL</span></span>](../com/building-and-registering-a-proxy-dll.md)
</dt> </dl>

 

 