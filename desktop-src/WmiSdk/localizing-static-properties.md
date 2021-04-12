---
description: Você pode localizar propriedades estáticas usando mapas de valores parciais.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Localizando propriedades estáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104298882"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="d9e68-103">Localizando propriedades estáticas</span><span class="sxs-lookup"><span data-stu-id="d9e68-103">Localizing Static Properties</span></span>

<span data-ttu-id="d9e68-104">Você pode localizar propriedades estáticas usando mapas de valores parciais.</span><span class="sxs-lookup"><span data-stu-id="d9e68-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="d9e68-105">O procedimento a seguir descreve como as propriedades estáticas podem ser localizadas usando mapas de valores parciais com expressões regulares.</span><span class="sxs-lookup"><span data-stu-id="d9e68-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="d9e68-106">**Para usar mapas de valor para localizar propriedades estáticas**</span><span class="sxs-lookup"><span data-stu-id="d9e68-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="d9e68-107">Crie um arquivo MOF mestre (Mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="d9e68-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="d9e68-108">O exemplo de código a seguir pode ser usado para criar um arquivo MOF mestre (Mastervm. MOF).</span><span class="sxs-lookup"><span data-stu-id="d9e68-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="d9e68-109">Crie as versões de linguagem neutra e específica do idioma do arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="d9e68-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="d9e68-110">Digite o comando a seguir em um prompt de comando para criar as versões de idioma neutro e específico do idioma do arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="d9e68-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="d9e68-111">O compilador MOF gera os arquivos MOF específicos de linguagem e neutros de idioma, LnVm. mof e LsVm. MFL.</span><span class="sxs-lookup"><span data-stu-id="d9e68-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="d9e68-112">Os valores em inglês americano para a propriedade [Numbers](numbers.md) são colocados no arquivo. MFL para o namespace American Inglês.</span><span class="sxs-lookup"><span data-stu-id="d9e68-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="d9e68-113">O exemplo de código a seguir mostra o conteúdo do arquivo LsVm. MFL.</span><span class="sxs-lookup"><span data-stu-id="d9e68-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="d9e68-114">Compile os dois arquivos MOF e armazene as informações de classe no repositório CIM.</span><span class="sxs-lookup"><span data-stu-id="d9e68-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="d9e68-115">Digite o seguinte comando em um prompt de comando para compilar os dois arquivos MOF.</span><span class="sxs-lookup"><span data-stu-id="d9e68-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="d9e68-116">Localize o arquivo MFL para outras localidades.</span><span class="sxs-lookup"><span data-stu-id="d9e68-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="d9e68-117">O exemplo de código a seguir mostra o conteúdo de um arquivo MFL para o namespace em francês.</span><span class="sxs-lookup"><span data-stu-id="d9e68-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="d9e68-118">O resultado líquido é que o nome de exibição e o valor da propriedade [Numbers](numbers.md) dependem da localidade do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="d9e68-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="d9e68-119">Se o usuário especificar uma localidade que não foi fornecida, os dados do qualificador padrão vêm do namespace em inglês (MS \_ 409).</span><span class="sxs-lookup"><span data-stu-id="d9e68-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="d9e68-120">A implicação desse design é que cada valor de cadeia de caracteres é usado como um identificador de pesquisa, que não pode ser localizado.</span><span class="sxs-lookup"><span data-stu-id="d9e68-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="d9e68-121">Ao definir esse esquema, você deve garantir que o valor que o provedor coloca é independente de localidade.</span><span class="sxs-lookup"><span data-stu-id="d9e68-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="d9e68-122">No momento, o WMI não fornece suporte de tempo de execução para mapear valores para cadeias de caracteres definidas por qualificadores.</span><span class="sxs-lookup"><span data-stu-id="d9e68-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="d9e68-123">A interpretação da sintaxe sugerida é a responsabilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d9e68-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



