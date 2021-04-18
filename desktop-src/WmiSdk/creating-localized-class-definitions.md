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
# <a name="creating-localized-class-definitions"></a>Criando definições de classe localizadas

A criação de definições de classe localizadas é um processo de três etapas. Comece escrevendo o código MOF que define as classes, incluindo todos os qualificadores que devem ser localizados. Esse arquivo original é chamado de arquivo de "MOF mestre" porque contém todos os qualificadores e propriedades que definem a classe.

Em seguida, use o [compilador MOF](mofcomp.md) para criar as versões de linguagem neutra e específica do idioma do arquivo MOF. O compilador MOF coloca a descrição básica da classe em um novo arquivo MOF e cria uma versão localizada do arquivo MOF que contém apenas as propriedades e os qualificadores que devem ser localizados. Embora as versões específicas do idioma e do idioma neutro do arquivo MOF possam ter o mesmo nome de arquivo, você deve usar uma extensão de nome de arquivo. MFL para indicar que o arquivo contém informações localizadas. Você pode localizar o arquivo. MFL em outras localidades, se necessário. O armazenamento das definições de classe no repositório CIM requer uma etapa adicional de usar o compilador MOF para compilar os arquivos MOF de idioma neutro e específico do idioma.

As etapas a seguir descrevem como criar e armazenar uma definição de classe localizada.

**Para criar e armazenar uma definição de classe localizada**

1.  Crie o arquivo MOF mestre que define as classes que você deseja que sejam localizadas.

    Salve esse código MOF em um arquivo chamado Mastermof. mof.

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

2.  Crie versões de idioma neutros e específicas do idioma do arquivo MOF compilando o arquivo MasterMOF. mof.

    Digite o seguinte comando em um prompt de comando para compilar o arquivo MasterMOF. mof.

    **Mofcomp-MOF: Lnmof. mof-MFL: Lsmof. MFL-emenda: MS \_ 409 Mastermof. mof**

3.  Compile os arquivos de idioma neutro (Lnmof. MOF) e específicos do idioma (Lsmof. MFL) e armazene as informações de classe no repositório do CIM.

    Digite os comandos a seguir em um prompt de comando para armazenar as informações de classe no repositório CIM.

    **Mofcomp Lnmof. mof**

    **Mofcomp Lsmof. MFL**

    Depois de compilar esses arquivos, você terá uma definição de classe neutra de idioma no namespace de \\ teste raiz e uma definição de classe localizada no \\ namespace raiz \\ MS \_ 409 de teste. Para obter mais informações sobre como compilar arquivos MOF localizados, consulte [compilando arquivos MOF localizados](compiling-localized-mof-files.md).

 

 



