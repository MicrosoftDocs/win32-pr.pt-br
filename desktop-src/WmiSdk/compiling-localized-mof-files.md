---
description: Você deve compilar o arquivo MOF mestre para criar os arquivos MOF de idioma neutro e específico do idioma.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilando arquivos MOF localizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297002"
---
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="c93da-103">Compilando arquivos MOF localizados</span><span class="sxs-lookup"><span data-stu-id="c93da-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="c93da-104">Você deve compilar o arquivo MOF mestre para criar os arquivos MOF de idioma neutro e específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="c93da-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="c93da-105">Digite o comando a seguir em um prompt de comando para compilar um arquivo MOF mestre.</span><span class="sxs-lookup"><span data-stu-id="c93da-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="c93da-106">**Mofcomp-MOF: Lnmof. mof-MFL: Lsmof. MFL-emenda: MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="c93da-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="c93da-107">Quando você executa esse comando, o compilador MOF cria dois arquivos MOF do arquivo original Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="c93da-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="c93da-108">O compilador MOF produz uma versão neutra de idioma, Lnmof. MOF, na qual todos os itens específicos do idioma são removidos.</span><span class="sxs-lookup"><span data-stu-id="c93da-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="c93da-109">Uma segunda versão específica de idioma, Lsmof. MOF, também é criada; Esse arquivo contém apenas os itens que foram marcados com o tipo de qualificador [**corrigido**](qualifier-flavors.md) no arquivo Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="c93da-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="c93da-110">O exemplo de código a seguir mostra o conteúdo do arquivo MOF neutro de idioma (Lnmof. MOF) que é gerado.</span><span class="sxs-lookup"><span data-stu-id="c93da-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

<span data-ttu-id="c93da-111">O exemplo de código a seguir mostra o conteúdo do arquivo MOF específico do idioma (Lsmof. MFL) que é gerado.</span><span class="sxs-lookup"><span data-stu-id="c93da-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

<span data-ttu-id="c93da-112">A compilação de um arquivo MOF com o qualificador [**corrigido**](qualifier-flavors.md) gera apenas arquivos MOF separados por idiomas e idiomas específicos. o repositório CIM não é atualizado com as novas informações de classe.</span><span class="sxs-lookup"><span data-stu-id="c93da-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="c93da-113">Você deve usar o compilador MOF para compilar os dois arquivos MOF que a primeira compilação produziu antes que qualquer informação de classe esteja disponível para o WMI.</span><span class="sxs-lookup"><span data-stu-id="c93da-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="c93da-114">Quando você compila um arquivo MOF mestre, somente os qualificadores com o tipo [**emendado**](qualifier-flavors.md) são movidos para o arquivo MOF específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="c93da-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="c93da-115">Os qualificadores que não têm o tipo **emendado** não são localizados e só existem na definição de classe básica no arquivo MOF com neutralidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="c93da-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="c93da-116">Qualificadores não-locais podem ser usados para descrições padrão se as descrições localizadas não estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c93da-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="c93da-117">Você pode usar o comando de [alteração de pragma](pragma-amendment.md) em vez de especificar [**emendado**](qualifier-flavors.md) como uma opção para o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="c93da-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="c93da-118">Qualquer uma dessas opções é equivalente a solicitar versões específicas do idioma e de idioma neutro de um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="c93da-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="c93da-119">Se você usar o comando de alteração de pragma ou a opção de linha de comando **corrigida** , deverá especificar o nome dos arquivos de saída usando as opções **-MFL** e **-MOF** no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="c93da-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="c93da-120">O arquivo MOF com neutralidade de idioma gerado pelo compilador MOF contém o equivalente Decimal da ID de localidade, mesmo que esse valor tenha sido inserido em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="c93da-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="c93da-121">No exemplo acima, o compilador converteu o valor 0x409 para o número decimal 1033 para o arquivo de saída Lnmof. mof.</span><span class="sxs-lookup"><span data-stu-id="c93da-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



