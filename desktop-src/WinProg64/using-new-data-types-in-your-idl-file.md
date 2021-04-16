---
title: Usando novos tipos de dados em seu arquivo IDL
description: O arquivo de cabeçalho Basetsd. h define os novos tipos de dados necessários para gravar aplicativos que são executados em ambas as janelas de 32 e 64 bits.
ms.assetid: 99a3904b-9120-4d1d-bd8c-1eb299bd6b27
keywords:
- Arquivo de cabeçalho Basetsd. h programação do Windows de 64 bits
- tipos de dados no arquivo IDL programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff1add2d70c99069911ac76ad168b7d31c3365f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105772526"
---
# <a name="using-new-data-types-in-your-idl-file"></a><span data-ttu-id="1db9d-105">Usando novos tipos de dados em seu arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="1db9d-105">Using New Data Types in Your IDL File</span></span>

<span data-ttu-id="1db9d-106">O arquivo de cabeçalho Basetsd. h define os novos tipos de dados necessários para gravar aplicativos que são executados em ambas as janelas de 32 e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="1db9d-106">The Basetsd.h header file defines the new data types needed for writing applications that run on both 32- and 64-bit Windows.</span></span> <span data-ttu-id="1db9d-107">Para usar esses tipos de dados em suas interfaces, importe Basetsd. h para o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="1db9d-107">To use these data types in your interfaces, import Basetsd.h into your IDL file.</span></span> <span data-ttu-id="1db9d-108">Não \# inclua o arquivo ou você terminará com várias definições no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="1db9d-108">Do not \#include the file or you will end up with multiple definitions at compile time.</span></span>

<span data-ttu-id="1db9d-109">Como alternativa, você pode incluir ou importar o arquivo Basetsd. idl em seu arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="1db9d-109">Alternatively, you can include or import the Basetsd.idl file into your IDL file.</span></span>

<span data-ttu-id="1db9d-110">Para obter mais informações sobre como adicionar arquivos de cabeçalho do sistema ao arquivo IDL, consulte [Importando arquivos e bibliotecas de tipos](/windows/desktop/Midl/importing-files-and-type-libraries) e [Importando arquivos de cabeçalho do sistema](/windows/desktop/Midl/importing-system-header-files).</span><span class="sxs-lookup"><span data-stu-id="1db9d-110">For more information on adding system header files to your IDL file, see [Importing Files and Type Libraries](/windows/desktop/Midl/importing-files-and-type-libraries) and [Importing System Header Files](/windows/desktop/Midl/importing-system-header-files).</span></span>

 

 