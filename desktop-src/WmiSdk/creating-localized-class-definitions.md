---
description: A criação de definições de classe localizadas é um processo de três etapas.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Criando definições de classe localizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105762173"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="67dfa-103">Criando definições de classe localizadas</span><span class="sxs-lookup"><span data-stu-id="67dfa-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="67dfa-104">A criação de definições de classe localizadas é um processo de três etapas.</span><span class="sxs-lookup"><span data-stu-id="67dfa-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="67dfa-105">Comece escrevendo o código MOF que define as classes, incluindo todos os qualificadores que devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="67dfa-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="67dfa-106">Esse arquivo original é chamado de arquivo de "MOF mestre" porque contém todos os qualificadores e propriedades que definem a classe.</span><span class="sxs-lookup"><span data-stu-id="67dfa-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="67dfa-107">Em seguida, use o [compilador MOF](mofcomp.md) para criar as versões de linguagem neutra e específica do idioma do arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="67dfa-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="67dfa-108">O compilador MOF coloca a descrição básica da classe em um novo arquivo MOF e cria uma versão localizada do arquivo MOF que contém apenas as propriedades e os qualificadores que devem ser localizados.</span><span class="sxs-lookup"><span data-stu-id="67dfa-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="67dfa-109">Embora as versões específicas do idioma e do idioma neutro do arquivo MOF possam ter o mesmo nome de arquivo, você deve usar uma extensão de nome de arquivo. MFL para indicar que o arquivo contém informações localizadas.</span><span class="sxs-lookup"><span data-stu-id="67dfa-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="67dfa-110">Você pode localizar o arquivo. MFL em outras localidades, se necessário.</span><span class="sxs-lookup"><span data-stu-id="67dfa-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="67dfa-111">O armazenamento das definições de classe no repositório CIM requer uma etapa adicional de usar o compilador MOF para compilar os arquivos MOF de idioma neutro e específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="67dfa-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="67dfa-112">As etapas a seguir descrevem como criar e armazenar uma definição de classe localizada.</span><span class="sxs-lookup"><span data-stu-id="67dfa-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="67dfa-113">**Para criar e armazenar uma definição de classe localizada**</span><span class="sxs-lookup"><span data-stu-id="67dfa-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="67dfa-114">Crie o arquivo MOF mestre que define as classes que você deseja que sejam localizadas.</span><span class="sxs-lookup"><span data-stu-id="67dfa-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="67dfa-115">Salve esse código MOF em um arquivo chamado Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="67dfa-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
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

2.  <span data-ttu-id="67dfa-116">Crie versões de idioma neutros e específicas do idioma do arquivo MOF compilando o arquivo MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="67dfa-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="67dfa-117">Digite o seguinte comando em um prompt de comando para compilar o arquivo MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="67dfa-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="67dfa-118">**Mofcomp-MOF: Lnmof. mof-MFL: Lsmof. MFL-emenda: MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="67dfa-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="67dfa-119">Compile os arquivos de idioma neutro (Lnmof. MOF) e específicos do idioma (Lsmof. MFL) e armazene as informações de classe no repositório do CIM.</span><span class="sxs-lookup"><span data-stu-id="67dfa-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="67dfa-120">Digite os comandos a seguir em um prompt de comando para armazenar as informações de classe no repositório CIM.</span><span class="sxs-lookup"><span data-stu-id="67dfa-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="67dfa-121">**Mofcomp Lnmof. mof**</span><span class="sxs-lookup"><span data-stu-id="67dfa-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="67dfa-122">**Mofcomp Lsmof. MFL**</span><span class="sxs-lookup"><span data-stu-id="67dfa-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="67dfa-123">Depois de compilar esses arquivos, você terá uma definição de classe neutra de idioma no namespace de \\ teste raiz e uma definição de classe localizada no \\ namespace raiz \\ MS \_ 409 de teste.</span><span class="sxs-lookup"><span data-stu-id="67dfa-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="67dfa-124">Para obter mais informações sobre como compilar arquivos MOF localizados, consulte [compilando arquivos MOF localizados](compiling-localized-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="67dfa-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



