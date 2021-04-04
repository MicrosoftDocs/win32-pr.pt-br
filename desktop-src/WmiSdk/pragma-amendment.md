---
description: Direciona o compilador MOF para separar um arquivo MOF em versões de idioma neutros e específicas de idiomas.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: alteração de pragma
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
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647699"
---
# <a name="pragma-amendment"></a><span data-ttu-id="1e7c9-103">alteração de pragma</span><span class="sxs-lookup"><span data-stu-id="1e7c9-103">pragma amendment</span></span>

<span data-ttu-id="1e7c9-104">O comando de pré-processador de **alteração de pragma** direciona o compilador MOF para separar um arquivo MOF em versões de idioma neutros e específicas de idiomas.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="1e7c9-105">O arquivo MOF específico do idioma move os qualificadores corrigidos para um namespace para uma localidade específica.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="1e7c9-106">Em seguida, você compila os arquivos MOF específicos do idioma e do idioma neutro para armazenar informações de classe no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="1e7c9-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e7c9-107">Examples</span></span>

<span data-ttu-id="1e7c9-108">O exemplo a seguir mostra como criar um arquivo MOF que contém qualificadores corrigidos.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="1e7c9-109">Em seguida, você pode compilar o código MOF com o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="1e7c9-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="1e7c9-110">**Mofcomp** **-MOF: Lnmof. mof** **-MFL: Lsmof. MFL** **Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="1e7c9-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="1e7c9-111">O comando instrui o compilador MOF a produzir dois arquivos MOF do arquivo original Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="1e7c9-112">O compilador MOF produz uma versão neutra de idioma do arquivo MOF, chamada Lnmof. MOF, com todos os itens específicos do idioma removidos.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="1e7c9-113">O compilador também cria um segundo arquivo MOF específico de idioma chamado Lsmof. MFL que contém apenas os itens que você deve localizar.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="1e7c9-114">Ao dividir um arquivo MOF com o qualificador de **emenda** ou o comando de **alteração de pragma** , você deve especificar as opções **-MOF** e **-MFL** .</span><span class="sxs-lookup"><span data-stu-id="1e7c9-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="1e7c9-115">Caso contrário, o compilador não gerará nenhum arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="1e7c9-116">Em seguida, você deve compilar os dois arquivos de saída para disponibilizar as informações de classe para o WMI.</span><span class="sxs-lookup"><span data-stu-id="1e7c9-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
```



## <a name="requirements"></a><span data-ttu-id="1e7c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e7c9-117">Requirements</span></span>



| <span data-ttu-id="1e7c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e7c9-118">Requirement</span></span> | <span data-ttu-id="1e7c9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1e7c9-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1e7c9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e7c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7c9-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e7c9-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1e7c9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e7c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7c9-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e7c9-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e7c9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e7c9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e7c9-125">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="1e7c9-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




