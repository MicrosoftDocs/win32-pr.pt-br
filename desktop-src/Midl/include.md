---
title: atributo include
description: A instrução ACF include especifica um ou mais arquivos de cabeçalho a serem incluídos no código stub gerado.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- incluir o atributo MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104084159"
---
# <a name="include-attribute"></a><span data-ttu-id="360e4-104">atributo include</span><span class="sxs-lookup"><span data-stu-id="360e4-104">include attribute</span></span>

<span data-ttu-id="360e4-105">A instrução ACF **include** especifica um ou mais arquivos de cabeçalho a serem incluídos no código stub gerado.</span><span class="sxs-lookup"><span data-stu-id="360e4-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="360e4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="360e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360e4-107">*nomes*</span><span class="sxs-lookup"><span data-stu-id="360e4-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="360e4-108">Especifica o nome de um ou mais arquivos de cabeçalho de linguagem C.</span><span class="sxs-lookup"><span data-stu-id="360e4-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="360e4-109">Use o nome completo do arquivo, incluindo o. A extensão H e coloque cada nome de arquivo entre aspas.</span><span class="sxs-lookup"><span data-stu-id="360e4-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="360e4-110">Separe vários nomes de arquivos de cabeçalho de linguagem C com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="360e4-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="360e4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="360e4-111">Remarks</span></span>

<span data-ttu-id="360e4-112">Como resultado da instrução **include** , o código stub gerado conterá uma instrução C-pré-processador **\# include** .</span><span class="sxs-lookup"><span data-stu-id="360e4-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="360e4-113">Você fornece o arquivo de cabeçalho de linguagem C ao compilar os stubs.</span><span class="sxs-lookup"><span data-stu-id="360e4-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="360e4-114">As instruções include contam com o mecanismo do compilador C para pesquisar os arquivos incluídos na estrutura do diretório.</span><span class="sxs-lookup"><span data-stu-id="360e4-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="360e4-115">Use a diretiva de [**importação**](import.md) em vez da diretiva **include** para arquivos do sistema que contêm tipos de dados que você deseja disponibilizar para o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="360e4-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="360e4-116">A diretiva de **importação** ignora protótipos de função e permite que você use opções de compilador MIDL que otimizam a geração de rotinas de suporte.</span><span class="sxs-lookup"><span data-stu-id="360e4-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="360e4-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="360e4-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="360e4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="360e4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360e4-119">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="360e4-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="360e4-120">**importe**</span><span class="sxs-lookup"><span data-stu-id="360e4-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="360e4-121">Importando arquivos e bibliotecas de tipos</span><span class="sxs-lookup"><span data-stu-id="360e4-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="360e4-122">Importar arquivos de cabeçalho do sistema</span><span class="sxs-lookup"><span data-stu-id="360e4-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




