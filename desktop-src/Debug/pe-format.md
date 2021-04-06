---
description: Esta especificação descreve a estrutura de arquivos executáveis (imagem) e arquivos de objeto na família de sistemas operacionais Windows. Esses arquivos são chamados de executável portátil (PE) e arquivos de formato de arquivo de objeto comum (COFF), respectivamente.
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: Formato PE
ms.topic: article
ms.date: 08/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 257185019f329e0d4431ca61d1d88e2c0347f133
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2021
ms.locfileid: "103919672"
---
# <a name="pe-format"></a>Formato PE

Esta especificação descreve a estrutura de arquivos executáveis (imagem) e arquivos de objeto na família de sistemas operacionais Windows. Esses arquivos são chamados de executável portátil (PE) e arquivos de formato de arquivo de objeto comum (COFF), respectivamente.

> [!Note]  
> Este documento é fornecido para auxiliar no desenvolvimento de ferramentas e aplicativos para Windows, mas não é garantido que seja uma especificação completa em todos os aspectos. A Microsoft se reserva o direito de alterar este documento sem aviso prévio.

Essa revisão do executável portátil da Microsoft e da especificação de formato de arquivo de objeto comum substitui todas as revisões anteriores dessa especificação.

## <a name="general-concepts"></a>Conceitos gerais

Este documento especifica a estrutura de arquivos executáveis (imagem) e arquivos de objeto na família Microsoft Windows de sistemas operacionais. Esses arquivos são chamados de executável portátil (PE) e arquivos de formato de arquivo de objeto comum (COFF), respectivamente. O nome "executável portátil" refere-se ao fato de que o formato não é específico da arquitetura.

Determinados conceitos que aparecem durante essa especificação são descritos na tabela a seguir:

| Nome                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| certificado de atributo <br/> | Um certificado que é usado para associar instruções verificáveis a uma imagem. Várias instruções verificáveis diferentes podem ser associadas a um arquivo; uma das mais úteis é uma instrução de um fabricante de software que indica qual deve ser o resumo da mensagem da imagem. Um resumo de mensagem é semelhante a uma soma de verificação, exceto pelo fato de que é extremamente difícil de forjar. Portanto, é muito difícil modificar um arquivo para ter o mesmo Resumo de mensagem que o arquivo original. A instrução pode ser verificada como sendo feita pelo fabricante usando esquemas de criptografia de chave pública ou privada. Este documento descreve detalhes sobre certificados de atributo diferentes de para permitir sua inserção em arquivos de imagem. <br/> |
| carimbo de data/hora <br/>       | Um carimbo que é usado para finalidades diferentes em vários locais em um arquivo. PE ou COFF. Na maioria dos casos, o formato de cada carimbo é o mesmo usado pelas funções de tempo na biblioteca de tempo de execução do C. Para exceções, consulte a inscriptização do tipo de depuração de imagem \_ \_ \_ reprodução em [tipo de depuração](#debug-type). Se o valor do carimbo for 0 ou 0xFFFFFFFF, ele não representará um carimbo de data/hora real ou significativo. <br/>                                                                                                                                                                                                                                                                                                                                            |
| ponteiro de arquivo <br/>          | O local de um item dentro do próprio arquivo, antes de ser processado pelo vinculador (no caso de arquivos de objeto) ou o carregador (no caso de arquivos de imagem). Em outras palavras, essa é uma posição dentro do arquivo, conforme armazenado em disco. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| vinculador <br/>                | Uma referência ao vinculador que é fornecida com Microsoft Visual Studio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| arquivo de objeto <br/>           | Um arquivo que é fornecido como entrada para o vinculador. O vinculador produz um arquivo de imagem que, por sua vez, é usado como entrada pelo carregador. O termo "arquivo de objeto" não implica necessariamente nenhuma conexão com a programação orientada a objeto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| reservado, deve ser 0 <br/>   | Uma descrição de um campo que indica que o valor do campo deve ser zero para geradores e consumidores devem ignorar o campo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Endereço virtual relativo (RVA) <br/>                   | Em um arquivo de imagem, esse é o endereço de um item depois que ele é carregado na memória, com o endereço base do arquivo de imagem subtraído dele. O RVA de um item quase sempre difere de sua posição dentro do arquivo no disco (ponteiro de arquivo). <br/> Em um arquivo de objeto, um RVA é menos significativo porque os locais de memória não são atribuídos. Nesse caso, um RVA seria um endereço dentro de uma seção (descrita posteriormente nesta tabela), à qual uma realocação é aplicada posteriormente durante a vinculação. Para simplificar, um compilador deve apenas definir o primeiro RVA em cada seção como zero. <br/>                                                                                                                                         |
| section <br/>               | A unidade básica de código ou dados em um arquivo. PE ou COFF. Por exemplo, todo o código em um arquivo de objeto pode ser combinado em uma única seção ou (dependendo do comportamento do compilador) cada função pode ocupar sua própria seção. Com mais seções, há mais sobrecarga de arquivo, mas o vinculador é capaz de vincular o código de forma mais seletiva. Uma seção é semelhante a um segmento na arquitetura Intel 8086. Todos os dados brutos em uma seção devem ser carregados de forma contígua. Além disso, um arquivo de imagem pode conter várias seções, como. TLS ou. realocação, que têm finalidades especiais. <br/>                                                                                                                                                                      |
| Endereço virtual (VA) <br/>                    | O mesmo que RVA, exceto pelo fato de que o endereço base do arquivo de imagem não é subtraído. O endereço é chamado de VA porque o Windows cria um espaço de VA distinto para cada processo, independentemente da memória física. Para quase todas as finalidades, um VA deve ser considerado apenas um endereço. Um VA não é tão previsível como RVA porque o carregador pode não carregar a imagem em seu local preferido. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Visão geral

A lista a seguir descreve o formato executável do Microsoft PE, com a base do cabeçalho da imagem na parte superior. A seção do cabeçalho EXE compatível com MS-DOS 2,0 até a seção não utilizada logo antes do cabeçalho PE é a seção do MS-DOS 2,0 e é usada apenas para compatibilidade com MS-DOS.

-   Cabeçalho EXE compatível com MS-DOS 2,0
-   unused
-   Identificador OEM

    Informações de OEM

    Deslocamento para o cabeçalho PE

-   Programa stub do MS-DOS 2,0 e tabela de realocação

-   unused

-   Cabeçalho PE (alinhado ao limite de 8 bytes)

-   Cabeçalhos de seção
-   Páginas de imagem:

    importar informações

    exportar informações

    realocações de base

    informações do recurso

A lista a seguir descreve o formato de módulo do objeto COFF da Microsoft:

-   Cabeçalho COFF da Microsoft
-   Cabeçalhos de seção
-   Dados brutos:

    code

    data

    informações de depuração

    relocações

## <a name="file-headers"></a>Cabeçalhos de arquivo

- [Stub do MS-DOS (somente imagem)](#ms-dos-stub-image-only)
- [Assinatura (somente imagem)](#signature-image-only)
- [Cabeçalho de arquivo COFF (objeto e imagem)](#coff-file-header-object-and-image)
  - [Tipos de máquina](#machine-types)
  - [Características](#characteristics)
- [Cabeçalho opcional (somente imagem)](#optional-header-image-only)
  - [Campos padrão de cabeçalho opcional (somente imagem)](#optional-header-standard-fields-image-only)
  - [Campos de Windows-Specific de cabeçalho opcionais (somente imagem)](#optional-header-windows-specific-fields-image-only)
  - [Diretórios de dados de cabeçalho opcionais (somente imagem)](#optional-header-data-directories-image-only)

O cabeçalho do arquivo PE consiste em um stub do Microsoft MS-DOS, a assinatura do PE, o cabeçalho do arquivo COFF e um cabeçalho opcional. Um cabeçalho de arquivo de objeto COFF consiste em um cabeçalho de arquivo COFF e um cabeçalho opcional. Em ambos os casos, os cabeçalhos de arquivo são seguidos imediatamente por cabeçalhos de seção.

### <a name="ms-dos-stub-image-only"></a>Stub do MS-DOS (somente imagem)

O stub do MS-DOS é um aplicativo válido que é executado no MS-DOS. Ele é colocado na frente da imagem EXE. O vinculador coloca um stub padrão aqui, que imprime a mensagem "este programa não pode ser executado no modo DOS" quando a imagem é executada no MS-DOS. O usuário pode especificar um stub diferente usando a opção de vinculador/STUB.

No local 0x3C, o stub tem o deslocamento do arquivo para a assinatura do PE. Essas informações permitem que o Windows execute corretamente o arquivo de imagem, embora tenha um stub do MS-DOS. Esse deslocamento de arquivo é colocado no local 0x3C durante a vinculação.

### <a name="signature-image-only"></a>Assinatura (somente imagem)

Após o stub do MS-DOS, no deslocamento do arquivo especificado em offset 0x3C, é uma assinatura de 4 bytes que identifica o arquivo como um arquivo de imagem de formato PE. Essa assinatura é "PE \\ 0 \\ 0" (as letras "P" E "e" seguidas por dois bytes nulos).

### <a name="coff-file-header-object-and-image"></a>Cabeçalho de arquivo COFF (objeto e imagem)

No início de um arquivo de objeto, ou imediatamente após a assinatura de um arquivo de imagem, é um cabeçalho de arquivo COFF padrão no formato a seguir. Observe que o carregador do Windows limita o número de seções a 96.

| Deslocamento         | Tamanho          | Campo                            | Descrição                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Computador <br/>              | O número que identifica o tipo de computador de destino. Para obter mais informações, consulte [tipos de máquina](#machine-types). <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | O número de seções. Isso indica o tamanho da tabela da seção, que segue imediatamente os cabeçalhos. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | Os poucos 32 bits do número de segundos desde 00:00 de janeiro de 1970 (um valor t de tempo de execução \_ do C), que indica quando o arquivo foi criado. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | O deslocamento do arquivo da tabela de símbolos COFF ou zero se nenhuma tabela de símbolos COFF estiver presente. Esse valor deve ser zero para uma imagem porque as informações de depuração COFF foram preteridas. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | O número de entradas na tabela de símbolos. Esses dados podem ser usados para localizar a tabela de cadeia de caracteres, que segue imediatamente a tabela de símbolos. Esse valor deve ser zero para uma imagem porque as informações de depuração COFF foram preteridas. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | O tamanho do cabeçalho opcional, que é necessário para arquivos executáveis, mas não para arquivos de objeto. Esse valor deve ser zero para um arquivo-objeto. Para obter uma descrição do formato de cabeçalho, consulte [cabeçalho opcional (somente imagem)](#optional-header-image-only). <br/> |
| 18 <br/> | 2 <br/> | Características <br/>      | Os sinalizadores que indicam os atributos do arquivo. Para obter valores de sinalizador específicos, consulte [características](#characteristics). <br/>                                                                                                                               |

#### <a name="machine-types"></a>Tipos de máquina

O campo computador tem um dos seguintes valores, que especificam o tipo de CPU. Um arquivo de imagem pode ser executado somente no computador especificado ou em um sistema que emula o computador especificado.

| Constante                                    | Valor              | Descrição                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| computador de arquivo de imagem \_ \_ \_ desconhecido <br/>   | 0x0 <br/>    | Presume-se que o conteúdo deste campo seja aplicável a qualquer tipo de computador <br/> |
| \_AM33 da \_ máquina do arquivo de imagem \_ <br/>      | 0x1d3 <br/>  | Matsushita AM33 <br/>                                                             |
| Máquina de arquivo de imagem \_ \_ \_ AMD64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| \_ARM de \_ máquina de arquivo de imagem \_ <br/>       | 0x1c0 <br/>  | little endian ARM <br/>                                                           |
| \_ARM64 da \_ máquina do arquivo de imagem \_ <br/>     | 0xaa64 <br/> | little endian ARM64 <br/>                                                         |
| \_ARMNT da \_ máquina do arquivo de imagem \_ <br/>     | 0x1c4 <br/>  | ARM Thumb-2 little endian <br/>                                                   |
| computador de arquivo de imagem \_ \_ \_ EBC <br/>       | 0xebc <br/>  | Código de byte EFI <br/>                                                               |
| Arquivo de imagem/ \_ \_ computador \_ i386 <br/>      | 0x14c <br/>  | Processadores Intel 386 ou posteriores e processadores compatíveis <br/>                     |
| Computador de arquivo de imagem \_ \_ \_ IA64 <br/>      | 0x200 <br/>  | Família de processadores Intel Itanium <br/>                                              |
| \_M32R da \_ máquina do arquivo de imagem \_ <br/>      | 0x9041 <br/> | Mitsubishi M32R little endian <br/>                                               |
| \_MIPS16 da \_ máquina do arquivo de imagem \_ <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| \_MIPSFPU da \_ máquina do arquivo de imagem \_ <br/>   | 0x366 <br/>  | MIPS com FPU <br/>                                                               |
| \_MIPSFPU16 da \_ máquina do arquivo de imagem \_ <br/> | 0x466 <br/>  | MIPS16 com FPU <br/>                                                             |
| \_POWERPC de \_ máquina de arquivo de imagem \_ <br/>   | 0x1f0 <br/>  | little endian do Power PC <br/>                                                      |
| \_POWERPCFP da \_ máquina do arquivo de imagem \_ <br/> | 0x1f1 <br/>  | Power PC com suporte de ponto flutuante <br/>                                        |
| \_R4000 da \_ máquina do arquivo de imagem \_ <br/>     | 0x166 <br/>  | little endian MIPS <br/>                                                          |
| \_RISCV32 da \_ máquina do arquivo de imagem \_ <br/>   | 0x5032 <br/> | Espaço de endereço de 32 de bit RISC-V <br/>                                                 |
| \_RISCV64 da \_ máquina do arquivo de imagem \_ <br/>   | 0x5064 <br/> | Espaço de endereço de 64 de bit RISC-V <br/>                                                 |
| \_RISCV128 da \_ máquina do arquivo de imagem \_ <br/>  | 0x5128 <br/> | Espaço de endereço de 128 de bit RISC-V <br/>                                                |
| \_SH3 da \_ máquina do arquivo de imagem \_ <br/>       | 0x1a2 <br/>  | SH3 Hitachi <br/>                                                                 |
| \_SH3DSP da \_ máquina do arquivo de imagem \_ <br/>    | 0x1a3 <br/>  | DSP Hitachi SH3 <br/>                                                             |
| \_Sh4 da \_ máquina do arquivo de imagem \_ <br/>       | 0x1a6 <br/>  | SH4 Hitachi <br/>                                                                 |
| \_SH5 da \_ máquina do arquivo de imagem \_ <br/>       | 0x1a8 <br/>  | SH5 Hitachi <br/>                                                                 |
| \_miniatura do \_ computador do arquivo de imagem \_ <br/>     | 0x1c2 <br/>  | Posição <br/>                                                                       |
| \_WCEMIPSV2 da \_ máquina do arquivo de imagem \_ <br/> | 0x169 <br/>  | MIPS little-endian Stone v2 <br/>                                                   |

#### <a name="characteristics"></a>Características

O campo características contém sinalizadores que indicam os atributos do arquivo de objeto ou de imagem. Os seguintes sinalizadores estão definidos no momento:

| Sinalizador                                                 | Valor              | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| arquivo de imagem \_ \_ RELOCS \_ removido <br/>            | 0x0001 <br/> | Somente imagem, Windows CE e Microsoft Windows NT e posterior. Isso indica que o arquivo não contém realocações de base e, portanto, deve ser carregado em seu endereço base preferencial. Se o endereço base não estiver disponível, o carregador relatará um erro. O comportamento padrão do vinculador é remover as realocações de base dos arquivos executáveis (EXE). <br/> |
| \_ \_ imagem executável do arquivo de imagem \_ <br/>           | 0x0002 <br/> | Somente imagem. Isso indica que o arquivo de imagem é válido e pode ser executado. Se esse sinalizador não for definido, isso indicará um erro de vinculador. <br/>                                                                                                                                                                                                                          |
| NUMS de linha de arquivo de imagem \_ \_ \_ \_ removido <br/>        | 0x0004 <br/> | Os números de linha COFF foram removidos. Esse sinalizador foi preterido e deve ser zero. <br/>                                                                                                                                                                                                                                                                       |
| arquivo de imagem \_ \_ local \_ SYMS \_ removido <br/>       | 0x0008 <br/> | As entradas da tabela de símbolos COFF para símbolos locais foram removidas. Esse sinalizador foi preterido e deve ser zero. <br/>                                                                                                                                                                                                                                             |
| arquivo de imagem \_ \_ agressiva \_ WS \_ Trim <br/>        | 0x0010 <br/> | Obsoleto. Corte agressivo de conjunto de trabalho. Esse sinalizador foi preterido para o Windows 2000 e posterior e deve ser zero. <br/>                                                                                                                                                                                                                                          |
| \_reconhecimento de \_ \_ endereço grande de arquivo \_ de imagem <br/>      | 0x0020 <br/> | O aplicativo pode manipular > endereços de 2 GB. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Esse sinalizador é reservado para uso futuro. <br/>                                                                                                                                                                                                                                                                                                                  |
| BYTES de arquivo de imagem \_ \_ \_ invertidos \_ <br/>         | 0x0080 <br/> | Little endian: o bit menos significativo (LSB) precede o bit mais significativo (MSB) na memória. Esse sinalizador foi preterido e deve ser zero. <br/>                                                                                                                                                                                                          |
| \_Computador de \_ 32 bits do arquivo de imagem \_ <br/>              | 0x0100 <br/> | O computador é baseado em uma arquitetura de palavra de 32 bits. <br/>                                                                                                                                                                                                                                                                                                        |
| depuração de arquivo de imagem \_ \_ \_ eliminada <br/>             | 0x0200 <br/> | As informações de depuração são removidas do arquivo de imagem. <br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ execução removível \_ do arquivo \_ de imagem da \_ permuta <br/> | 0x0400 <br/> | Se a imagem estiver em mídia removível, carregue-a completamente e copie-a para o arquivo de permuta. <br/>                                                                                                                                                                                                                                                                        |
| \_arquivo \_ de imagem NET \_ Run \_ da \_ permuta <br/>        | 0x0800 <br/> | Se a imagem estiver na mídia de rede, carregue-a completamente e copie-a para o arquivo de permuta. <br/>                                                                                                                                                                                                                                                                          |
| \_sistema de arquivos de imagem \_ <br/>                      | 0x1000 <br/> | O arquivo de imagem é um arquivo de sistema, não um programa de usuário. <br/>                                                                                                                                                                                                                                                                                                   |
| \_dll do arquivo de imagem \_ <br/>                         | 0x2000 <br/> | O arquivo de imagem é uma DLL (biblioteca de vínculo dinâmico). Esses arquivos são considerados arquivos executáveis para quase todas as finalidades, embora não possam ser executados diretamente. <br/>                                                                                                                                                                                              |
| IMAGEM \_ \_ \_ somente sistema de \_ arquivos <br/>            | 0x4000 <br/> | O arquivo deve ser executado somente em um computador com um processador. <br/>                                                                                                                                                                                                                                                                                                 |
| BYTES de arquivo de imagem \_ \_ \_ revertidos- \_ Olá <br/>         | 0x8000 <br/> | Big endian: o MSB precede o LSB na memória. Esse sinalizador foi preterido e deve ser zero. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Cabeçalho opcional (somente imagem)

Cada arquivo de imagem tem um cabeçalho opcional que fornece informações para o carregador. Esse cabeçalho é opcional no sentido de que alguns arquivos (especificamente, arquivos de objeto) não o têm. Para arquivos de imagem, esse cabeçalho é necessário. Um arquivo de objeto pode ter um cabeçalho opcional, mas geralmente esse cabeçalho não tem nenhuma função em um arquivo de objeto, exceto para aumentar seu tamanho.

Observe que o tamanho do cabeçalho opcional não é fixo. O campo **SizeOfOptionalHeader** no cabeçalho COFF deve ser usado para validar que uma investigação no arquivo de um determinado diretório de dados não vai além de **SizeOfOptionalHeader**. Para obter mais informações, consulte [cabeçalho de arquivo COFF (objeto e imagem)](#coff-file-header-object-and-image).

O campo **NumberOfRvaAndSizes** do cabeçalho opcional também deve ser usado para garantir que nenhuma investigação de uma entrada de diretório de dados específica vá além do cabeçalho opcional. Além disso, é importante validar o número mágico do cabeçalho opcional para a compatibilidade de formato.

O número mágico do cabeçalho opcional determina se uma imagem é um PE32 ou PE32 + executável.

| Número mágico      | Formato PE         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32 + <br/> |

As imagens PE32 + permitem um espaço de endereço de 64 bits, limitando o tamanho da imagem a 2 gigabytes. Outras PE32 + modificações são abordadas em suas respectivas seções.

O cabeçalho opcional em si tem três partes principais.

| Deslocamento (PE32/PE32 +) | Tamanho (PE32/PE32 +)    | Parte do cabeçalho                         | Descrição                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Campos padrão <br/>         | Campos que são definidos para todas as implementações de COFF, incluindo UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Campos específicos do Windows <br/> | Campos adicionais para dar suporte a recursos específicos do Windows (por exemplo, subsistemas). <br/>                                                                              |
| 96/112 <br/>  | Variável <br/> | Diretórios de dados <br/>        | Pares de endereço/tamanho para tabelas especiais encontradas no arquivo de imagem e são usados pelo sistema operacional (por exemplo, a tabela de importação e a tabela de exportação). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Campos padrão de cabeçalho opcional (somente imagem)

Os oito primeiros campos do cabeçalho opcional são campos padrão que são definidos para cada implementação de COFF. Esses campos contêm informações gerais que são úteis para carregar e executar um arquivo executável. Eles não são alterados para o formato PE32 +.

| Deslocamento         | Tamanho          | Campo                               | Descrição                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Mágica <br/>                   | O inteiro sem sinal que identifica o estado do arquivo de imagem. O número mais comum é 0x10B, que o identifica como um arquivo executável normal. 0x107 o identifica como uma imagem de ROM e 0x20B a identifica como um PE32 + executável. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | O número da versão principal do vinculador. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | O número da versão secundária do vinculador. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | O tamanho da seção de código (texto) ou a soma de todas as seções de código se houver várias seções. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | O tamanho da seção de dados inicializados ou a soma de todas essas seções, se houver várias seções de dados. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | O tamanho da seção de dados não inicializado (BSS) ou a soma de todas essas seções, se houver várias seções BSS. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | O endereço do ponto de entrada relativo à imagem base quando o arquivo executável é carregado na memória. Para imagens de programa, esse é o endereço inicial. Para drivers de dispositivo, esse é o endereço da função de inicialização. Um ponto de entrada é opcional para DLLs. Quando nenhum ponto de entrada está presente, esse campo deve ser zero. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | O endereço relativo à base da imagem da seção de início de código quando ela é carregada na memória. <br/>                                                                                                                                                                                                                    |

PE32 contém este campo adicional, que está ausente no PE32 +, após BaseOfCode.

| Deslocamento         | Tamanho          | Campo                  | Descrição                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | O endereço relativo à base da imagem da seção de início de dados quando ela é carregada na memória. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Campos de Windows-Specific de cabeçalho opcionais (somente imagem)

Os próximos 21 campos são uma extensão para o formato de cabeçalho opcional COFF. Eles contêm informações adicionais que são exigidas pelo vinculador e pelo carregador no Windows.

| Deslocamento (PE32/PE32 +) | Tamanho (PE32/PE32 +) | Campo                                   | Descrição                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase <br/>                   | O endereço preferencial do primeiro byte de imagem quando carregado na memória; deve ser um múltiplo de 64 K. O padrão para DLLs é 0x10000000. O padrão para Windows CE EXEs é 0x00010000. O padrão para Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 e Windows me é 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | O alinhamento (em bytes) das seções quando elas são carregadas na memória. Ele deve ser maior ou igual ao alinhamento de File. O padrão é o tamanho da página para a arquitetura. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | O fator de alinhamento (em bytes) usado para alinhar os dados brutos das seções no arquivo de imagem. O valor deve ser uma potência de 2 entre 512 e 64 K, inclusive. O padrão é 512. Se o SectionAlignment for menor que o tamanho da página da arquitetura, o FileAlignment deverá corresponder a SectionAlignment. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | O número de versão principal do sistema operacional necessário. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | O número de versão secundária do sistema operacional necessário. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | O número de versão principal da imagem. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | O número de versão secundária da imagem. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | O número de versão principal do subsistema. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | O número de secundária principal do subsistema. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Reservado, deve ser zero. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | O tamanho (em bytes) da imagem, incluindo todos os cabeçalhos, à medida que a imagem é carregada na memória. Ele deve ser um múltiplo de SectionAlignment. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | O tamanho combinado de um stub do MS-DOS, cabeçalho PE e cabeçalhos de seção arredondados para um múltiplo de alinhamento de File. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | Soma <br/>                    | A soma de verificação do arquivo de imagem. O algoritmo para computar a soma de verificação é incorporado em IMAGHELP.DLL. Os itens a seguir são verificados para validação no tempo de carregamento: todos os drivers, qualquer DLL carregada no momento da inicialização e qualquer DLL que é carregada em um processo crítico do Windows. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsistema <br/>                   | O subsistema necessário para executar esta imagem. Para obter mais informações, consulte [subsistema do Windows](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Para obter mais informações, consulte [características de dll](#dll-characteristics) mais adiante nesta especificação. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | O tamanho da pilha a ser reservada. Somente SizeOfStackCommit é confirmado; o restante é disponibilizado uma página por vez até que o tamanho da reserva seja atingido. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | O tamanho da pilha a ser confirmada. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | O tamanho do espaço de heap local a ser reservado. Somente SizeOfHeapCommit é confirmado; o restante é disponibilizado uma página por vez até que o tamanho da reserva seja atingido. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | O tamanho do espaço de heap local a ser confirmado. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Reservado, deve ser zero. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | O número de entradas de diretório de dados no restante do cabeçalho opcional. Cada uma descreve uma localização e um tamanho. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Subsistema do Windows

Os valores a seguir definidos para o campo subsistema do cabeçalho opcional determinam qual subsistema do Windows (se houver) é necessário para executar a imagem.

| Constante                                                  | Valor          | Descrição                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| subsistema de imagem \_ \_ desconhecido <br/>                     | 0 <br/>  | Um subsistema desconhecido <br/>                                 |
| subsistema de imagem \_ \_ nativo <br/>                      | 1 <br/>  | Drivers de dispositivo e processos nativos do Windows <br/>          |
| \_GUI do Windows do SUBsistema de imagens \_ \_ <br/>                | 2 <br/>  | O subsistema GUI (interface gráfica do usuário) do Windows <br/> |
| \_Cui do Windows do SUBsistema de imagem \_ \_ <br/>                | 3 <br/>  | O subsistema de caracteres do Windows <br/>                      |
| \_Cui OS2 do SUBsistema de imagens \_ \_ <br/>                    | 5 <br/>  | O subsistema do sistema operacional/2 <br/>                         |
| \_Cui POSIX do SUBsistema de imagem \_ \_ <br/>                  | 7 <br/>  | O subsistema de caracteres POSIX <br/>                        |
| \_ \_ janelas nativas do subsistema de imagens \_ <br/>             | 8 <br/>  | Driver Win9x nativo <br/>                                  |
| subsistema da imagem \_ \_ GUI do Windows \_ CE \_ <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| \_aplicativo EFI do SUBsistema de imagens \_ \_ <br/>            | 10 <br/> | Um aplicativo EFI (Extensible Firmware Interface) <br/>   |
| \_Driver do \_ \_ serviço de inicialização \_ EFI \_ do subsistema de imagens <br/> | 11 <br/> | Um driver EFI com serviços de inicialização <br/>                     |
| \_Driver de \_ tempo de \_ execução EFI do SUBsistema de imagem \_ <br/>       | 12 <br/> | Um driver EFI com serviços de tempo de execução <br/>                 |
| \_ \_ EFI ROM do subsistema de imagens \_ <br/>                    | 13 <br/> | Uma imagem EFI ROM <br/>                                     |
| \_Xbox do SUBsistema de imagens \_ <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| \_aplicativo de inicialização do Windows do SUBsistema de imagens \_ \_ \_ <br/>  | 16 <br/> | Aplicativo de inicialização do Windows. <br/>                            |

##### <a name="dll-characteristics"></a>Características de DLL

Os valores a seguir são definidos para o campo DllCharacteristics do cabeçalho opcional.

| Constante                                                             | Valor              | Descrição                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Reservado, deve ser zero. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Reservado, deve ser zero. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Reservado, deve ser zero. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Reservado, deve ser zero. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ alta \_ entropia \_ VA <br/>             | 0x0020 <br/> | A imagem pode lidar com um espaço de endereço virtual de alta entropia de 64 bits. <br/>                               |
| DLLCHARACTERISTICS de imagem \_\_ <br/> \_base dinâmica <br/>    | 0x0040 <br/> | A DLL pode ser realocada no tempo de carregamento. <br/>                                                          |
| DLLCHARACTERISTICS de imagem \_\_ <br/> FORÇAR \_ integridade <br/> | 0x0080 <br/> | As verificações de integridade de código são impostas. <br/>                                                         |
| DLLCHARACTERISTICS de imagem \_\_ <br/> compatível com NX \_ <br/>       | 0x0100 <br/> | A imagem é compatível com NX. <br/>                                                                     |
| DLLCHARACTERISTICS de imagem \_ \_ sem \_ isolamento <br/>                | 0x0200 <br/> | Reconhecimento de isolamento, mas não Isole a imagem. <br/>                                              |
| DLLCHARACTERISTICS de imagem \_ \_ sem \_ Seh <br/>                      | 0x0400 <br/> | Não usa manipulação de exceção estruturada (SE). Nenhum manipulador SE pode ser chamado nesta imagem. <br/> |
| DLLCHARACTERISTICS de imagem \_ \_ sem \_ Associação <br/>                     | 0x0800 <br/> | Não associe a imagem. <br/>                                                                      |
| \_APPCONTAINER DLLCHARACTERISTICS de imagem \_ <br/>                  | 0x1000 <br/> | A imagem deve ser executada em um AppContainer. <br/>                                                      |
| \_ \_ driver WDM do Image DLLCHARACTERISTICS \_ <br/>                  | 0x2000 <br/> | Um driver WDM. <br/>                                                                               |
| IMAGE \_ DLLCHARACTERISTICS \_ Guard \_ CF <br/>                     | 0x4000 <br/> | A imagem dá suporte à proteção de fluxo de controle. <br/>                                                          |
| reconhecimento de imagem \_ \_ do DLLCHARACTERISTICS terminal \_ Server \_ <br/>      | 0x8000 <br/> | Terminal Server ciente. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Diretórios de dados de cabeçalho opcionais (somente imagem)

Cada diretório de dados fornece o endereço e o tamanho de uma tabela ou cadeia de caracteres que o Windows usa. Essas entradas de diretório de dados são carregadas na memória para que o sistema possa usá-las em tempo de execução. Um diretório de dados é um campo de 8 bytes que tem a seguinte declaração:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

O primeiro campo, VirtualAddress, é, na verdade, o RVA da tabela. O RVA é o endereço da tabela em relação ao endereço base da imagem quando a tabela é carregada. O segundo campo fornece o tamanho em bytes. Os diretórios de dados, que formam a última parte do cabeçalho opcional, são listados na tabela a seguir.

Observe que o número de diretórios não é fixo. Antes de procurar um diretório específico, verifique o campo NumberOfRvaAndSizes no cabeçalho opcional.

Além disso, não presuma que o RVAs nesta tabela aponte para o início de uma seção ou que as seções que contêm tabelas específicas têm nomes específicos.

| Deslocamento (PE/PE32 +)   | Tamanho          | Campo                               | Descrição                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Exportar tabela <br/>            | O tamanho e o endereço da tabela de exportação. Para obter mais informações, consulte a [seção. Edata (somente imagem)](#the-edata-section-image-only). <br/>                                                |
| 104/120 <br/> | 8 <br/> | Importar tabela <br/>            | O tamanho e o endereço da tabela de importação. Para obter mais informações, consulte [a seção. iData](#the-idata-section).<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Tabela de recursos <br/>          | O tamanho e o endereço da tabela de recursos. Para obter mais informações, consulte [a seção. rsrc](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Tabela de exceção <br/>         | O tamanho e o endereço da tabela de exceção. Para obter mais informações, consulte [a seção. pData](#the-pdata-section). <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Tabela de certificados <br/>       | O tamanho e o endereço da tabela do certificado de atributo. Para obter mais informações, consulte [a tabela de certificados de atributo (somente imagem)](#the-attribute-certificate-table-image-only). <br/> |
| 136/152 <br/> | 8 <br/> | Tabela de realocação base <br/>   | O tamanho e o endereço da tabela de realocação de base. Para obter mais informações, consulte [a seção. realocação (somente imagem)](#the-reloc-section-image-only).<br/>                                   |
| 144/160 <br/> | 8 <br/> | Depurar <br/>                   | O endereço e o tamanho inicial dos dados de depuração. Para obter mais informações, consulte [a seção. Debug](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Arquitetura <br/>            | Reservado, deve ser 0 <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | PTR global <br/>              | O RVA do valor a ser armazenado no registro do ponteiro global. O membro de tamanho dessa estrutura deve ser definido como zero. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | Tabela TLS <br/>               | O endereço e o tamanho da tabela do armazenamento local de threads (TLS). Para obter mais informações, [a seção. TLS](#the-tls-section).<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Carregar tabela de configuração <br/>       | O tamanho e o endereço da tabela de configuração de carregamento. Para obter mais informações, [a estrutura de configuração de carregamento (somente imagem)](#the-load-configuration-structure-image-only).<br/>       |
| 184/200 <br/> | 8 <br/> | Importação associada <br/>            | O tamanho e o endereço da tabela de importação vinculada. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | IAT <br/>                     | O tamanho e o endereço da tabela de endereços de importação. Para obter mais informações, consulte [importar tabela de endereços](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Atrasar descritor de importação <br/> | O tamanho e o endereço do descritor de importação de atraso. Para obter mais informações, consulte [atrasar-carregar tabelas de importação (somente imagem)](#delay-load-import-tables-image-only).<br/>                    |
| 208/224 <br/> | 8 <br/> | Cabeçalho de tempo de execução CLR <br/>      | O tamanho e o endereço do cabeçalho do tempo de execução CLR. Para obter mais informações, consulte [a seção. cormeta (somente objeto)](#the-cormeta-section-object-only).<br/>                                |
| 216/232 <br/> | 8 <br/> | Reservado, deve ser zero <br/>  |                                                                                                                                                                                      |

A entrada da tabela de certificado aponta para uma tabela de certificados de atributo. Esses certificados não são carregados na memória como parte da imagem. Como tal, o primeiro campo dessa entrada, que normalmente é um RVA, é um ponteiro de arquivo em vez disso.

## <a name="section-table-section-headers"></a>Tabela de seções (cabeçalhos de seção)

- [Sinalizadores de seção](#section-flags)
- [Seções agrupadas (somente objeto)](#grouped-sections-object-only)

Cada linha da tabela da seção é, na verdade, um cabeçalho de seção. Essa tabela imediatamente segue o cabeçalho opcional, se houver. Esse posicionamento é necessário porque o cabeçalho do arquivo não contém um ponteiro direto para a tabela da seção. Em vez disso, o local da tabela da seção é determinado pelo cálculo do local do primeiro byte após os cabeçalhos. Certifique-se de usar o tamanho do cabeçalho opcional, conforme especificado no cabeçalho do arquivo.

O número de entradas na tabela da seção é fornecido pelo campo NumberOfSections no cabeçalho do arquivo. As entradas na tabela da seção são numeradas a partir de um (1). As entradas da seção código e memória de dados estão na ordem escolhida pelo vinculador.

Em um arquivo de imagem, o VAs para seções deve ser atribuído pelo vinculador para que ele esteja em ordem crescente e adjacente, e deve ser um múltiplo do valor de SectionAlignment no cabeçalho opcional.

Cada cabeçalho de seção (entrada de tabela de seção) tem o seguinte formato, para um total de 40 bytes por entrada.



| Deslocamento         | Tamanho          | Campo                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nome <br/>                 | Uma cadeia de caracteres codificada em UTF-8 de 8 bytes. Se a cadeia de caracteres tiver exatamente 8 caracteres, não haverá nenhum nulo de término. Para nomes mais longos, esse campo contém uma barra (/) que é seguida por uma representação ASCII de um número decimal que é um deslocamento na tabela de cadeia de caracteres. As imagens executáveis não usam uma tabela de cadeia de caracteres e não dão suporte a nomes de seção com mais de 8 caracteres. Nomes longos em arquivos de objeto são truncados se forem emitidos para um arquivo executável. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | O tamanho total da seção quando carregado na memória. Se esse valor for maior que SizeOfRawData, a seção será preenchida com zero. Esse campo é válido somente para imagens executáveis e deve ser definido como zero para arquivos de objeto. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | Para imagens executáveis, o endereço do primeiro byte da seção em relação à base da imagem quando a seção é carregada na memória. Para arquivos de objeto, esse campo é o endereço do primeiro byte antes que a relocação seja aplicada; para simplificar, os compiladores devem definir isso como zero. Caso contrário, é um valor arbitrário que é subtraído dos deslocamentos durante a realocação. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | O tamanho da seção (para arquivos de objeto) ou o tamanho dos dados inicializados em disco (para arquivos de imagem). Para imagens executáveis, isso deve ser um múltiplo de FileAlignment do cabeçalho opcional. Se isso for menor que VirtualSize, o restante da seção será preenchido com zero. Como o campo SizeOfRawData é arredondado, mas o campo VirtualSize não é, é possível que SizeOfRawData seja maior que VirtualSize também. Quando uma seção contém apenas dados não inicializados, esse campo deve ser zero. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | O ponteiro de arquivo para a primeira página da seção dentro do arquivo COFF. Para imagens executáveis, isso deve ser um múltiplo de FileAlignment do cabeçalho opcional. Para arquivos de objeto, o valor deve ser alinhado em um limite de 4 bytes para obter o melhor desempenho. Quando uma seção contém apenas dados não inicializados, esse campo deve ser zero. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | O ponteiro do arquivo para o início das entradas de realocação da seção. Isso é definido como zero para imagens executáveis ou se não houver realocações. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | O ponteiro do arquivo para o início das entradas de número de linha para a seção. Isso será definido como zero se não houver números de linha COFF. Esse valor deve ser zero para uma imagem porque as informações de depuração COFF foram preteridas. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | O número de entradas de realocação para a seção. Isso é definido como zero para imagens executáveis. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | O número de entradas de número de linha para a seção. Esse valor deve ser zero para uma imagem porque as informações de depuração COFF foram preteridas. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Características <br/>      | Os sinalizadores que descrevem as características da seção. Para obter mais informações, consulte [sinalizadores de seção](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Sinalizadores de seção

Os sinalizadores de seção no campo características do cabeçalho da seção indicam as características da seção.



| Sinalizador                                              | Valor                  | Descrição                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| tipo de SCN de imagem \_ \_ \_ sem \_ teclado <br/>             | 0x00000008 <br/> | A seção não deve ser preenchida para o próximo limite. Esse sinalizador é obsoleto e é substituído por IMAGE \_ SCN \_ align \_ 1BYTES. Isso é válido somente para arquivos de objeto. <br/> |
|                                                   | 0x00000010 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| \_ \_ código CNT de SCN de imagem \_ <br/>                 | 0x00000020 <br/> | A seção contém código executável. <br/>                                                                                                                           |
| \_ \_ \_ dados inicializados CNT do Image SCN \_ <br/>    | 0x00000040 <br/> | A seção contém dados inicializados. <br/>                                                                                                                          |
| \_dados não \_ \_ inicializados do Image SCN CNT \_ <br/> | 0x00000080 <br/> | A seção contém dados não inicializados. <br/>                                                                                                                        |
| IMAGE \_ SCN \_ lnk \_ Other <br/>                | 0x00000100 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| informações do IMAGE \_ SCN \_ lnk \_ <br/>                 | 0x00000200 <br/> | A seção contém comentários ou outras informações. A seção. drectve tem esse tipo. Isso é válido somente para arquivos de objeto. <br/>                                    |
|                                                   | 0x00000400 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| remoção de IMAGE \_ SCN \_ lnk \_ Remove <br/>               | 0x00000800 <br/> | A seção não se tornará parte da imagem. Isso é válido somente para arquivos de objeto. <br/>                                                                             |
| IMAGE \_ SCN \_ lnk \_ COMDAT <br/>               | 0x00001000 <br/> | A seção contém dados COMDAT. Para obter mais informações, consulte [seções COMDAT (somente objeto)](#comdat-sections-object-only). Isso é válido somente para arquivos de objeto. <br/> |
| \_GPREL de SCN de imagem \_ <br/>                     | 0x00008000 <br/> | A seção contém dados referenciados por meio do ponteiro global (GP). <br/>                                                                                           |
| IMAGE \_ SCN \_ mem \_ limpável <br/>            | 0x00020000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ mem \_ 16 bits <br/>                | 0x00020000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ mem \_ bloqueado <br/>               | 0x00040000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| \_pré-carregamento de \_ Mem de SCN de imagem \_ <br/>              | 0x00080000 <br/> | Reservado para uso futuro. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ alinhar \_ 1BYTES <br/>             | 0x00100000 <br/> | Alinhar dados em um limite de 1 byte. Válido somente para arquivos de objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ alinhar \_ 2BYTES <br/>             | 0x00200000 <br/> | Alinhar dados em um limite de 2 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ alinhar \_ 4BYTES <br/>             | 0x00300000 <br/> | Alinhar dados em um limite de 4 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                   |
| IMAGE \_ SCN \_ alinhar \_ 8BYTES <br/>             | 0x00400000 <br/> | Alinhar dados em um limite de 8 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ alinhar \_ 16BYTES <br/>            | 0x00500000 <br/> | Alinhar dados em um limite de 16 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ alinhar \_ 32BYTES <br/>            | 0x00600000 <br/> | Alinhar dados em um limite de 32 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ alinhar \_ 64BYTES <br/>            | 0x00700000 <br/> | Alinhar dados em um limite de 64 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                  |
| IMAGE \_ SCN \_ alinhar \_ 128BYTES <br/>           | 0x00800000 <br/> | Alinhar dados em um limite de 128 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ alinhar \_ 256BYTES <br/>           | 0x00900000 <br/> | Alinhar dados em um limite de 256 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ alinhar \_ 512BYTES <br/>           | 0x00A00000 <br/> | Alinhar dados em um limite de 512 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                 |
| IMAGE \_ SCN \_ alinhar \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Alinhar dados em um limite de 1024 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ alinhar \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Alinhar dados em um limite de 2048 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ alinhar \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Alinhar dados em um limite de 4096 bytes. Válido somente para arquivos de objeto. <br/>                                                                                                |
| IMAGE \_ SCN \_ alinhar \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Alinhar dados em um limite de 8192 bytes. Válido somente para arquivos de objeto. <br/>                                                                                               |
| IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | A seção contém realocações estendidas. <br/>                                                                                                                      |
| IMAGE \_ SCN \_ mem \_ Descartado <br/>          | 0x02000000 <br/> | A seção pode ser descartada conforme necessário. <br/>                                                                                                                         |
| IMAGE \_ SCN \_ mem \_ não \_ armazenada em cache <br/>          | 0x04000000 <br/> | A seção não pode ser armazenada em cache. <br/>                                                                                                                                   |
| IMAGE \_ SCN \_ mem \_ não \_ paginável <br/>           | 0x08000000 <br/> | A seção não é paginável. <br/>                                                                                                                                    |
| IMAGE \_ SCN \_ mem \_ compartilhado <br/>               | 0x10000000 <br/> | A seção pode ser compartilhada na memória. <br/>                                                                                                                            |
| execução de Mem de IMAGE \_ SCN \_ \_ <br/>              | 0x20000000 <br/> | A seção pode ser executada como código. <br/>                                                                                                                            |
| leitura de Mem de IMAGE \_ SCN \_ \_ <br/>                 | 0x40000000 <br/> | A seção pode ser lida. <br/>                                                                                                                                        |
| gravação de Mem de IMAGE \_ SCN \_ \_ <br/>                | 0x80000000 <br/> | A seção pode ser gravada. <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL indica que a contagem de realocações da seção excede os 16 bits reservados para ele no cabeçalho da seção. Se o bit for definido e o campo NumberOfRelocations no cabeçalho da seção for 0xFFFF, a contagem de realocação real será armazenada no campo VirtualAddress de 32 bits da primeira relocação. Erro se a IMAGE \_ SCN \_ lnk \_ NRELOC \_ OVFL estiver definida e houver menos de realocações 0xFFFF na seção.

### <a name="grouped-sections-object-only"></a>Seções agrupadas (somente objeto)

O "$"? o caractere (cifrão) tem uma interpretação especial em nomes de seção em arquivos de objeto.

Ao determinar a seção de imagem que conterá o conteúdo de uma seção de objeto, o vinculador descarta o "$"? e todos os caracteres que o seguem. Portanto, uma seção de objeto chamada. o **texto $ X** realmente contribui para a seção **. Text** da imagem.

No entanto, os caracteres após o "$"? Determine a ordem das contribuições para a seção de imagem. Todas as contribuições com o mesmo nome de seção de objeto são alocadas de forma contígua na imagem, e os blocos de contribuições são classificados em ordem lexical por nome de seção de objeto. Portanto, tudo nos arquivos de objeto com o nome da seção **. Text $ X** acaba em conjunto, após as contribuições **. Text $ W** e antes das contribuições **. Text $ Y** .

O nome da seção em um arquivo de imagem nunca contém um "$"? .

## <a name="other-contents-of-the-file"></a>Outro conteúdo do arquivo

- [Dados da seção](#section-data)
- [Relocalidades COFF (somente objeto)](#coff-relocations-object-only)
  - [Indicadores de tipo](#type-indicators)
- [Números de linha COFF (preteridos)](#coff-line-numbers-deprecated)
- [Tabela de símbolos COFF](#coff-symbol-table)
  - [Representação do nome do símbolo](#symbol-name-representation)
  - [Valores de número de seção](#section-number-values)
  - [Representação de tipo](#type-representation)
  - [Classe de armazenamento](#storage-class)
- [Registros de símbolo auxiliares](#auxiliary-symbol-records)
  - [Formato auxiliar 1: definições de função](#auxiliary-format-1-function-definitions)
  - [Formato auxiliar 2:. BF e símbolos. EF](#auxiliary-format-2-bf-and-ef-symbols)
  - [Formato auxiliar 3: externamente fracas](#auxiliary-format-3-weak-externals)
  - [Formato auxiliar 4: arquivos](#auxiliary-format-4-files)
  - [Formato auxiliar 5: definições de seção](#auxiliary-format-5-section-definitions)
  - [Seções COMDAT (somente objeto)](#comdat-sections-object-only)
  - [Definição de token CLR (somente objeto)](#clr-token-definition-object-only)
- [Tabela de cadeia de caracteres COFF](#coff-string-table)
- [A tabela de certificado de atributo (somente imagem)](#the-attribute-certificate-table-image-only)
  - [Dados do certificado](#certificate-data)
- [Atrasar-carregar tabelas de importação (somente imagem)](#delay-load-import-tables-image-only)
  - [A tabela do Delay-Load Directory](#the-delay-load-directory-table)
  - [Atributos](#attributes)
  - [Nome](#name)
  - [Identificador de módulo](#module-handle)
  - [Atrasar tabela de endereços de importação](#delay-import-address-table)
  - [Atrasar tabela de nomes de importação](#delay-import-name-table)
  - [Atrasar a tabela de endereços de importação e o carimbo de data/hora](#delay-bound-import-address-table-and-time-stamp)
  - [Atrasar descarregamento da tabela de endereços de importação](#delay-unload-import-address-table)

As estruturas de dados que foram descritas até agora, até e incluindo o cabeçalho opcional, estão todas localizadas em um deslocamento fixo desde o início do arquivo (ou do cabeçalho PE se o arquivo for uma imagem que contenha um stub do MS-DOS).

O restante de um objeto ou arquivo de imagem COFF contém blocos de dados que não estão necessariamente em qualquer deslocamento de arquivo específico. Em vez disso, os locais são definidos por ponteiros no cabeçalho opcional ou em um cabeçalho de seção.

Uma exceção é para imagens com um valor de SectionAlignment menor do que o tamanho da página da arquitetura (4 K para Intel x86 e para MIPS, e 8 K para Itanium). Para obter uma descrição de SectionAlignment, consulte [cabeçalho opcional (somente imagem)](#optional-header-image-only). Nesse caso, há restrições no deslocamento do arquivo dos dados da seção, conforme descrito na seção 5,1, "dados da seção". Outra exceção é que o certificado de atributo e as informações de depuração devem ser colocados no final de um arquivo de imagem, com a tabela de certificado de atributo imediatamente anterior à seção de depuração, porque o carregador não os mapeia na memória. No entanto, a regra sobre o certificado de atributo e as informações de depuração não se aplica a arquivos de objeto.

### <a name="section-data"></a>Dados da seção

Os dados inicializados de uma seção consistem em blocos simples de bytes. No entanto, para seções que contêm todos os zeros, os dados da seção não precisam ser incluídos.

Os dados de cada seção estão localizados no deslocamento do arquivo fornecido pelo campo PointerToRawData no cabeçalho da seção. O tamanho desses dados no arquivo é indicado pelo campo SizeOfRawData. Se SizeOfRawData for menor que VirtualSize, o resto será preenchido com zeros.

Em um arquivo de imagem, os dados da seção devem ser alinhados em um limite, conforme especificado pelo campo filealign no cabeçalho opcional. Os dados da seção devem aparecer na ordem dos valores de RVA para as seções correspondentes (como os cabeçalhos de seção individuais na tabela da seção).

Há restrições adicionais nos arquivos de imagem se o valor de SectionAlignment no cabeçalho opcional for menor que o tamanho de página da arquitetura. Para esses arquivos, o local dos dados da seção no arquivo deve corresponder ao seu local na memória quando a imagem é carregada, de modo que o deslocamento físico dos dados da seção seja o mesmo que o RVA.

### <a name="coff-relocations-object-only"></a>Relocalidades COFF (somente objeto)

Os arquivos de objeto contêm realocações COFF, que especificam como os dados da seção devem ser modificados quando colocados no arquivo de imagem e, subsequentemente, carregados na memória.

Os arquivos de imagem não contêm relocalidades COFF, porque todos os símbolos referenciados já foram atribuídos a endereços em um espaço de endereço simples. Uma imagem contém informações de realocação na forma de realocações de base na seção. realocação (a menos que a imagem tenha o atributo de arquivo de imagem \_ \_ RELOCS \_ removido). Para obter mais informações, consulte [a seção. realocação (somente imagem)](#the-reloc-section-image-only).

Para cada seção em um arquivo de objeto, uma matriz de registros de comprimento fixo mantém as relocalidades COFF da seção. A posição e o comprimento da matriz são especificados no cabeçalho da seção. Cada elemento da matriz tem o formato a seguir.



| Deslocamento        | Tamanho          | Campo                        | Descrição                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | O endereço do item ao qual a realocação é aplicada. Esse é o deslocamento do início da seção, além do valor do campo RVA/offset da seção. Consulte a [tabela da seção (cabeçalhos de seção)](#section-table-section-headers). Por exemplo, se o primeiro byte da seção tiver um endereço de 0x10, o terceiro byte terá um endereço de 0x12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Um índice de base zero na tabela de símbolos. Esse símbolo fornece o endereço a ser usado para a realocação. Se o símbolo especificado tiver a classe de armazenamento de seção, o endereço do símbolo será o endereço com a primeira seção do mesmo nome. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Tipo <br/>             | Um valor que indica o tipo de realocação que deve ser executada. Os tipos de realocação válidos dependem do tipo de computador. Consulte [indicadores de tipo](#type-indicators). <br/>                                                                                                                                                                                     |



 

Se o símbolo referido pelo campo SymbolTableIndex tiver a seção classe de armazenamento de \_ classes Sym da classe Storage \_ \_ , o endereço do símbolo será o início da seção. A seção geralmente está no mesmo arquivo, exceto quando o arquivo de objeto faz parte de um arquivo morto (biblioteca). Nesse caso, a seção pode ser encontrada em qualquer outro arquivo de objeto no arquivo que tenha o mesmo nome de membro de arquivo como o arquivo de objeto atual. (A relação com o nome de membro de arquivo é usada na vinculação de tabelas de importação, ou seja, a seção. iData.)

#### <a name="type-indicators"></a>Indicadores de tipo

O campo tipo do registro de realocação indica que tipo de realocação deve ser executada. Diferentes tipos de realocação são definidos para cada tipo de computador.

##### <a name="x64-processors"></a>Processadores x64

Os seguintes indicadores de tipo de realocação são definidos para x64 e processadores compatíveis.



| Constante                                | Valor              | Descrição                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ de \_ AMD64 de rel \_ absoluta <br/> | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                        |
| \_ADDR64 de \_ AMD64 de rel de imagem \_ <br/>   | 0x0001 <br/> | O VA de 64 bits do destino de realocação. <br/>                                                                                                           |
| \_ADDR32 de \_ AMD64 de rel de imagem \_ <br/>   | 0x0002 <br/> | O VA de 32 bits do destino de realocação. <br/>                                                                                                           |
| \_ADDR32NB de \_ AMD64 de rel de imagem \_ <br/> | 0x0003 <br/> | O endereço de 32 bits sem uma base de imagem (RVA). <br/>                                                                                                   |
| \_REL32 de \_ AMD64 de rel de imagem \_ <br/>    | 0x0004 <br/> | O endereço relativo de 32 bits do byte após a realocação. <br/>                                                                               |
| IMAGE \_ rel \_ AMD64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | O endereço de 32 bits relativo à distância de byte 1 da realocação. <br/>                                                                               |
| IMAGE \_ rel \_ AMD64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | O endereço de 32 bits relativo à distância de byte 2 da realocação. <br/>                                                                               |
| IMAGE \_ rel \_ AMD64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | O endereço de 32 bits relativo à distância de byte 3 da realocação. <br/>                                                                               |
| IMAGE \_ rel \_ AMD64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | O endereço de 32 bits relativo à distância de byte 4 da realocação. <br/>                                                                               |
| IMAGE \_ rel \_ AMD64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | O endereço de 32 bits relativo à distância de byte 5 da realocação. <br/>                                                                               |
| \_ \_ Seção AMD64 de rel de imagem \_ <br/>  | 0x000A <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                  |
| \_SECREL de \_ AMD64 de rel de imagem \_ <br/>   | 0x000B <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/> |
| \_SECREL7 de \_ AMD64 de rel de imagem \_ <br/>  | 0x000C <br/> | Um deslocamento não assinado de 7 bits da base da seção que contém o destino. <br/>                                                                    |
| \_ \_ Token AMD64 de rel de imagem \_ <br/>    | 0x000D <br/> | Tokens CLR. <br/>                                                                                                                                       |
| \_SREL32 de \_ AMD64 de rel de imagem \_ <br/>   | 0x000E <br/> | Um valor dependente de span com sinal de 32 bits emitido para o objeto. <br/>                                                                                     |
| Par imagem de \_ AMD64 de rel \_ \_ <br/>     | 0x000F <br/> | Um par que deve seguir imediatamente cada valor dependente de span. <br/>                                                                                   |
| \_SSPAN32 de \_ AMD64 de rel de imagem \_ <br/>  | 0x0010 <br/> | Um valor dependente de span com sinal de 32 bits que é aplicado no momento do link. <br/>                                                                                |



 

##### <a name="arm-processors"></a>Processadores ARM

Os seguintes indicadores de tipo de realocação são definidos para processadores ARM.



| Constante                                | Valor              | Descrição                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ do \_ ARM de rel \_ absoluto <br/>   | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                                                                                                                                 |
| \_ADDR32 do \_ ARM de rel de imagem \_ <br/>     | 0x0001 <br/> | O VA de 32 bits do destino. <br/>                                                                                                                                                                                                                               |
| \_ADDR32NB do \_ ARM de rel de imagem \_ <br/>   | 0x0002 <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                                                                                                                              |
| \_BRANCH24 do \_ ARM de rel de imagem \_ <br/>   | 0x0003 <br/> | O deslocamento relativo de 24 bits para o destino. <br/>                                                                                                                                                                                                            |
| \_BRANCH11 do \_ ARM de rel de imagem \_ <br/>   | 0x0004 <br/> | A referência a uma chamada de sub-rotina. A referência consiste em instruções de 2 16 bits com deslocamentos de 11 bits. <br/>                                                                                                                                                 |
| \_REL32 do \_ ARM de rel de imagem \_ <br/>      | 0x000A <br/> | O endereço relativo de 32 bits do byte após a realocação. <br/>                                                                                                                                                                                        |
| \_ \_ seção ARM de rel de imagem \_ <br/>    | 0x000E <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                                                                                                                           |
| \_SECREL do \_ ARM de rel de imagem \_ <br/>     | 0x000F <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/>                                                                                                          |
| \_MOV32 do \_ ARM de rel de imagem \_ <br/>      | 0x0010 <br/> | O VA de 32 bits do destino. Essa realocação é aplicada usando uma instrução MOVW para os 16 bits baixos seguidos por um MOVT para os 16 bits superiores. <br/>                                                                                                              |
| IMAGEM \_ \_ MOV32 do Thumb rel \_ <br/>    | 0x0011 <br/> | O VA de 32 bits do destino. Essa realocação é aplicada usando uma instrução MOVW para os 16 bits baixos seguidos por um MOVT para os 16 bits superiores. <br/>                                                                                                              |
| IMAGEM \_ \_ BRANCH20 do Thumb rel \_ <br/> | 0x0012 <br/> | A instrução é corrigida com o deslocamento relativo de 21 bits para o destino alinhado de 2 bytes. O bit menos significativo da substituição é sempre zero e não é armazenado. Essa relocação corresponde a uma instrução B condicional de Thumb de 2 32 bits. <br/> |
| Não usado <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMAGEM \_ \_ BRANCH24 do Thumb rel \_ <br/> | 0x0014 <br/> | A instrução é corrigida com o deslocamento relativo de 25 bits para o destino alinhado de 2 bytes. O bit menos significativo do deslocamento é zero e não é armazenado. Essa relocação corresponde a uma instrução Thumb-2 B. <br/>                            |
| IMAGEM \_ \_ BLX23 do Thumb rel \_ <br/>    | 0x0015 <br/> | A instrução é corrigida com o deslocamento relativo de 25 bits para o destino alinhado de 4 bytes. Os dois bits baixos da substituição são zero e não são armazenados. <br/> Essa relocação corresponde a uma instrução BLX Thumb-2. <br/>                      |
| \_par de \_ ARM de rel de imagem \_ <br/>       | 0x0016 <br/> | A realocação é válida somente quando segue imediatamente um REFHI de ARM \_ ou \_ REFHI Thumb. Seu SymbolTableIndex contém uma substituição e não um índice na tabela de símbolos. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>Processadores ARM64

Os seguintes indicadores de tipo de realocação são definidos para processadores ARM64.



| Constante                                       | Valor              | Descrição                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ ARM64 de rel \_ \_ absoluta <br/>        | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                        |
| \_ARM64 rel \_ \_ ADDR32 da imagem <br/>          | 0x0001 <br/> | O VA de 32 bits do destino. <br/>                                                                                                                      |
| \_ARM64 rel \_ \_ ADDR32NB da imagem <br/>        | 0x0002 <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                     |
| \_ARM64 rel \_ \_ BRANCH26 da imagem <br/>        | 0x0003 <br/> | O deslocamento relativo de 26 bits para o destino, para as instruções B e BL. <br/>                                                                        |
| IMAGE \_ rel \_ ARM64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | A base da página do destino, para instrução ADRP. <br/>                                                                                                |
| \_ARM64 rel \_ \_ REL21 da imagem <br/>           | 0x0005 <br/> | O deslocamento relativo de 12 bits para o destino, para instrução ADR <br/>                                                                               |
| IMAGE \_ rel \_ ARM64 \_ PAGEOFFSET \_ 12A <br/> | 0x0006 <br/> | O deslocamento de página de 12 bits do destino para instruções adiciona/adiciona (immediate) com Shift zero. <br/>                                                      |
| IMAGE \_ rel \_ ARM64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | O deslocamento de página de 12 bits do destino, para a instrução LDR (indexada e não assinada imediatamente). <br/>                                                          |
| \_ARM64 rel \_ \_ SECREL da imagem <br/>          | 0x0008 <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/> |
| IMAGE \_ rel \_ ARM64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 do deslocamento da seção do destino, para obter instruções, adicione/ADDS (imediato) com Shift zero. <br/>                                                  |
| IMAGE \_ rel \_ ARM64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 do deslocamento da seção do destino, para obter instruções, adicione/ADDS (imediato) com Shift zero. <br/>                                                 |
| IMAGE \_ rel \_ ARM64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 do deslocamento da seção do destino, para a instrução LDR (indexada e não assinada imediatamente). <br/>                                                      |
| \_ \_ Token ARM64 rel de imagem \_ <br/>           | 0x000C <br/> | Token CLR. <br/>                                                                                                                                        |
| \_ \_ Seção ARM64 rel de imagem \_ <br/>         | 0x000D <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                  |
| \_ARM64 rel \_ \_ ADDR64 da imagem <br/>          | 0x000E <br/> | O VA de 64 bits do destino de realocação. <br/>                                                                                                           |
| \_ARM64 rel \_ \_ BRANCH19 da imagem <br/>        | 0x000F <br/> | O deslocamento de 19 bits para o destino de realocação para a instrução B condicional. <br/>                                                                        |
| \_ARM64 rel \_ \_ BRANCH14 da imagem <br/>        | 0x0010 <br/> | O deslocamento de 14 bits para o destino de realocação, para obter instruções TBZ e TBNZ. <br/>                                                                        |
| \_ARM64 rel \_ \_ REL32 da imagem <br/>           | 0x0011 <br/> | O endereço relativo de 32 bits do byte após a realocação. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Processadores Hitachi SuperH

Os seguintes indicadores de tipo de realocação são definidos para processadores SH3 e SH4. As relocalidades específicas do SH5 são indicadas como SHM (SH Media).



| Constante                                      | Valor              | Descrição                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ SH3 de rel \_ \_ absoluta <br/>         | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                                                                                     |
| \_SH3 rel \_ \_ DIRECT16 da imagem <br/>         | 0x0001 <br/> | Uma referência ao local de 16 bits que contém o VA do símbolo de destino. <br/>                                                                                                                                  |
| \_SH3 rel \_ \_ DIRECT32 da imagem <br/>         | 0x0002 <br/> | O VA de 32 bits do símbolo de destino. <br/>                                                                                                                                                                            |
| \_SH3 rel \_ \_ DIRECT8 da imagem <br/>          | 0x0003 <br/> | Uma referência ao local de 8 bits que contém o VA do símbolo de destino. <br/>                                                                                                                                   |
| \_Word rel \_ SH3 \_ DIRECT8 \_ <br/>    | 0x0004 <br/> | Uma referência à instrução de 8 bits que contém o VA de 16 bits efetivo do símbolo de destino. <br/>                                                                                                               |
| IMAGE \_ rel \_ SH3 \_ DIRECT8 \_ Long <br/>    | 0x0005 <br/> | Uma referência à instrução de 8 bits que contém o VA de 32 bits efetivo do símbolo de destino. <br/>                                                                                                               |
| \_SH3 rel \_ \_ DIRECT4 da imagem <br/>          | 0x0006 <br/> | Uma referência ao local de 8 bits cujos poucos bits baixos contêm o VA do símbolo de destino. <br/>                                                                                                                        |
| \_Word rel \_ SH3 \_ DIRECT4 \_ <br/>    | 0x0007 <br/> | Uma referência à instrução de 8 bits cujos poucos bits baixos contêm o VA de 16 bits efetivo do símbolo de destino. <br/>                                                                                                    |
| IMAGE \_ rel \_ SH3 \_ DIRECT4 \_ Long <br/>    | 0x0008 <br/> | Uma referência à instrução de 8 bits cujos poucos bits baixos contêm a VA de 32 bits do símbolo de destino. <br/>                                                                                                    |
| \_Word rel \_ SH3 \_ PCREL8 \_ <br/>     | 0x0009 <br/> | Uma referência à instrução de 8 bits que contém o deslocamento relativo de 16 bits efetivo do símbolo de destino. <br/>                                                                                                  |
| IMAGE \_ rel \_ SH3 \_ PCREL8 \_ Long <br/>     | 0x000A <br/> | Uma referência à instrução de 8 bits que contém o deslocamento relativo de 32 bits efetivo do símbolo de destino. <br/>                                                                                                  |
| \_Word rel \_ SH3 \_ PCREL12 \_ <br/>    | 0x000B <br/> | Uma referência à instrução de 16 bits cujos poucos 12 bits contêm o deslocamento relativo de 16 bits efetivo do símbolo de destino. <br/>                                                                                     |
| \_Seção Image rel \_ SH3 \_ STARTOF \_ <br/> | 0x000C <br/> | Uma referência a um local de 32 bits que é o VA da seção que contém o símbolo de destino. <br/>                                                                                                                |
| \_Seção imagem rel \_ SH3 \_ sizeof \_ <br/>  | 0x000D <br/> | Uma referência ao local de 32 bits que é o tamanho da seção que contém o símbolo de destino. <br/>                                                                                                            |
| \_ \_ Seção SH3 rel de imagem \_ <br/>          | 0x000E <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                                                                               |
| \_SH3 rel \_ \_ SECREL da imagem <br/>           | 0x000F <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/>                                                              |
| IMAGEM \_ rel \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | O RVA de 32 bits do símbolo de destino. <br/>                                                                                                                                                                           |
| IMAGE \_ rel \_ SH3 \_ GPREL4 \_ Long <br/>     | 0x0011 <br/> | GP relativo. <br/>                                                                                                                                                                                                   |
| \_ \_ Token SH3 rel de imagem \_ <br/>            | 0x0012 <br/> | Token CLR. <br/>                                                                                                                                                                                                     |
| \_SHM rel \_ \_ PCRELPT da imagem <br/>          | 0x0013 <br/> | O deslocamento da instrução atual no longwords. Se o bit nomode não estiver definido, insira o inverso do bit inferior no bit 32 para selecionar PTA ou PTB. <br/>                                                          |
| \_SHM rel \_ \_ REFLO da imagem <br/>            | 0x0014 <br/> | Os 16 bits baixos do endereço de 32 bits. <br/>                                                                                                                                                                         |
| \_SHM rel \_ \_ REFHALF da imagem <br/>          | 0x0015 <br/> | Os 16 bits altos do endereço de 32 bits. <br/>                                                                                                                                                                        |
| \_SHM rel \_ \_ RELLO da imagem <br/>            | 0x0016 <br/> | Os 16 bits baixos do endereço relativo. <br/>                                                                                                                                                                       |
| \_SHM rel \_ \_ RELHALF da imagem <br/>          | 0x0017 <br/> | Os 16 bits altos do endereço relativo. <br/>                                                                                                                                                                      |
| \_par Image rel \_ SHM \_ <br/>             | 0x0018 <br/> | A realocação é válida somente quando segue imediatamente uma realocação REFHALF, RELHALF ou RELLO. O campo SymbolTableIndex da realocação contém uma substituição e não um índice na tabela de símbolos. <br/> |
| IMAGEM \_ de \_ SHM rel do Image \_ <br/>           | 0x8000 <br/> | A realocação ignora o modo de seção. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>Processadores IBM PowerPC

Os seguintes indicadores de tipo de realocação são definidos para processadores PowerPC.



| Constante                              | Valor              | Descrição                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ de \_ PPC de rel \_ absoluta <br/> | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                                                                                                                                                                                                                                              |
| \_ADDR64 de \_ PPC de rel de imagem \_ <br/>   | 0x0001 <br/> | O VA de 64 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                            |
| \_ADDR32 de \_ PPC de rel de imagem \_ <br/>   | 0x0002 <br/> | O VA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                            |
| \_ADDR24 de \_ PPC de rel de imagem \_ <br/>   | 0x0003 <br/> | Os 24 bits baixos do VA do destino. Isso é válido somente quando o símbolo de destino é absoluto e pode ser estendido para seu valor original. <br/>                                                                                                                                                                                                                          |
| \_ADDR16 de \_ PPC de rel de imagem \_ <br/>   | 0x0004 <br/> | Os 16 bits baixos do VA do destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| \_ADDR14 de \_ PPC de rel de imagem \_ <br/>   | 0x0005 <br/> | Os 14 bits baixos do VA do destino. Isso é válido somente quando o símbolo de destino é absoluto e pode ser estendido para seu valor original. <br/>                                                                                                                                                                                                                               |
| \_REL24 de \_ PPC de rel de imagem \_ <br/>    | 0x0006 <br/> | Um deslocamento relativo a um PC de 24 bits para o local do símbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| \_REL14 de \_ PPC de rel de imagem \_ <br/>    | 0x0007 <br/> | Um deslocamento relativo a um PC de 14 bits para o local do símbolo. <br/>                                                                                                                                                                                                                                                                                                                   |
| \_ADDR32NB de \_ PPC de rel de imagem \_ <br/> | 0x000A <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                           |
| \_SECREL de \_ PPC de rel de imagem \_ <br/>   | 0x000B <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/>                                                                                                                                                                                                                       |
| \_ \_ seção PPC de rel de imagem \_ <br/>  | 0x000C <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                                                                                                                                                                                                                                        |
| \_SECREL16 de \_ PPC de rel de imagem \_ <br/> | 0x000F <br/> | O deslocamento de 16 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/>                                                                                                                                                                                                                       |
| \_REFHI de \_ PPC de rel de imagem \_ <br/>    | 0x0010 <br/> | Os altos 16 bits do VA de 32 bits de destino. Isso é usado para a primeira instrução em uma sequência de duas instruções que carrega um endereço completo. Essa realocação deve ser imediatamente seguida por uma realocação de par cujo SymbolTableIndex contém um deslocamento de 16 bits assinado que é adicionado aos 16 bits superiores que foi obtido do local que está sendo realocado. <br/> |
| \_REFLO de \_ PPC de rel de imagem \_ <br/>    | 0x0011 <br/> | Os 16 bits baixos do VA do destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| \_par de \_ PPC de rel de imagem \_ <br/>     | 0x0012 <br/> | Uma realocação válida somente quando segue imediatamente uma relocação de REFHI ou SECRELHI. Seu SymbolTableIndex contém uma substituição e não um índice na tabela de símbolos. <br/>                                                                                                                                                                                        |
| \_SECRELLO de \_ PPC de rel de imagem \_ <br/> | 0x0013 <br/> | Os 16 bits baixos do deslocamento de 32 bits do destino desde o início de sua seção. <br/>                                                                                                                                                                                                                                                                                   |
| \_GPREL de \_ PPC de rel de imagem \_ <br/>    | 0x0015 <br/> | O deslocamento assinado de 16 bits do destino relativo ao registro de GP. <br/>                                                                                                                                                                                                                                                                                               |
| \_token de \_ PPC de rel de imagem \_ <br/>    | 0x0016 <br/> | O token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Processadores Intel 386

Os seguintes indicadores de tipo de realocação são definidos para processadores Intel 386 e compatíveis.



| Constante                               | Valor              | Descrição                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ de \_ pasta de rel \_ absoluta <br/> | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                        |
| \_DIR16 de \_ pasta de rel de imagem \_ <br/>    | 0x0001 <br/> | Não há suporte. <br/>                                                                                                                                    |
| \_REL16 de \_ pasta de rel de imagem \_ <br/>    | 0x0002 <br/> | Não há suporte. <br/>                                                                                                                                    |
| \_DIR32 de \_ pasta de rel de imagem \_ <br/>    | 0x0006 <br/> | O VA de 32 bits do destino. <br/>                                                                                                                           |
| \_DIR32NB de \_ pasta de rel de imagem \_ <br/>  | 0x0007 <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                          |
| \_SEG12 de \_ pasta de rel de imagem \_ <br/>    | 0x0009 <br/> | Não há suporte. <br/>                                                                                                                                    |
| \_ \_ Seção i386 da imagem de rel \_ <br/>  | 0x000A <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                  |
| \_SECREL de \_ pasta de rel de imagem \_ <br/>   | 0x000B <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/> |
| \_ \_ Token i386 de rel de imagem \_ <br/>    | 0x000C <br/> | O token CLR. <br/>                                                                                                                                    |
| \_SECREL7 de \_ pasta de rel de imagem \_ <br/>  | 0x000D <br/> | Um deslocamento de 7 bits da base da seção que contém o destino. <br/>                                                                             |
| \_REL32 de \_ pasta de rel de imagem \_ <br/>    | 0x0014 <br/> | O deslocamento relativo de 32 bits para o destino. Isso dá suporte à ramificação relativa do x86 e a instruções de chamada. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Intel Itanium Processor Family (IPF)

Os seguintes indicadores de tipo de realocação são definidos para a família de processadores Intel Itanium e processadores compatíveis. Observe que as realocações em instruções usam o deslocamento do grupo e o número do slot para o deslocamento de realocação.



| Constante                                 | Valor              | Descrição                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ do \_ IA64 de rel \_ absoluto <br/>   | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                                                                                                                                                                                                          |
| \_IMM14 rel \_ IA64 de imagem \_ <br/>      | 0x0001 <br/> | A realocação de instrução pode ser seguida por uma realocação de adendo cujo valor é adicionado ao endereço de destino antes de ser inserido no slot especificado no pacote IMM14. O destino de realocação deve ser absoluto ou a imagem deve ser corrigida. <br/>                                                                                 |
| \_IMM22 rel \_ IA64 de imagem \_ <br/>      | 0x0002 <br/> | A realocação de instrução pode ser seguida por uma realocação de adendo cujo valor é adicionado ao endereço de destino antes de ser inserido no slot especificado no pacote IMM22. O destino de realocação deve ser absoluto ou a imagem deve ser corrigida. <br/>                                                                                 |
| \_IMM64 rel \_ IA64 de imagem \_ <br/>      | 0x0003 <br/> | O número de slot dessa relocação deve ser um (1). A realocação pode ser seguida por uma realocação de adendo cujo valor é adicionado ao endereço de destino antes de ser armazenado em todos os três slots do pacote IMM64. <br/>                                                                                                                   |
| \_DIR32 rel \_ IA64 de imagem \_ <br/>      | 0x0004 <br/> | O VA de 32 bits do destino. Isso só tem suporte para/LARGEADDRESSAWARE: nenhuma imagem. <br/>                                                                                                                                                                                                                                                    |
| \_DIR64 rel \_ IA64 de imagem \_ <br/>      | 0x0005 <br/> | O VA de 64 bits do destino. <br/>                                                                                                                                                                                                                                                                                                             |
| \_PCREL21B rel \_ IA64 de imagem \_ <br/>   | 0x0006 <br/> | A instrução é corrigida com o deslocamento relativo de 25 bits para o destino alinhado de 16 bits. Os 4 bits baixos da substituição são zero e não são armazenados. <br/>                                                                                                                                                                     |
| \_PCREL21M rel \_ IA64 de imagem \_ <br/>   | 0x0007 <br/> | A instrução é corrigida com o deslocamento relativo de 25 bits para o destino alinhado de 16 bits. Os 4 bits baixos da substituição, que são zero, não são armazenados. <br/>                                                                                                                                                                 |
| \_PCREL21F rel \_ IA64 de imagem \_ <br/>   | 0x0008 <br/> | O LSBs deste deslocamento de realocação deve conter o número do slot, enquanto o restante é o endereço do pacote. O pacote é corrigido com o deslocamento relativo de 25 bits para o destino alinhado de 16 bits. Os 4 bits baixos da substituição são zero e não são armazenados. <br/>                                                                |
| \_GPREL22 rel \_ IA64 de imagem \_ <br/>    | 0x0009 <br/> | A realocação de instrução pode ser seguida por uma realocação de adendo cujo valor é adicionado ao endereço de destino e, em seguida, um deslocamento relativo a GP de 22 bits que é calculado e aplicado ao pacote GPREL22. <br/>                                                                                                                            |
| \_LTOFF22 rel \_ IA64 de imagem \_ <br/>    | 0x000A <br/> | A instrução é corrigida com o deslocamento relativo a GP de 22 bits para a entrada da tabela literal do símbolo de destino. O vinculador cria essa entrada de tabela literal com base nessa relocação e na realocação de adendo que pode seguir. <br/>                                                                                                        |
| \_ \_ Seção IA64 da imagem de rel \_ <br/>    | 0x000B <br/> | O índice da seção de 16 bits da seção contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                                                                                                                                                                                                         |
| \_SECREL22 rel \_ IA64 de imagem \_ <br/>   | 0x000C <br/> | A instrução é corrigida com o deslocamento de 22 bits do destino desde o início de sua seção. Essa relocação pode ser seguida imediatamente por uma relocação de adendo, cujo campo de valor contém o deslocamento não assinado de 32 bits do destino desde o início da seção. <br/>                                                     |
| \_SECREL64I rel \_ IA64 de imagem \_ <br/>  | 0x000D <br/> | O número de slot para essa realocação deve ser um (1). A instrução é corrigida com o deslocamento de 64 bits do destino desde o início de sua seção. Essa relocação pode ser seguida imediatamente por uma realocação de adendo cujo campo de valor contenha o deslocamento não assinado de 32 bits do destino desde o início da seção. <br/> |
| \_SECREL32 rel \_ IA64 de imagem \_ <br/>   | 0x000E <br/> | O endereço dos dados a serem corrigidos com o deslocamento de 32 bits do destino desde o início de sua seção. <br/>                                                                                                                                                                                                                          |
| \_DIR32NB rel \_ IA64 de imagem \_ <br/>    | 0x0010 <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                            |
| \_SREL14 rel \_ IA64 de imagem \_ <br/>     | 0x0011 <br/> | Isso é aplicado a um imediato de 14 bits assinado que contém a diferença entre dois destinos relocáveis. Este é um campo declarativo para o vinculador que indica que o compilador já emitiu esse valor. <br/>                                                                                                              |
| \_SREL22 rel \_ IA64 de imagem \_ <br/>     | 0x0012 <br/> | Isso é aplicado a um imediato de 22 bits assinado que contém a diferença entre dois destinos relocáveis. Este é um campo declarativo para o vinculador que indica que o compilador já emitiu esse valor. <br/>                                                                                                              |
| \_SREL32 rel \_ IA64 de imagem \_ <br/>     | 0x0013 <br/> | Isso é aplicado a um imediato de 32 bits assinado que contém a diferença entre dois valores relocáveis. Este é um campo declarativo para o vinculador que indica que o compilador já emitiu esse valor. <br/>                                                                                                               |
| \_UREL32 rel \_ IA64 de imagem \_ <br/>     | 0x0014 <br/> | Isso é aplicado a um imediato de 32 bits sem sinal que contém a diferença entre dois valores relocáveis. Este é um campo declarativo para o vinculador que indica que o compilador já emitiu esse valor. <br/>                                                                                                            |
| \_PCREL60X rel \_ IA64 de imagem \_ <br/>   | 0x0015 <br/> | Uma correção relativa a um PC de 60 bits que sempre permanece como uma instrução de BRL de um pacote MLX. <br/>                                                                                                                                                                                                                                                 |
| \_PCREL60B rel \_ IA64 de imagem \_ <br/>   | 0x0016 <br/> | Uma correção relativa a um PC de 60 bits. Se o deslocamento de destino couber em um campo de 25 bits assinado, converta todo o pacote em um pacote MBB com NOP. B no slot 1 e uma instrução BR de 25 bits (com os 4 bits mais baixos todos os zero e descartados) no slot 2. <br/>                                                                                          |
| \_PCREL60F rel \_ IA64 de imagem \_ <br/>   | 0x0017 <br/> | Uma correção relativa a um PC de 60 bits. Se o deslocamento de destino couber em um campo de 25 bits assinado, converta todo o pacote em um pacote MFB com NOP. F no slot 1 e uma instrução de 25 bits (4 bits mais baixos todos os zero e ignorados) BR no slot 2. <br/>                                                                                                   |
| \_PCREL60I rel \_ IA64 de imagem \_ <br/>   | 0x0018 <br/> | Uma correção relativa a um PC de 60 bits. Se o deslocamento de destino couber em um campo de 25 bits assinado, converta todo o pacote em um pacote de MIB com NOP. No slot 1 e uma instrução de 25 bits (4 bits mais baixos todos os zero e ignorados) BR no slot 2. <br/>                                                                                                   |
| \_PCREL60M rel \_ IA64 de imagem \_ <br/>   | 0x0019 <br/> | Uma correção relativa a um PC de 60 bits. Se o deslocamento de destino couber em um campo de 25 bits assinado, converta todo o pacote em um pacote MMB com NOP. M no slot 1 e uma instrução de 25 bits (4 bits mais baixos todos os zero e removido) BR no slot 2. <br/>                                                                                                   |
| \_IMMGPREL64 rel \_ IA64 de imagem \_ <br/> | 0x001a <br/> | Uma correção de GP relativa de 64 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| \_ \_ Token IA64 de rel de imagem \_ <br/>      | 0x001b <br/> | Um token CLR. <br/>                                                                                                                                                                                                                                                                                                                        |
| \_GPREL32 rel \_ IA64 de imagem \_ <br/>    | 0x001c <br/> | Uma correção de GP relativa de 32 bits. <br/>                                                                                                                                                                                                                                                                                                         |
| \_ \_ Adendo IA64 da \_ imagem <br/>     | 0x001F <br/> | A realocação é válida somente quando segue imediatamente uma das seguintes realocações: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I ou SECREL32. Seu valor contém o adendo para aplicar a instruções em um pacote, não para dados. <br/>                                                                  |



 

##### <a name="mips-processors"></a>Processadores MIPS

Os seguintes indicadores de tipo de realocação são definidos para processadores MIPS.



| Constante                                | Valor              | Descrição                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_MIPS de \_ rel \_ absoluta de imagem <br/>  | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                                                                                                                                                                                                                                              |
| \_REFHALF de \_ MIPS de rel de imagem \_ <br/>   | 0x0001 <br/> | Os altos 16 bits do VA de 32 bits de destino. <br/>                                                                                                                                                                                                                                                                                                                             |
| \_REFWORD de \_ MIPS de rel de imagem \_ <br/>   | 0x0002 <br/> | O VA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| \_JMPADDR de \_ MIPS de rel de imagem \_ <br/>   | 0x0003 <br/> | Os 26 bits baixos do VA do destino. Isso dá suporte às instruções MIPS J e JAL. <br/>                                                                                                                                                                                                                                                                                      |
| \_REFHI de \_ MIPS de rel de imagem \_ <br/>     | 0x0004 <br/> | Os altos 16 bits do VA de 32 bits de destino. Isso é usado para a primeira instrução em uma sequência de duas instruções que carrega um endereço completo. Essa realocação deve ser imediatamente seguida por uma realocação de par cujo SymbolTableIndex contém um deslocamento de 16 bits assinado que é adicionado aos 16 bits superiores que são obtidos do local que está sendo realocado. <br/> |
| \_REFLO de \_ MIPS de rel de imagem \_ <br/>     | 0x0005 <br/> | Os 16 bits baixos do VA do destino. <br/>                                                                                                                                                                                                                                                                                                                                     |
| \_GPREL de \_ MIPS de rel de imagem \_ <br/>     | 0x0006 <br/> | Um deslocamento assinado de 16 bits do destino relativo ao registro de GP. <br/>                                                                                                                                                                                                                                                                                                 |
| \_literal de \_ MIPS de rel de imagem \_ <br/>   | 0x0007 <br/> | O mesmo que IMAGE \_ rel \_ MIPS \_ GPREL. <br/>                                                                                                                                                                                                                                                                                                                                    |
| \_ \_ seção MIPS de rel. de imagem \_ <br/>   | 0x000A <br/> | O índice da seção de 16 bits da seção contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                                                                                                                                                                                                                                             |
| \_SECREL de \_ MIPS de rel de imagem \_ <br/>    | 0x000B <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/>                                                                                                                                                                                                                       |
| \_SECRELLO de \_ MIPS de rel de imagem \_ <br/>  | 0x000C <br/> | Os 16 bits baixos do deslocamento de 32 bits do destino desde o início de sua seção. <br/>                                                                                                                                                                                                                                                                                   |
| \_SECRELHI de \_ MIPS de rel de imagem \_ <br/>  | 0x000D <br/> | Os altos 16 bits do deslocamento de 32 bits do destino desde o início de sua seção. Uma \_ \_ relocação de par de local de MIPS de imagem \_ deve imediatamente seguir este. O SymbolTableIndex da realocação do par contém um deslocamento de 16 bits assinado que é adicionado aos 16 bits superiores que são obtidos do local que está sendo realocado. <br/>                            |
| \_JMPADDR16 de \_ MIPS de rel de imagem \_ <br/> | 0x0010 <br/> | Os 26 bits baixos do VA do destino. Isso dá suporte à instrução MIPS16 JAL. <br/>                                                                                                                                                                                                                                                                                           |
| \_REFWORDNB de \_ MIPS de rel de imagem \_ <br/> | 0x0022 <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                                |
| \_par de \_ MIPS de rel de imagens \_ <br/>      | 0x0025 <br/> | A realocação é válida somente quando segue imediatamente uma relocação de REFHI ou SECRELHI. Seu SymbolTableIndex contém uma substituição e não um índice na tabela de símbolos. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Mitsubishi M32R

Os seguintes indicadores de tipo de realocação são definidos para os processadores Mitsubishi M32R.



| Constante                               | Valor              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ M32R de rel \_ \_ absoluta <br/> | 0x0000 <br/> | A realocação é ignorada. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| \_M32R rel \_ \_ ADDR32 da imagem <br/>   | 0x0001 <br/> | O VA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| \_M32R rel \_ \_ ADDR32NB da imagem <br/> | 0x0002 <br/> | O RVA de 32 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| \_M32R rel \_ \_ ADDR24 da imagem <br/>   | 0x0003 <br/> | O VA de 24 bits do destino. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| \_M32R rel \_ \_ GPREL16 da imagem <br/>  | 0x0004 <br/> | O deslocamento de 16 bits do destino do registro de GP. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| \_M32R rel \_ \_ PCREL24 da imagem <br/>  | 0x0005 <br/> | O deslocamento de 24 bits do destino do contador do programa (PC), deslocado para a esquerda por 2 bits e a assinatura estendida <br/>                                                                                                                                                                                                                                                                                                |
| \_M32R rel \_ \_ PCREL16 da imagem <br/>  | 0x0006 <br/> | O deslocamento de 16 bits do destino do PC, deslocado para a esquerda por 2 bits e com o sinal estendido <br/>                                                                                                                                                                                                                                                                                                                  |
| \_M32R rel \_ \_ PCREL8 da imagem <br/>   | 0x0007 <br/> | O deslocamento de 8 bits do destino do PC, deslocado para a esquerda por 2 bits e com o sinal estendido <br/>                                                                                                                                                                                                                                                                                                                   |
| \_M32R rel \_ \_ REFHALF da imagem <br/>  | 0x0008 <br/> | O 16 MSBs do VA de destino. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| \_M32R rel \_ \_ REFHI da imagem <br/>    | 0x0009 <br/> | O 16 MSBs do VA de destino, ajustado para a extensão de assinatura de LSB. Isso é usado para a primeira instrução em uma sequência de duas instruções que carrega um endereço de 32 bits completo. Essa realocação deve ser imediatamente seguida por uma realocação de par cujo SymbolTableIndex contém um deslocamento de 16 bits assinado que é adicionado aos 16 bits superiores que são obtidos do local que está sendo realocado. <br/> |
| \_M32R rel \_ \_ REFLO da imagem <br/>    | 0x000A <br/> | O 16 LSBs do VA de destino. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| \_Par Image rel \_ M32R \_ <br/>     | 0x000B <br/> | A realocação deve seguir a realocação REFHI. Seu SymbolTableIndex contém uma substituição e não um índice na tabela de símbolos. <br/>                                                                                                                                                                                                                                                             |
| \_ \_ Seção M32R rel de imagem \_ <br/>  | 0x000C <br/> | O índice da seção de 16 bits da seção que contém o destino. Isso é usado para dar suporte a informações de depuração. <br/>                                                                                                                                                                                                                                                                                  |
| \_M32R rel \_ \_ SECREL da imagem <br/>   | 0x000D <br/> | O deslocamento de 32 bits do destino desde o início de sua seção. Isso é usado para dar suporte a informações de depuração e armazenamento local de thread estático. <br/>                                                                                                                                                                                                                                                 |
| \_ \_ Token M32R rel de imagem \_ <br/>    | 0x000E <br/> | O token CLR. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>Números de linha COFF (preteridos)

Os números de linha COFF não serão mais produzidos e, no futuro, não serão consumidos.

Números de linha COFF indicam a relação entre o código e os números de linha em arquivos de origem. O formato Microsoft para números de linha COFF é semelhante ao COFF padrão, mas foi estendido para permitir que uma única seção se relacione aos números de linha em vários arquivos de origem.

Números de linha COFF consistem em uma matriz de registros de comprimento fixo. O local (deslocamento de arquivo) e o tamanho da matriz são especificados no cabeçalho da seção. Cada registro de número de linha é do formato a seguir.



| Deslocamento        | Tamanho          | Campo                  | Descrição                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Tipo ( \* ) <br/>  | Esta é uma União de dois campos: SymbolTableIndex e VirtualAddress. Se SymbolTableIndex ou RVA é usado depende do valor de LineNumber. <br/> |
| 4 <br/> | 2 <br/> | LineNumber <br/> | Quando diferente de zero, esse campo especifica um número de linha baseado em um. Quando zero, o campo de tipo é interpretado como um índice de tabela de símbolos para uma função. <br/>    |



 

O campo tipo é uma União de campos de 2 4 bytes: SymbolTableIndex e VirtualAddress.



| Deslocamento        | Tamanho          | Campo                        | Descrição                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Usado quando LineNumber é zero: índice para entrada de tabela de símbolo para uma função. Esse formato é usado para indicar a função à qual um grupo de registros de número de linha se refere. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Usado quando LineNumber é diferente de zero: o RVA do código executável que corresponde à linha de origem indicada. Em um arquivo de objeto, ele contém o VA dentro da seção. <br/> |



 

Um registro de número de linha pode definir o campo LineNumber como zero e apontar para uma definição de função na tabela de símbolos ou pode funcionar como uma entrada de número de linha padrão, fornecendo um inteiro positivo (número de linha) e o endereço correspondente no código do objeto.

Um grupo de entradas de número de linha sempre começa com o primeiro formato: o índice de um símbolo de função. Se esse for o primeiro registro de número de linha na seção, ele também será o nome do símbolo COMDAT para a função se o sinalizador COMDAT da seção estiver definido. Consulte [seções COMDAT (somente objeto)](#comdat-sections-object-only). O registro auxiliar da função na tabela de símbolos tem um ponteiro para o campo LineNumber que aponta para esse mesmo registro de número de linha.

Um registro que identifica uma função é seguido por qualquer número de entradas de número de linha que forneçam informações de número de linha real (ou seja, entradas com LineNumber maior que zero). Essas entradas são baseadas em um, em relação ao início da função, e representam cada linha de origem na função, exceto a primeira linha.

Por exemplo, o primeiro registro de número de linha para o exemplo a seguir especificaria a função ReverseSign (SymbolTableIndex de ReverseSign e lineNumber definido como zero). Em seguida, os registros com valores de LineNumber de 1, 2 e 3 seguirão, correspondendo às linhas de origem, conforme mostrado:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>Tabela de símbolos COFF

A tabela de símbolos nesta seção é herdada do formato COFF tradicional. É diferente de Microsoft Visual C++ informações de depuração. Um arquivo pode conter uma tabela de símbolos COFF e Visual C++ informações de depuração, e as duas são mantidas separadas. Algumas ferramentas da Microsoft usam a tabela de símbolos para fins limitados, mas importantes, como a comunicação de informações COMDAT para o vinculador. Nomes de seção e nomes de arquivo, bem como símbolos de dados e de código, são listados na tabela de símbolos.

O local da tabela de símbolos é indicado no cabeçalho COFF.

A tabela de símbolos é uma matriz de registros, cada um com 18 bytes de comprimento. Cada registro é um registro de tabela de símbolos padrão ou auxiliar. Um registro padrão define um símbolo ou nome e tem o formato a seguir.



| Deslocamento         | Tamanho          | Campo                          | Descrição                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Nome ( \* ) <br/>          | O nome do símbolo, representado por uma União de três estruturas. Uma matriz de 8 bytes será usada se o nome não tiver mais de 8 bytes de comprimento. Para obter mais informações, consulte [símbolo de representação de nome](https://www.bing.com/search?q=Symbol+Name+Representation). <br/> |
| 8 <br/>  | 4 <br/> | Valor <br/>              | O valor que está associado ao símbolo. A interpretação desse campo depende de SectionNumber e StorageClass. Um significado típico é o endereço relocável. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | O inteiro assinado que identifica a seção, usando um índice baseado em um na tabela da seção. Alguns valores têm um significado especial, conforme definido na seção tópico 5.4.2, "valores de número de seção". <br/>                                         |
| 14 <br/> | 2 <br/> | Tipo <br/>               | Um número que representa o tipo. As ferramentas da Microsoft definem esse campo como 0x20 (Function) ou 0x0 (não uma função). Para obter mais informações, consulte [representação de tipo](#type-representation). <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Um valor enumerado que representa a classe de armazenamento. Para obter mais informações, consulte [classe de armazenamento](#storage-class). <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOfAuxSymbols <br/> | O número de entradas da tabela de símbolos auxiliares que seguem este registro. <br/>                                                                                                                                                           |



 

Zero ou mais registros de tabela de símbolos auxiliares seguem imediatamente cada registro de tabela de símbolos padrão. No entanto, normalmente não mais de um registro de tabela de símbolo auxiliar segue um registro de tabela de símbolos padrão (exceto para os registros. File com nomes de arquivo longos). Cada registro auxiliar tem o mesmo tamanho que um registro de tabela de símbolos padrão (18 bytes), mas em vez de definir um novo símbolo, o registro auxiliar fornece informações adicionais sobre o último símbolo definido. A escolha dos vários formatos a serem usados depende do campo StorageClass. Os formatos definidos atualmente para registros de tabela de símbolos auxiliares são mostrados na seção 5,5, "registros de símbolo auxiliares".

As ferramentas que lêem tabelas de símbolo COFF devem ignorar os registros de símbolo auxiliares cuja interpretação é desconhecida. Isso permite que o formato de tabela de símbolos seja estendido para adicionar novos registros auxiliares, sem interromper as ferramentas existentes.

#### <a name="symbol-name-representation"></a>Representação do nome do símbolo

O campo Curtoname em uma tabela de símbolos consiste em 8 bytes que contêm o próprio nome, se não tiver mais de 8 bytes de comprimento ou se o campo nome curto fornecer um deslocamento para a tabela de cadeia de caracteres. Para determinar se o próprio nome ou um deslocamento é fornecido, teste os 4 primeiros bytes para igualdade com zero.

Por convenção, os nomes são tratados como cadeias de caracteres codificadas UTF-8 terminadas com zero.



| Deslocamento        | Tamanho          | Campo                 | Descrição                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | ShortName <br/> | Uma matriz de 8 bytes. Essa matriz será preenchida com NULLs à direita se o nome tiver menos de 8 bytes de comprimento. <br/> |
| 0 <br/> | 4 <br/> | Zeros <br/>    | Um campo que será definido como todos os zeros se o nome tiver mais de 8 bytes. <br/>                                     |
| 4 <br/> | 4 <br/> | Deslocamento <br/>    | Um deslocamento para a tabela de cadeia de caracteres. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Valores de número de seção

Normalmente, o campo de valor de seção em uma entrada de tabela de símbolo é um índice baseado em um na tabela da seção. No entanto, esse campo é um inteiro assinado e pode receber valores negativos. Os valores a seguir, menos de um, têm significados especiais.



| Constante                          | Valor          | Descrição                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ Sym \_ indefinido <br/> | 0 <br/>  | O registro de símbolo ainda não foi atribuído a uma seção. Um valor de zero indica que uma referência a um símbolo externo está definida em outro lugar. Um valor diferente de zero é um símbolo comum com um tamanho que é especificado pelo valor. <br/> |
| IMAGEM \_ Sym \_ absoluta <br/>  | -1 <br/> | O símbolo tem um valor absoluto (não relocável) e não é um endereço. <br/>                                                                                                                                                  |
| \_depuração de Sym de imagem \_ <br/>     | -2 <br/> | O símbolo fornece informações gerais de tipo ou depuração, mas não corresponde a uma seção. As ferramentas da Microsoft usam essa configuração junto com. registros de arquivo (arquivo de classe de armazenamento). <br/>                                            |



 

#### <a name="type-representation"></a>Representação de tipo

O campo de tipo de uma entrada de tabela de símbolo contém 2 bytes, em que cada byte representa informações de tipo. O LSB representa o tipo de dados simples (base) e o MSB representa o tipo complexo, se houver:



| MSB                                                       | LSB                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Tipo complexo: nenhum, ponteiro, função, matriz. <br/> | Tipo base: inteiro, ponto flutuante e assim por diante. <br/> |



 

Os valores a seguir são definidos para o tipo base, embora as ferramentas da Microsoft geralmente não usem esse campo e defina LSB como 0. Em vez disso, Visual C++ informações de depuração são usadas para indicar tipos. No entanto, os possíveis valores COFF são listados aqui para fins de integridade.



| Constante                             | Valor          | Descrição                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| IMAGE \_ Sym \_ tipo \_ NULL <br/>   | 0 <br/>  | Nenhuma informação de tipo ou tipo base desconhecido. Ferramentas da Microsoft Use essa configuração <br/> |
| tipo de imagem \_ Sym \_ \_ void <br/>   | 1 <br/>  | Nenhum tipo válido; usado com ponteiros e funções void <br/>                       |
| \_caractere de \_ tipo \_ Sym de imagem <br/>   | 2 <br/>  | Um caractere (byte assinado) <br/>                                                  |
| tipo de imagem \_ Sym \_ \_ Short <br/>  | 3 <br/>  | Um inteiro assinado de 2 bytes <br/>                                                    |
| tipo de imagem \_ Sym \_ \_ int <br/>    | 4 <br/>  | Um tipo inteiro natural (normalmente 4 bytes no Windows) <br/>                       |
| tipo de imagem \_ Sym \_ \_ longo <br/>   | 5 <br/>  | Um inteiro com sinal de 4 bytes <br/>                                                    |
| tipo de imagem \_ Sym \_ \_ float <br/>  | 6 <br/>  | Um número de ponto flutuante de 4 bytes <br/>                                             |
| tipo de imagem \_ Sym \_ \_ duplo <br/> | 7 <br/>  | Um número de ponto flutuante de 8 bytes <br/>                                            |
| \_struct do \_ tipo \_ Sym da imagem <br/> | 8 <br/>  | Uma estrutura <br/>                                                                |
| Union de tipo de imagem \_ Sym \_ \_ <br/>  | 9 <br/>  | Uma União <br/>                                                                    |
| \_enumeração de \_ tipo \_ Sym de imagem <br/>   | 10 <br/> | Um tipo enumerado <br/>                                                         |
| tipo de imagem \_ Sym \_ \_ Moe <br/>    | 11 <br/> | Um membro da enumeração (um valor específico) <br/>                                 |
| \_byte do \_ tipo \_ Sym da imagem <br/>   | 12 <br/> | Um byte; inteiro de 1 byte não assinado <br/>                                            |
| tipo de imagem \_ Sym \_ \_ Word <br/>   | 13 <br/> | Uma palavra; inteiro de 2 bytes não assinado <br/>                                            |
| IMAGEM \_ Sym \_ tipo \_ uint <br/>   | 14 <br/> | Um inteiro sem sinal de tamanho natural (normalmente, 4 bytes) <br/>                    |
| tipo de imagem \_ Sym \_ \_ DWORD <br/>  | 15 <br/> | Um inteiro de 4 bytes não assinado <br/>                                                 |



 

O byte mais significativo especifica se o símbolo é um ponteiro para, função retornando ou matriz do tipo base que é especificado no LSB. Ferramentas da Microsoft Use este campo somente para indicar se o símbolo é uma função, de forma que apenas dois valores resultantes sejam 0x0 e 0x20 para o campo tipo. No entanto, outras ferramentas podem usar esse campo para comunicar mais informações.

É muito importante especificar o atributo da função corretamente. Essas informações são necessárias para que a vinculação incremental funcione corretamente. Para algumas arquiteturas, as informações podem ser necessárias para outras finalidades.



| Constante                                | Valor         | Descrição                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| IMAGE \_ Sym \_ DTYPE \_ NULL <br/>     | 0 <br/> | Nenhum tipo derivado; o símbolo é uma variável escalar simples. <br/> |
| \_ \_ ponteiro DTYPE de imagem Sym \_ <br/>  | 1 <br/> | O símbolo é um ponteiro para o tipo base. <br/>                    |
| \_função Sym \_ DTYPE da imagem \_ <br/> | 2 <br/> | O símbolo é uma função que retorna um tipo base. <br/>       |
| \_matriz de \_ DTYPE de Sym de imagem \_ <br/>    | 3 <br/> | O símbolo é uma matriz de tipo base. <br/>                     |



 

#### <a name="storage-class"></a>Classe de armazenamento

O campo StorageClass da tabela de símbolos indica que tipo de definição um símbolo representa. A tabela a seguir mostra os valores possíveis. Observe que o campo StorageClass é um inteiro de 1 byte não assinado. O valor especial-1 deve, portanto, ser levado para significar seu equivalente não assinado, 0xFF.

Embora o formato COFF tradicional use muitos valores de classe de armazenamento, as ferramentas da Microsoft contam com Visual C++ formato de depuração para a maioria das informações simbólicas e geralmente usam apenas quatro valores de classe de armazenamento: externo (2), estático (3), função (101) e arquivo (103). Exceto no segundo título de coluna abaixo, "value" deve ser levado para significar o campo Value do registro de símbolo (cuja interpretação depende do número encontrado como a classe de armazenamento).



| Constante                                          | Valor                 | Descrição/interpretação do campo valor                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ fim \_ da função da classe Sym da imagem \_ <br/>  | -1 (0xFF) <br/> | Um símbolo especial que representa o fim da função, para fins de depuração. <br/>                                                                                                                                                                                                                                                  |
| \_classe Sym de imagem \_ \_ nula <br/>               | 0 <br/>         | Nenhuma classe de armazenamento atribuída. <br/>                                                                                                                                                                                                                                                                                                     |
| \_classe Sym de imagem \_ \_ automática <br/>          | 1 <br/>         | A variável automática (Stack). O campo valor especifica o deslocamento do quadro da pilha. <br/>                                                                                                                                                                                                                                              |
| \_classe Sym de imagem \_ \_ externa <br/>           | 2 <br/>         | Um valor que as ferramentas da Microsoft usam para símbolos externos. O campo valor indica o tamanho se o número da seção for IMAGE \_ Sym \_ undefined (0). Se o número da seção não for zero, o campo valor especificará o deslocamento dentro da seção. <br/>                                                                                 |
| \_classe Sym de imagem \_ \_ estática <br/>             | 3 <br/>         | O deslocamento do símbolo na seção. Se o campo de valor for zero, o símbolo representará um nome de seção. <br/>                                                                                                                                                                                                            |
| \_registro da \_ classe \_ Sym da imagem <br/>           | 4 <br/>         | Uma variável de registro. O campo valor especifica o número do registro. <br/>                                                                                                                                                                                                                                                            |
| Def de classe de imagem \_ Sym \_ \_ externa \_ <br/>      | 5 <br/>         | Um símbolo que é definido externamente. <br/>                                                                                                                                                                                                                                                                                           |
| \_rótulo da \_ classe \_ Sym da imagem <br/>              | 6 <br/>         | Um rótulo de código que é definido dentro do módulo. O campo valor especifica o deslocamento do símbolo na seção. <br/>                                                                                                                                                                                                         |
| \_ \_ \_ rótulo indefinido da classe Sym da imagem \_ <br/>   | 7 <br/>         | Uma referência a um rótulo de código que não está definido. <br/>                                                                                                                                                                                                                                                                               |
| \_ \_ \_ membro da classe Sym \_ da imagem de \_ struct <br/> | 8 <br/>         | O membro da estrutura. O campo valor especifica o membro n-th. <br/>                                                                                                                                                                                                                                                               |
| \_argumento da \_ classe \_ Sym da imagem <br/>           | 9 <br/>         | Um argumento formal (parâmetro) de uma função. O campo valor especifica o n-ésimo argumento. <br/>                                                                                                                                                                                                                                      |
| \_marca de \_ struct da classe Sym \_ da imagem \_ <br/>        | 10 <br/>        | A marca de estrutura-Name entry. <br/>                                                                                                                                                                                                                                                                                                  |
| \_ \_ \_ membro da classe Sym \_ da imagem de \_ Union <br/>  | 11 <br/>        | Um membro de União. O campo valor especifica o membro n-th. <br/>                                                                                                                                                                                                                                                                     |
| \_ \_ marca Union da classe Image Sym \_ \_ <br/>         | 12 <br/>        | A entrada da tag-Name da União. <br/>                                                                                                                                                                                                                                                                                                      |
| \_definição do \_ tipo de classe Image Sym \_ \_ <br/>   | 13 <br/>        | Uma entrada de typedef. <br/>                                                                                                                                                                                                                                                                                                               |
| classe Sym de imagem não \_ \_ definida como \_ \_ estática <br/>  | 14 <br/>        | Uma declaração de dados estáticos. <br/>                                                                                                                                                                                                                                                                                                     |
| \_marca de \_ enumeração da classe Sym \_ da imagem \_ <br/>          | 15 <br/>        | Uma entrada TagName de tipo enumerado. <br/>                                                                                                                                                                                                                                                                                              |
| \_ \_ \_ membro da classe Sym \_ da imagem de \_ enum <br/>   | 16 <br/>        | Um membro de uma enumeração. O campo valor especifica o membro n-th. <br/>                                                                                                                                                                                                                                                         |
| \_parâmetro de \_ registro da classe Sym \_ da imagem \_ <br/>    | 17 <br/>        | Um parâmetro de registro. <br/>                                                                                                                                                                                                                                                                                                          |
| \_campo de \_ bits de classe Image Sym \_ \_ <br/>         | 18 <br/>        | Uma referência de campo de bits. O campo valor especifica o n-bit no campo bit. <br/>                                                                                                                                                                                                                                                |
| \_bloco de \_ classe Image Sym \_ <br/>              | 100 <br/>       | Um registro. BB (início do bloco) ou. EB (fim do bloco). O campo valor é o endereço relocável do local do código. <br/>                                                                                                                                                                                                      |
| \_função de \_ classe \_ Sym de imagem <br/>           | 101 <br/>       | Um valor que as ferramentas da Microsoft usam para registros de símbolo que definem a extensão de uma função: Begin function (. BF), End Function (. EF) e linhas na função (. LF). Para registros. LF, o campo valor fornece o número de linhas de origem na função. Para registros. EF, o campo valor fornece o tamanho do código da função. <br/> |
| \_ \_ fim da classe Image Sym \_ \_ de \_ struct <br/>    | 102 <br/>       | Uma entrada de fim de estrutura. <br/>                                                                                                                                                                                                                                                                                                     |
| \_arquivo de \_ classe \_ Sym de imagem <br/>               | 103 <br/>       | Um valor que as ferramentas da Microsoft, bem como o formato COFF tradicional, usam para o registro de símbolo de arquivo-fonte. O símbolo é seguido por registros auxiliares que nomeiem o arquivo. <br/>                                                                                                                                                       |
| \_seção da \_ classe \_ Sym da imagem <br/>            | 104 <br/>       | Uma definição de uma seção (ferramentas da Microsoft usam a classe de armazenamento estático em vez disso). <br/>                                                                                                                                                                                                                                                  |
| \_classe Sym de imagem \_ \_ fraca \_ externa <br/>     | 105 <br/>       | Um externo fraco. Para obter mais informações, consulte [formato auxiliar 3: externas fracas](#auxiliary-format-3-weak-externals). <br/>                                                                                                                                                                                                           |
| \_ \_ token CLR da classe Sym \_ da \_ imagem <br/>         | 107 <br/>       | Um símbolo de token CLR. O nome é uma cadeia de caracteres ASCII que consiste no valor hexadecimal do token. Para obter mais informações, consulte [definição de token CLR (somente objeto)](#clr-token-definition-object-only). <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Registros de símbolo auxiliares

Os registros da tabela de símbolos auxiliares sempre seguem e se aplicam a um registro de tabela de símbolos padrão. Um registro auxiliar pode ter qualquer formato que as ferramentas possam reconhecer, mas 18 bytes devem ser alocados para eles para que a tabela de símbolos seja mantida como uma matriz de tamanho regular. Atualmente, as ferramentas da Microsoft reconhecem formatos auxiliares para os seguintes tipos de registros: definições de função, símbolos de início e término de função (. BF e. EF), externos fracos, nomes de arquivo e definições de seção.

O design COFF tradicional também inclui formatos de registro auxiliar para matrizes e estruturas. As ferramentas da Microsoft não as usam, mas, em vez disso, colocam essas informações simbólicas em Visual C++ formato de depuração nas seções de depuração.

#### <a name="auxiliary-format-1-function-definitions"></a>Formato auxiliar 1: definições de função

Um registro de tabela de símbolos marca o início de uma definição de função se ela tiver todos os itens a seguir: uma classe de armazenamento de EXTERNAL (2), um valor de tipo que indica que é uma função (0x20) e um número de seção maior que zero. Observe que um registro de tabela de símbolos que tem um número de seção de indefinido (0) não define a função e não tem um registro auxiliar. Os registros de símbolo de definição de função são seguidos por um registro auxiliar no formato descrito abaixo:



| Deslocamento         | Tamanho          | Campo                             | Descrição                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | O índice de tabela de símbolos do registro de símbolo. BF (Begin Function) correspondente. <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | O tamanho do código executável para a função em si. Se a função estiver em sua própria seção, o SizeOfRawData no cabeçalho da seção será maior ou igual a esse campo, dependendo das considerações de alinhamento. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | O deslocamento do arquivo da primeira entrada de número de linha COFF para a função ou zero se não houver nenhum. Para obter mais informações, consulte [números de linha COFF (preterido)](#coff-line-numbers-deprecated). <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | O índice de tabela de símbolos do registro para a função seguinte. Se a função for a última na tabela de símbolos, esse campo será definido como zero. <br/>                                                                           |
| 16 <br/> | 2 <br/> | Não usado <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Formato auxiliar 2:. BF e símbolos. EF

Para cada definição de função na tabela de símbolos, três itens descrevem o início, o fim e o número de linhas. Cada um desses símbolos tem a função de classe de armazenamento (101):

Um registro de símbolo chamado. BF (função Begin). O campo de valor não é usado.

Um registro de símbolo chamado. LF (linhas na função). O campo valor fornece o número de linhas na função.

Um registro de símbolo chamado. EF (fim da função). O campo valor tem o mesmo número que o campo tamanho total no registro de símbolo de definição de função.

Os registros de símbolo. BF e. EF (mas não os registros. LF) são seguidos por um registro auxiliar com o seguinte formato:



| Deslocamento         | Tamanho          | Campo                                         | Descrição                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Não usado <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | LineNumber <br/>                        | O número de linha ordinal real (1, 2, 3 e assim por diante) dentro do arquivo de origem, correspondente ao registro. BF ou. EF. <br/>                                               |
| 6 <br/>  | 6 <br/> | Não usado <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction (somente BF) <br/> | O índice Symbol-Table do próximo registro de símbolo. BF. Se a função for a última na tabela de símbolos, esse campo será definido como zero. Ele não é usado para registros. EF. <br/> |
| 16 <br/> | 2 <br/> | Não usado <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Formato auxiliar 3: externamente fracas

"Externas fracas" são um mecanismo para arquivos de objeto que permite flexibilidade no momento do link. Um módulo pode conter um símbolo externo não resolvido (sym1), mas também pode incluir um registro auxiliar que indica que, se sym1 não estiver presente no momento do link, outro símbolo externo (sym2) será usado para resolver referências.

Se uma definição de sym1 estiver vinculada, uma referência externa ao símbolo será resolvida normalmente. Se uma definição de sym1 não estiver vinculada, todas as referências para o externo fraco para sym1 referem-se a sym2 em vez disso. O símbolo externo, sym2, deve sempre ser vinculado; Normalmente, ele é definido no módulo que contém a referência fraca para sym1.

As externas fracas são representadas por um registro de tabela de símbolos com a classe de armazenamento externo, o número da seção UNDEF e um valor de zero. O registro de símbolo externo fraco é seguido por um registro auxiliar com o seguinte formato:



| Deslocamento        | Tamanho           | Campo                       | Descrição                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | O índice de tabela de símbolos de sym2, o símbolo a ser vinculado se sym1 não for encontrado. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Características <br/> | Um valor de imagem \_ de \_ pesquisa externa fraca \_ \_ nolibrary indica que nenhuma pesquisa de biblioteca para sym1 deve ser executada. <br/> Um valor de IMAGE \_ \_ biblioteca de \_ pesquisa externa fraca \_ indica que uma pesquisa de biblioteca para sym1 deve ser executada. <br/> Um valor de \_ alias de \_ pesquisa externa fraca de imagem \_ \_ indica que sym1 é um alias para sym2. <br/> |
| 8 <br/> | 10 <br/> | Não usado <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Observe que o campo características não está definido em WINNT. T em vez disso, o campo tamanho total é usado.

#### <a name="auxiliary-format-4-files"></a>Formato auxiliar 4: arquivos

Esse formato segue um registro de tabela de símbolos com o arquivo de classe de armazenamento (103). O nome do símbolo em si deve ser. File e o registro auxiliar que o segue fornece o nome de um arquivo de código-fonte.



| Deslocamento        | Tamanho           | Campo                 | Descrição                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | Nome do Arquivo <br/> | Uma cadeia de caracteres ANSI que fornece o nome do arquivo de origem. Isso será preenchido com valores nulos se for menor que o comprimento máximo. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Formato auxiliar 5: definições de seção

Esse formato segue um registro de tabela de símbolos que define uma seção. Um registro desse tipo tem um nome de símbolo que é o nome de uma seção (como. Text ou. drectve) e tem a classe de armazenamento estática (3). O registro auxiliar fornece informações sobre a seção à qual se refere. Portanto, ele duplica algumas das informações no cabeçalho da seção.



| Deslocamento         | Tamanho          | Campo                           | Descrição                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Comprimento <br/>              | O tamanho dos dados da seção; o mesmo que SizeOfRawData no cabeçalho da seção. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | O número de entradas de realocação para a seção. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | O número de entradas de número de linha para a seção. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | Soma <br/>            | A soma de verificação dos dados de pouca. Será aplicável se o sinalizador IMAGE \_ SCN \_ lnk \_ COMDAT estiver definido no cabeçalho da seção. Para obter mais informações, consulte [seções COMDAT (somente objeto)](#comdat-sections-object-only). <br/> |
| 12 <br/> | 2 <br/> | Número <br/>              | Índice baseado em um na tabela da seção associada. Isso é usado quando a configuração de seleção COMDAT é 5. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Seleção <br/>           | O número de seleção COMDAT. Isso será aplicável se a seção for uma seção COMDAT. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | Não usado <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>Seções COMDAT (somente objeto)

O campo de seleção do formato auxiliar de definição de seção será aplicável se a seção for uma seção COMDAT. Uma seção COMDAT é uma seção que pode ser definida por mais de um arquivo de objeto. (A imagem \_ do sinalizador SCN \_ lnk \_ COMDAT é definido no campo de sinalizadores de seção do cabeçalho da seção.) O campo seleção determina a maneira como o vinculador resolve as várias definições de seções COMDAT.

O primeiro símbolo que tem o valor da seção da seção COMDAT deve ser o símbolo da seção. Esse símbolo tem o nome da seção, o campo de valor igual a zero, o número da seção da seção COMDAT em questão, o campo de tipo igual a IMAGE \_ Sym \_ tipo \_ NULL, o campo de classe igual a Image \_ Sym \_ Class \_ static e um registro auxiliar. O segundo símbolo é chamado de "símbolo COMDAT" e é usado pelo vinculador em conjunto com o campo de seleção.

Os valores para o campo de seleção são mostrados abaixo.



| Constante                                        | Valor         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGEM \_ COMDAT \_ selecionar \_ noduplicatas <br/> | 1 <br/> | Se esse símbolo já estiver definido, o vinculador emitirá um erro "símbolo definido de multiplicação". <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGEM \_ COMDAT \_ selecionar \_ qualquer <br/>          | 2 <br/> | Qualquer seção que define o mesmo símbolo COMDAT pode ser vinculada; o restante é removido. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGEM \_ COMDAT \_ selecionar \_ mesmo \_ tamanho <br/>   | 3 <br/> | O vinculador escolhe uma seção arbitrária entre as definições deste símbolo. Se todas as definições não forem do mesmo tamanho, um erro "símbolo definido de multiplicação" será emitido. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGEM \_ COMDAT \_ selecionar \_ \_ correspondência exata <br/> | 4 <br/> | O vinculador escolhe uma seção arbitrária entre as definições deste símbolo. Se todas as definições não corresponderem exatamente, um erro "símbolo definido de multiplicação" será emitido. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGEM \_ COMDAT \_ selecionar \_ Associação <br/>  | 5 <br/> | A seção será vinculada se uma certa outra seção COMDAT estiver vinculada. Essa outra seção é indicada pelo campo número do registro de símbolo auxiliar para a definição da seção. Essa configuração é útil para definições que têm componentes em várias seções (por exemplo, código em um e dados em outro), mas onde todas devem ser vinculadas ou descartadas como um conjunto. A outra seção à qual esta seção está associada deve ser uma seção COMDAT, que pode ser outra seção COMDAT associativa. Uma cadeia de associação da seção de seções COMDATs associativas não pode formar um loop. A cadeia de associação de seção deve eventualmente vir a uma seção COMDAT que não tem a imagem \_ COMDAT \_ selecione \_ conjunto associativo. <br/> |
| IMAGEM \_ COMDAT \_ selecionar \_ maior <br/>      | 6 <br/> | O vinculador escolhe a maior definição entre todas as definições deste símbolo. Se várias definições tiverem esse tamanho, a escolha entre elas será arbitrária. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>Definição de token CLR (somente objeto)

Esse símbolo auxiliar geralmente segue o \_ token CLR da classe Sym da imagem \_ \_ \_ . Ele é usado para associar um token ao namespace da tabela de símbolos COFF.



| Deslocamento        | Tamanho           | Campo                        | Descrição                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bAuxType <br/>         | Deve ser o \_ \_ \_ tipo de símbolo aux de imagem \_ \_ de token def (1). <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Reservado, deve ser zero. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | O índice de símbolo do símbolo COFF ao qual essa definição de token CLR se refere. <br/> |
| 6 <br/> | 12 <br/> |                              | Reservado, deve ser zero. <br/>                                                        |



 

### <a name="coff-string-table"></a>Tabela de cadeia de caracteres COFF

Imediatamente após a tabela de símbolos COFF está a tabela de cadeia de caracteres COFF. A posição dessa tabela é encontrada ao pegar o endereço da tabela de símbolos no cabeçalho COFF e adicionar o número de símbolos multiplicado pelo tamanho de um símbolo.

No início da tabela de cadeia de caracteres COFF há 4 bytes que contêm o tamanho total (em bytes) do restante da tabela de cadeias de caracteres. Esse tamanho inclui o próprio campo de tamanho, para que o valor nesse local seja 4 se nenhuma cadeia de caracteres estivesse presente.

Após o tamanho, são cadeias de caracteres terminadas em nulo apontadas por símbolos na tabela de símbolos COFF.

### <a name="the-attribute-certificate-table-image-only"></a>A tabela de certificado de atributo (somente imagem)

Os certificados de atributo podem ser associados a uma imagem com a adição de uma tabela de certificado de atributo. A tabela de certificado de atributo é composta de um conjunto de entradas de certificado de atributo contíguos e alinhadas em quadword. O preenchimento zero é inserido entre a extremidade original do arquivo e o início da tabela de certificado de atributo para alcançar esse alinhamento. Cada entrada de certificado de atributo contém os campos a seguir.



| Deslocamento       | Tamanho                         | Campo                       | Descrição                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Especifica o comprimento da entrada do certificado de atributo. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Contém o número de versão do certificado. Para obter detalhes, consulte o texto a seguir.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Especifica o tipo de conteúdo em bCertificate. Para obter detalhes, consulte o texto a seguir.<br/>             |
| 8<br/> | Consulte o seguinte<br/> | bCertificate<br/>     | Contém um certificado, como uma assinatura Authenticode. Para obter detalhes, consulte o texto a seguir.<br/> |



 

O valor de endereço virtual da entrada da tabela de certificado no diretório de dados de cabeçalho opcional é um deslocamento de arquivo para a primeira entrada de certificado de atributo. As entradas subsequentes são acessadas avançando os bytes de dwLength da entrada, arredondados para um múltiplo de 8 bytes, do início da entrada do certificado de atributo atual. Isso continuará até que a soma dos valores de dwLength arredondados seja igual ao valor de tamanho da entrada da tabela certificados no diretório de dados de cabeçalho opcional. Se a soma dos valores arredondados de dwLength não for igual ao valor de tamanho, a tabela de certificado de atributo ou o campo tamanho será corrompido.

Por exemplo, se a entrada da tabela de certificado do diretório de dados de cabeçalho opcional contiver:


```C++
virtual address = 0x5000
size = 0x1000
```



O primeiro certificado começa no offset 0x5000 do início do arquivo no disco. Para avançar todas as entradas de certificado de atributo:

1.  Adicione o valor dwLength do primeiro certificado de atributo ao deslocamento inicial.
2.  Arredonde o valor da etapa 1 para cima até o múltiplo de 8 bytes mais próximo para localizar o deslocamento da segunda entrada de certificado de atributo.
3.  Adicione o valor de deslocamento da etapa 2 ao segundo valor dwLength da entrada de certificado de atributo e Arredonde para o múltiplo mais próximo de 8 bytes para determinar o deslocamento da terceira entrada de certificado de atributo.
4.  Repita a etapa 3 para cada certificado sucessivo até que o deslocamento calculado seja igual a 0x6000 (0x5000 início + 0x1000, tamanho total), que indica que você analisou a tabela inteira.

Como alternativa, você pode enumerar as entradas de certificado chamando a função Win32 **ImageEnumerateCertificates** em um loop. Para obter um link para a página de referência da função, consulte [References](#references).

As entradas de tabela de certificado de atributo podem conter qualquer tipo de certificado, desde que a entrada tenha o valor de dwLength correto, um valor de wRevision exclusivo e um valor de wCertificateType exclusivo. O tipo mais comum de entrada de tabela de certificado é uma \_ estrutura de certificado do Win, que está documentada em wintrust. h e discutida no restante desta seção.

As opções para o \_ membro Win Certificate **wRevision** incluem (mas não se limitam a) o seguinte.



| Valor             | Nome                                 | Observações                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | Revisão de certificado de WIN \_ \_ \_ 1 \_ 0<br/> | Versão 1, versão herdada da estrutura de certificado do Win \_ . Há suporte apenas para fins de verificação de assinaturas Authenticode herdadas<br/> |
| 0x0200<br/> | Revisão de certificado de vitórias \_ \_ \_ 2 \_ 0<br/> | A versão 2 é a versão atual da estrutura de certificado do Win \_ . <br/>                                                                       |



 

As opções para o \_ membro Win Certificate **wCertificateType** incluem (mas não estão limitadas a) os itens na tabela a seguir. Observe que alguns valores não têm suporte no momento.



| Valor             | Nome                                           | Observações                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | Tipo de certificado do WIN \_ \_ \_ X509 <br/>              | bCertificate contém um certificado X. 509 <br/> Sem suporte<br/>         |
| 0x0002<br/> | tipo de certificado do WIN \_ \_ \_ \_ dados assinados PKCS \_<br/> | bCertificate contém uma \# estrutura SIGNEDDATA PKCS 7<br/>                         |
| 0x0003<br/> | Tipo de certificado de vitória \_ \_ \_ reservado \_ 1<br/>        | Reservado <br/>                                                                    |
| 0x0004<br/> | \_tipo de certificado Win \_ \_ \_ pilha TS Stack \_ assinado<br/>  | Assinatura de certificado de pilha de protocolo Terminal Server <br/> Sem suporte<br/> |



 

O \_ membro **bCertificate** da estrutura de certificados do Win contém uma matriz de bytes de comprimento variável com o tipo de conteúdo especificado por **wCertificateType**. O tipo com suporte de Authenticode é \_ o \_ tipo \_ de certificado Win \_ dados assinados PKCS \_ , uma \# estrutura **SignedData** PKCS 7. Para obter detalhes sobre o formato de assinatura digital Authenticode, consulte [formato de assinatura executável portátil do Windows Authenticode](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Se o conteúdo de **bCertificate** não terminar em um limite de quadword, a entrada do certificado de atributo será preenchida com zeros, do final do **bCertificate** para o próximo limite de quadword.

O valor de **dwLength** é o comprimento da estrutura de certificado do Win finalizada \_ e é calculado como:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Esse comprimento deve incluir o tamanho de qualquer preenchimento que seja usado para atender ao requisito de que cada \_ estrutura de certificado do Win esteja quadword alinhada:

` dwLength += (8 - (dwLength & 7)) & 7;`

O **tamanho da tabela do certificado**– especificado na entrada da **tabela certificados** nos [diretórios de dados de cabeçalho opcionais (somente imagem)](#optional-header-data-directories-image-only)– inclui o preenchimento.

Para obter mais informações sobre como usar a API de ImageHlp para enumerar, adicionar e remover certificados de arquivos PE, consulte [ImageHlp Functions](imagehlp-functions.md).

#### <a name="certificate-data"></a>Dados do certificado

Conforme indicado na seção anterior, os certificados na tabela de certificado de atributo podem conter qualquer tipo de certificado. Os certificados que garantem a integridade de um arquivo PE podem incluir um hash de imagem PE.

Um hash de imagem PE (ou hash de arquivo) é semelhante a uma soma de verificação de arquivo, pois o algoritmo de hash produz um resumo de mensagem que está relacionado à integridade de um arquivo. No entanto, uma soma de verificação é produzida por um algoritmo simples e é usada principalmente para detectar se um bloco de memória em disco ficou insatisfatório e os valores armazenados ali foram corrompidos. Um hash de arquivo é semelhante a uma soma de verificação, pois ele também detecta corrupção de arquivo. No entanto, ao contrário da maioria dos algoritmos de soma de verificação, é muito difícil modificar um arquivo sem alterar o hash de arquivo de seu valor original não modificado. Portanto, um hash de arquivo pode ser usado para detectar modificações intencionais e até mesmo sutis em um arquivo, como aqueles introduzidos por vírus, hackers ou programas de cavalo de Troia.

Quando incluído em um certificado, o resumo da imagem deve excluir determinados campos na imagem do PE, como a soma de verificação e a entrada da tabela de certificado em diretórios de dados de cabeçalho opcionais. Isso ocorre porque o ato de adicionar um certificado altera esses campos e faria com que um valor de hash diferente fosse calculado.

A função **ImageGetDigestStream** do Win32 fornece um fluxo de dados de um arquivo PE de destino com o qual as funções de hash são. Esse fluxo de dados permanece consistente quando os certificados são adicionados ou removidos de um arquivo PE. Com base nos parâmetros que são passados para **ImageGetDigestStream**, outros dados da imagem PE podem ser omitidos da computação de hash. Para obter um link para a página de referência da função, consulte [References](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load importar tabelas (somente imagem)

Essas tabelas foram adicionadas à imagem para dar suporte a um mecanismo uniforme para que os aplicativos adiem o carregamento de uma DLL até a primeira chamada para essa DLL. O layout das tabelas corresponde ao das tabelas de importação tradicionais que são descritas na seção 6,4, [a seção. iData](#the-idata-section)". Apenas alguns detalhes são discutidos aqui.

#### <a name="the-delay-load-directory-table"></a>A tabela do Delay-Load Directory

A tabela de diretório de carregamento de atraso é a contraparte da tabela de importação de diretório. Ele pode ser recuperado por meio da entrada do descritor de importação de atraso na lista de diretórios de dados de cabeçalho opcionais (offset 200). A tabela é organizada da seguinte maneira:



| Deslocamento         | Tamanho          | Campo                                  | Descrição                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Atributos <br/>                 | Deve ser zero. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Nome <br/>                       | O RVA do nome da DLL a ser carregada. O nome reside na seção de dados somente leitura da imagem. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Identificador de módulo <br/>              | O RVA do identificador do módulo (na seção de dados da imagem) da DLL a ser carregada com atraso. Ele é usado para armazenamento pela rotina que é fornecida para gerenciar o carregamento de atraso. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Atrasar tabela de endereços de importação <br/> | O RVA da tabela de endereços de importação de carregamento de atraso. Para obter mais informações, consulte [atrasar a tabela de endereços de importação (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Atrasar tabela de nomes de importação <br/>    | O RVA da tabela de nome de carregamento de atraso, que contém os nomes das importações que podem precisar ser carregadas. Isso corresponde ao layout da tabela de nomes de importação. Para obter mais informações, consulte a [tabela de dicas/nome](#hintname-table).<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Tabela de importação de atrasos associadas <br/>   | O RVA da tabela de endereços de carregamento de atraso associado, se existir. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Descarregar tabela de importação de atraso <br/>  | O RVA da tabela de endereços de carregamento de atraso de descarga, se existir. Esta é uma cópia exata da tabela de endereços de importação de atraso. Se o chamador descarregar a DLL, essa tabela deverá ser copiada de volta na tabela de endereços de importação de atraso para que as chamadas subsequentes para a DLL continuem a usar o mecanismo de conversão corretamente. <br/> |
| 28 <br/> | 4 <br/> | Carimbo de Data/Hora <br/>                 | O carimbo de data/hora da DLL à qual esta imagem foi associada. <br/>                                                                                                                                                                                                                                                     |



 

As tabelas que são referenciadas nessa estrutura de dados são organizadas e classificadas da mesma forma que suas contrapartes para importações tradicionais. Para obter detalhes, consulte [a seção. iData](#the-idata-section).

#### <a name="attributes"></a>Atributos

Como ainda, nenhum sinalizador de atributo é definido. O vinculador define esse campo como zero na imagem. Esse campo pode ser usado para estender o registro indicando a presença de novos campos ou pode ser usado para indicar comportamentos para as funções auxiliares de atraso ou descarregamento.

#### <a name="name"></a>Nome

O nome da DLL a ser carregada com atraso reside na seção de dados somente leitura da imagem. Ele é referenciado por meio do campo szName.

#### <a name="module-handle"></a>Identificador de módulo

O identificador da DLL a ser carregada com atraso está na seção de dados da imagem. O campo phmod aponta para o identificador. O auxiliar de carregamento de atraso fornecido usa esse local para armazenar o identificador para a DLL carregada.

#### <a name="delay-import-address-table"></a>Atrasar tabela de endereços de importação

A tabela de endereços de importação de atraso (IAT) é referenciada pelo descritor de importação de atraso por meio do campo pIAT. O auxiliar de carregamento de atraso atualiza esses ponteiros com os pontos de entrada reais para que as conversões não estejam mais no loop de chamada. Os ponteiros de função são acessados usando a expressão `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Atrasar tabela de nomes de importação

A tabela de nomes de importação de atraso (INT) contém os nomes das importações que podem exigir carregamento. Elas são ordenadas da mesma maneira que os ponteiros de função no IAT. Eles consistem nas mesmas estruturas que o padrão INT e são acessados usando a expressão `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Atrasar a tabela de endereços de importação e o carimbo de data/hora

A tabela de endereços de importação de limite de atraso (BIAT) é uma tabela opcional de itens de dados de conversão de imagem \_ \_ que é usada junto com o campo de carimbo de data/hora da tabela de diretório de carregamento de atraso por uma fase de associação pós-processo.

#### <a name="delay-unload-import-address-table"></a>Atrasar descarregamento da tabela de endereços de importação

O atraso de descarregar tabela de endereços de importação (UIAT) é uma tabela opcional de itens de dados de conversão de imagem \_ \_ que o código de descarregamento usa para lidar com uma solicitação de descarga explícita. Ele consiste em dados inicializados na seção somente leitura, que é uma cópia exata do IAT original que mencionou o código para as conversões de carregamento de atraso. Na solicitação de descarga, a biblioteca pode ser liberada, o \* phmod limpo e o UIAT escrito sobre o IAT para restaurar tudo para seu estado de pré-carregamento.

## <a name="special-sections"></a>Seções especiais

- [A seção. Debug](#the-debug-section)
  - [Diretório de depuração (somente imagem)](#debug-directory-image-only)
  - [Tipo de depuração](#debug-type)
  - [. Debug $ F (somente objeto)](#debugf-object-only)
  - [. Debug $ S (somente objeto)](#debugs-object-only)
  - [. Debug $ P (somente objeto)](#debugp-object-only)
  - [. debug $ T (somente objeto)](#debugt-object-only)
  - [Suporte do vinculador para informações de depuração da Microsoft](#linker-support-for-microsoft-debug-information)
- [A seção. drectve (somente objeto)](#the-drectve-section-object-only)
- [A seção. Edata (somente imagem)](#the-edata-section-image-only)
  - [Exportar tabela de diretórios](#export-directory-table)
  - [Exportar tabela de endereços](#export-address-table)
  - [Exportar tabela de ponteiros de nome](#export-name-pointer-table)
  - [Exportar tabela ordinal](#export-ordinal-table)
  - [Exportar tabela de nomes](#export-name-table)
- [A seção. iData](#the-idata-section)
  - [Importar tabela de diretórios](#import-directory-table)
  - [Importar tabela de pesquisa](#import-lookup-table)
  - [Tabela de dica/nome](#hintname-table)
  - [Importar tabela de endereços](#delay-import-address-table)
- [A seção. pData](#the-pdata-section)
- [A seção. realocação (somente imagem)](#the-reloc-section-image-only)
  - [Bloco de realocação de base](#base-relocation-block)
  - [Tipos de realocação base](#base-relocation-types)
- [A seção. TLS](#the-tls-section)
  - [O diretório TLS](#the-tls-directory)
  - [Funções de retorno de chamada TLS](#tls-callback-functions)
- [A estrutura de configuração de carregamento (somente imagem)](#the-load-configuration-structure-image-only)
  - [Carregar diretório de configuração](#load-configuration-directory)
  - [Carregar layout de configuração](#load-configuration-layout)
- [A seção. rsrc](#the-rsrc-section)
  - [Tabela de diretório de recursos](#resource-directory-table)
  - [Entradas do diretório de recursos](#resource-directory-entries)
  - [Cadeia de caracteres do diretório de recursos](#resource-directory-string)
  - [Entrada de dados do recurso](#resource-data-entry)
- [A seção. cormeta (somente objeto)](#the-cormeta-section-object-only)
- [A seção. sxdata](#the-sxdata-section)

As seções COFF típicas contêm código ou dados que os vinculadores e os carregadores do Microsoft Win32 não têm conhecimento especial sobre o conteúdo da seção. O conteúdo é relevante apenas para o aplicativo que está sendo vinculado ou executado.

No entanto, algumas seções COFF têm significados especiais quando encontradas em arquivos de objeto ou arquivos de imagem. Ferramentas e carregadores reconhecem essas seções porque têm sinalizadores especiais definidos no cabeçalho da seção, porque localizações especiais no cabeçalho opcional da imagem apontam para elas ou porque o próprio nome da seção indica uma função especial da seção. (Mesmo que o nome da seção em si não indique uma função especial da seção, o nome da seção é ditado por convenção, de modo que os autores dessa especificação possam se referir a um nome de seção em todos os casos.)

As seções reservadas e seus atributos são descritos na tabela a seguir, seguida por descrições detalhadas para os tipos de seção que são persistidos em executáveis e os tipos de seção que contêm metadados para extensões.



| Nome da seção          | Conteúdo                                                                                                                                                                  | Características                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| . BSS <br/>      | Dados não inicializados (formato livre) <br/>                                                                                                                             | Image \_ SCN \_ CNT \_ Uninitialized \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | Metadados CLR que indicam que o arquivo de objeto contém código gerenciado <br/>                                                                                       | informações do IMAGE \_ SCN \_ lnk \_ <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . Data <br/>     | Dados inicializados (formato livre) <br/>                                                                                                                               | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . Debug $ F <br/>  | Informações de depuração FPO geradas (somente objeto, somente arquitetura x86 e agora obsoleto) <br/>                                                                       | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem é \_ Descartado <br/>                                                                                                                                                                                                                                                                                           |
| . Debug $ P <br/>  | Tipos de depuração pré-compilados (somente objeto) <br/>                                                                                                                        | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem é \_ Descartado <br/>                                                                                                                                                                                                                                                                                           |
| . depurar $ S <br/>  | Depurar símbolos (somente objeto) <br/>                                                                                                                                  | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem é \_ Descartado <br/>                                                                                                                                                                                                                                                                                           |
| . debug $ T <br/>  | Tipos de depuração (somente objeto) <br/>                                                                                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem é \_ Descartado <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Opções do vinculador <br/>                                                                                                                                               | informações do IMAGE \_ SCN \_ lnk \_ <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Exportar tabelas <br/>                                                                                                                                                | Image \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                                           |
| .idata <br/>    | Importar tabelas <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| .idlsym <br/>   | Inclui SEH (Image only) registrado para dar suporte a atributos IDL. Para obter informações, consulte "atributos IDL" em [referências](#references) no final deste tópico. <br/> | informações do IMAGE \_ SCN \_ lnk \_ <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . pData <br/>    | Informações da exceção <br/>                                                                                                                                        | Image \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                                           |
| . rdata <br/>    | Dados inicializados somente leitura <br/>                                                                                                                                   | Image \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                                           |
| . realocação <br/>    | Realocações de imagem <br/>                                                                                                                                            | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem é \_ Descartado <br/>                                                                                                                                                                                                                                                                                           |
| . rsrc <br/>     | Diretório de recursos <br/>                                                                                                                                           | Image \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                                           |
| . seção sbss <br/>     | Dados não inicializados de GP relativos (formato livre) <br/>                                                                                                                 | IMAGE \_ SCN \_ CNT \_ Uninitialized \_ Data \| Image \_ SCN \_ mem \_ Read \| IMAGE \_ SCN \_ mem \_ Write \| Image \_ SCN \_ GPREL o \_ sinalizador Image SCN \_ GPREL Flag deve ser definido apenas para arquiteturas IA64; esse sinalizador não é válido para outras arquiteturas. O \_ sinalizador GPREL de SCN de imagem \_ é apenas para arquivos de objeto; quando esse tipo de seção aparece em um arquivo de imagem, o sinalizador de GPREL de SCN de imagem \_ \_ não deve ser definido. <br/> |
| . sdata <br/>    | Dados inicializados com relação a GP (formato livre) <br/>                                                                                                                   | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| IMAGE \_ SCN \_ mem \_ Write \| Image \_ SCN \_ GPREL o \_ sinalizador Image SCN \_ GPREL Flag deve ser definido apenas para arquiteturas IA64; esse sinalizador não é válido para outras arquiteturas. O \_ sinalizador GPREL de SCN de imagem \_ é apenas para arquivos de objeto; quando esse tipo de seção aparece em um arquivo de imagem, o sinalizador de GPREL de SCN de imagem \_ \_ não deve ser definido. <br/>   |
| .srdata <br/>   | Dados somente leitura relativos a GP (formato livre) <br/>                                                                                                                     | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ GPREL o \_ sinalizador Image SCN \_ GPREL deve ser definido apenas para arquiteturas IA64; esse sinalizador não é válido para outras arquiteturas. O \_ sinalizador GPREL de SCN de imagem \_ é apenas para arquivos de objeto; quando esse tipo de seção aparece em um arquivo de imagem, o sinalizador de GPREL de SCN de imagem \_ \_ não deve ser definido. <br/>                             |
| .sxdata <br/>   | Dados do manipulador de exceção registrado (formato livre e apenas x86/Object) <br/>                                                                                          | \_O Image SCN \_ lnk \_ info contém o índice de símbolo de cada um dos manipuladores de exceção que estão sendo referenciados pelo código nesse arquivo de objeto. O símbolo pode ser para um símbolo de UNDEF ou um que esteja definido nesse módulo. <br/>                                                                                                                                                                     |
| .text <br/>     | Código executável (formato livre) <br/>                                                                                                                                | IMAGE \_ SCN \_ CNT \_ Code \| Image \_ SCN \_ mem \_ executar \| IIMAGE \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                           |
| . TLS <br/>      | Armazenamento local de thread (somente objeto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . TLS $ <br/>     | Armazenamento local de thread (somente objeto) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| .vsdata <br/>   | Dados inicializados com relação a GP (formato livre e somente para arquiteturas ARM, SH4 e Thumb) <br/>                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read \| Image \_ SCN \_ mem \_ Write <br/>                                                                                                                                                                                                                                                                                                 |
| . xdata <br/>    | Informações de exceção (formato livre) <br/>                                                                                                                          | Image \_ SCN \_ CNT \_ INITIALIZED \_ Data \| Image \_ SCN \_ mem \_ Read <br/>                                                                                                                                                                                                                                                                                                                           |



 

Algumas das seções listadas aqui são marcadas como "somente objeto" ou "somente imagem" para indicar que sua semântica especial é relevante apenas para arquivos de objeto ou arquivos de imagem, respectivamente. Uma seção que está marcada como "imagem somente" pode ainda aparecer em um arquivo de objeto como uma maneira de entrar no arquivo de imagem, mas a seção não tem um significado especial para o vinculador, somente para o carregador de arquivo de imagem.

### <a name="the-debug-section"></a>A seção. Debug

A seção. Debug é usada em arquivos de objeto para conter informações de depuração geradas pelo compilador e em arquivos de imagem para conter todas as informações de depuração geradas. Esta seção descreve o empacotamento de informações de depuração em arquivos de objeto e imagem.

A próxima seção descreve o formato do diretório de depuração, que pode estar em qualquer lugar da imagem. As seções subsequentes descrevem os "grupos" em arquivos de objeto que contêm informações de depuração.

O padrão para o vinculador é que as informações de depuração não são mapeadas para o espaço de endereço da imagem. Uma seção. Debug existe somente quando as informações de depuração são mapeadas no espaço de endereço.

#### <a name="debug-directory-image-only"></a>Diretório de depuração (somente imagem)

Os arquivos de imagem contêm um diretório de depuração opcional que indica qual formulário de informações de depuração está presente e onde está. Esse diretório consiste em uma matriz de entradas do diretório de depuração cujo local e tamanho são indicados no cabeçalho opcional da imagem.

O diretório de depuração pode estar em uma seção descartada. debug (se houver) ou pode ser incluído em qualquer outra seção no arquivo de imagem, ou não estar em uma seção.

Cada entrada do diretório de depuração identifica o local e o tamanho de um bloco de informações de depuração. O RVA especificado poderá ser zero se as informações de depuração não forem cobertas por um cabeçalho de seção (ou seja, ela residir no arquivo de imagem e não estiver mapeada no espaço de endereço de tempo de execução). Se ele for mapeado, o RVA será seu endereço.

Uma entrada de diretório de depuração tem o seguinte formato:



| Deslocamento         | Tamanho          | Campo                        | Descrição                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Características <br/>  | Reservado, deve ser zero. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | A hora e a data em que os dados de depuração foram criados. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | O número de versão principal do formato de dados de depuração. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | O número de versão secundária do formato de dados de depuração. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Tipo <br/>             | O formato das informações de depuração. Este campo habilita o suporte a vários depuradores. Para obter mais informações, consulte [debug Type](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | O tamanho dos dados de depuração (não incluindo o próprio diretório de depuração). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | O endereço dos dados de depuração quando carregados, em relação à base da imagem. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | O ponteiro de arquivo para os dados de depuração. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Tipo de depuração

Os valores a seguir são definidos para o campo de tipo da entrada do diretório de depuração:



| Constante                                        | Valor          | Descrição                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| tipo de depuração de imagem \_ \_ \_ desconhecido <br/>         | 0 <br/>  | Um valor desconhecido que é ignorado por todas as ferramentas. <br/>                                                                                                                                                       |
| tipo de depuração de imagem \_ \_ \_ COFF <br/>            | 1 <br/>  | As informações de depuração do COFF (números de linha, tabela de símbolos e tabela de cadeia de caracteres). Esse tipo de informação de depuração também é apontado por campos nos cabeçalhos de arquivo. <br/>                                          |
| tipo de depuração de imagem \_ \_ \_ CODEVIEW <br/>        | 2 <br/>  | As informações de depuração de Visual C++. <br/>                                                                                                                                                                    |
| tipo de depuração de imagem \_ \_ \_ FPO <br/>             | 3 <br/>  | As informações de omissão do ponteiro do quadro (FPO). Essas informações dizem ao depurador como interpretar quadros de pilhas não padrão, que usam o Registro EBP para uma finalidade diferente de um ponteiro de quadro. <br/> |
| tipo de depuração de imagem \_ \_ \_ misc <br/>            | 4 <br/>  | O local do arquivo DBG. <br/>                                                                                                                                                                            |
| \_exceção de \_ tipo de depuração de imagem \_ <br/>       | 5 <br/>  | Uma cópia da seção. pData. <br/>                                                                                                                                                                            |
| \_correção de \_ tipo de depuração de imagem \_ <br/>           | 6 <br/>  | Reservado. <br/>                                                                                                                                                                                            |
| \_ \_ tipo de depuração \_ de imagem OMAP \_ como \_ src <br/>   | 7 <br/>  | O mapeamento de um RVA na imagem para um RVA na imagem de origem. <br/>                                                                                                                                          |
| \_ \_ tipo de depuração \_ de imagem OMAP \_ da \_ src <br/> | 8 <br/>  | O mapeamento de um RVA na imagem de origem para um RVA na imagem. <br/>                                                                                                                                          |
| tipo de depuração de imagem \_ \_ \_ BORLAND <br/>         | 9 <br/>  | Reservado para Borland. <br/>                                                                                                                                                                                |
| Tipo de depuração de imagem \_ \_ \_ RESERVED10 <br/>      | 10 <br/> | Reservado. <br/>                                                                                                                                                                                            |
| \_CLSID do \_ tipo de depuração de imagem \_ <br/>           | 11 <br/> | Reservado. <br/>                                                                                                                                                                                            |
| \_reprodução de \_ tipo de depuração de imagem \_ <br/>           | 16 <br/> | Determinante do PE ou reprodução. <br/>                                                                                                                                                                   |
| tipo de depuração de imagem \_ \_ \_ ex \_ DLLCHARACTERISTICS | 20 | Bits de características de DLL estendidas. |



 

Se o campo tipo for definido como tipo de depuração de imagem \_ \_ \_ FPO, os dados brutos de depuração serão uma matriz na qual cada membro descreve o quadro de pilha de uma função. Nem todas as funções no arquivo de imagem devem ter informações de FPO definidas para ela, mesmo que o tipo de depuração seja FPO. Supõe-se que as funções que não têm informações de FPO tenham quadros de pilhas normais. O formato das informações FPO é o seguinte:


```C++
#define FRAME_FPO   0               
#define FRAME_TRAP  1
#define FRAME_TSS   2
               
typedef struct _FPO_DATA {
    DWORD       ulOffStart;            // offset 1st byte of function code
    DWORD       cbProcSize;            // # bytes in function
    DWORD       cdwLocals;             // # bytes in locals/4
    WORD        cdwParams;             // # bytes in params/4
    WORD        cbProlog : 8;          // # bytes in prolog
    WORD        cbRegs   : 3;          // # regs saved
    WORD        fHasSEH  : 1;          // TRUE if SEH in func
    WORD        fUseBP   : 1;          // TRUE if EBP has been allocated
    WORD        reserved : 1;          // reserved for future use
    WORD        cbFrame  : 2;          // frame type
} FPO_DATA;
```



A presença de uma entrada de tipo de depuração de imagem de tipo \_ \_ \_ reproduza indica que o arquivo PE foi criado de forma a atingir o determinante ou reprodução. Se a entrada não for alterada, o arquivo PE de saída é garantido como bit a bit idêntico, independentemente de quando ou onde o PE é produzido. Vários campos de carimbo de data/hora no arquivo PE são preenchidos com parte ou todos os bits de um valor de hash calculado que usa o conteúdo do arquivo PE como entrada e, portanto, não representam mais a data e a hora reais quando um arquivo PE ou dados específicos relacionados no PE é produzido. Os dados brutos dessa entrada de depuração podem estar vazios ou podem conter um valor de hash calculado precedido por um valor de quatro bytes que representa o comprimento do valor de hash.

Se o campo tipo for definido como tipo de depuração de imagem \_ \_ \_ \_ , por exemplo, DLLCHARACTERISTICS, os dados brutos de depuração conterão bits de características de dll estendidos, em outros, que podem ser definidos no cabeçalho opcional da imagem. Consulte [características de dll](#dll-characteristics) na seção [cabeçalho opcional Windows-Specific campos (somente imagem)](#optional-header-windows-specific-fields-image-only).

##### <a name="extended-dll-characteristics"></a>Características de DLL estendidas

Os valores a seguir são definidos para os bits de características de DLL estendidas.

| Constante | Valor | Descrição |
|-|-|-|
| IMAGE \_ DLLCHARACTERISTICS \_ ex \_ CET \_ compatível | 0x0001 | A imagem é compatível com CET. |

#### <a name="debugf-object-only"></a>. Debug $ F (somente objeto)

Os dados nesta seção foram substituídos no Visual C++ versão 7,0 e posterior por um conjunto de dados mais amplo que é emitido em uma subseção **. Debug $ S** .

Os arquivos de objeto podem conter seções. Debug $ F cujo conteúdo é um ou mais \_ registros de dados FPO (informações de omissão de ponteiro de quadro). Consulte " \_ \_ tipo de depuração \_ de imagem FPO" em [tipo de depuração](#debug-type).

O vinculador reconhece isso **. depurar $ F** registros. Se as informações de depuração estiverem sendo geradas, o vinculador classificará os \_ registros de dados FPO por RVA de procedimento e gerará uma entrada de diretório de depuração para eles.

O compilador não deve gerar registros FPO para procedimentos que têm um formato de quadro padrão.

#### <a name="debugs-object-only"></a>. Debug $ S (somente objeto)

Esta seção contém Visual C++ informações de depuração (informações simbólicas).

#### <a name="debugp-object-only"></a>. Debug $ P (somente objeto)

Esta seção contém Visual C++ informações de depuração (informações pré-compiladas). Esses são tipos compartilhados entre todos os objetos que foram compilados usando o cabeçalho pré-compilado que foi gerado com esse objeto.

#### <a name="debugt-object-only"></a>. debug $ T (somente objeto)

Esta seção contém Visual C++ informações de depuração (informações de tipo).

#### <a name="linker-support-for-microsoft-debug-information"></a>Suporte do vinculador para informações de depuração da Microsoft

Para oferecer suporte a informações de depuração, o vinculador:

-   Coleta todos os dados de depuração relevantes das seções **. Debug $ F**, **debug $ S**, **. Debug $ P** e **. debug $ T** .

-   Processa esses dados juntamente com as informações de depuração geradas pelo vinculador no arquivo PDB e cria uma entrada de diretório de depuração para fazer referência a ele.

### <a name="the-drectve-section-object-only"></a>A seção. drectve (somente objeto)

Uma seção é uma seção de diretiva se tiver o \_ sinalizador de informações de SCN lnk de imagem \_ \_ definido no cabeçalho da seção e tiver o nome da seção **. drectve** . O vinculador remove uma seção **. drectve** depois de processar as informações, portanto, a seção não aparece no arquivo de imagem que está sendo vinculado.

Uma seção **. drectve** consiste em uma cadeia de caracteres de texto que pode ser codificada como ANSI ou UTF-8. Se o marcador de ordem de byte UTF-8 (BOM, um prefixo de três bytes que consiste em 0xEF, 0xBB e 0xBF) não estiver presente, a cadeia de caracteres de diretiva será interpretada como ANSI. A cadeia de caracteres de diretiva é uma série de opções de vinculador que são separadas por espaços. Cada opção contém um hífen, o nome da opção e qualquer atributo apropriado. Se uma opção contiver espaços, a opção deverá ser colocada entre aspas. A seção **. drectve** não deve ter realocações ou números de linha.

### <a name="the-edata-section-image-only"></a>A seção. Edata (somente imagem)

A seção exportar dados, denominada. Edata, contém informações sobre símbolos que outras imagens podem acessar por meio de vinculação dinâmica. Os símbolos exportados geralmente são encontrados em DLLs, mas as DLLs também podem importar símbolos.

Uma visão geral da estrutura geral da seção exportar é descrita abaixo. As tabelas descritas geralmente são contíguas no arquivo na ordem mostrada (embora isso não seja necessário). Somente a tabela de exportação de diretório e a tabela de endereços de exportação são necessárias para exportar símbolos como ordinais. (Um ordinal é uma exportação que é acessada diretamente pelo índice da tabela de endereços de exportação.) A tabela de ponteiros de nome, a tabela ordinal e a tabela de nomes de exportação existem para dar suporte ao uso de nomes de exportação.



| Nome da tabela                         | Description                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exportar tabela de diretórios <br/> | Uma tabela com apenas uma linha (ao contrário do diretório de depuração). Esta tabela indica os locais e tamanhos das outras tabelas de exportação. <br/>                                                                                                                                                                                                               |
| Exportar tabela de endereços <br/>   | Uma matriz de RVAs de símbolos exportados. Esses são os endereços reais das funções e dos dados exportados no código executável e nas seções de dados. Outros arquivos de imagem podem importar um símbolo usando um índice para esta tabela (um ordinal) ou, opcionalmente, usando o nome público que corresponde ao ordinal se um nome público for definido. <br/> |
| Tabela de ponteiros de nome <br/>     | Uma matriz de ponteiros para os nomes de exportação públicos, classificados em ordem crescente. <br/>                                                                                                                                                                                                                                                                    |
| Tabela ordinal <br/>          | Uma matriz dos ordinais que correspondem aos membros da tabela de ponteiros de nome. A correspondência é por posição; Portanto, a tabela de ponteiros de nome e a tabela ordinal devem ter o mesmo número de membros. Cada ordinal é um índice na tabela de endereços de exportação. <br/>                                                                        |
| Exportar tabela de nomes <br/>      | Uma série de cadeias de caracteres ASCII terminadas em nulo. Os membros da tabela de ponteiros de nome apontam para essa área. Esses nomes são os nomes públicos pelos quais os símbolos são importados e exportados; Eles não são necessariamente os mesmos que os nomes privados que são usados no arquivo de imagem. <br/>                                                           |



 

Quando outro arquivo de imagem importa um símbolo por nome, o carregador Win32 pesquisa a tabela de ponteiros de nome para uma cadeia de caracteres correspondente. Se uma cadeia de caracteres correspondente for encontrada, o ordinal associado será identificado pesquisando o membro correspondente na tabela ordinal (ou seja, o membro da tabela ordinal com o mesmo índice que o ponteiro de cadeia de caracteres encontrado na tabela de ponteiros de nome). O ordinal resultante é um índice na tabela de endereços de exportação, que fornece o local real do símbolo desejado. Cada símbolo de exportação pode ser acessado por um ordinal.

Quando outro arquivo de imagem importa um símbolo por ordinal, é desnecessário Pesquisar a tabela de ponteiro de nome para uma cadeia de caracteres correspondente. O uso direto de um ordinal é, portanto, mais eficiente. No entanto, um nome de exportação é mais fácil de lembrar e não exige que o usuário saiba o índice de tabela do símbolo.

#### <a name="export-directory-table"></a>Exportar tabela de diretórios

As informações de exportação de símbolo começam com a tabela exportar diretório, que descreve o restante das informações de símbolo de exportação. A tabela exportar diretório contém informações de endereço que são usadas para resolver importações para os pontos de entrada dentro desta imagem.



| Deslocamento         | Tamanho          | Campo                                | Descrição                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Sinalizadores de exportação <br/>             | Reservado, deve ser 0. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Carimbo de data/hora <br/>          | A hora e a data em que os dados de exportação foram criados. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Versão Principal <br/>            | O número da versão principal. Os números de versão principal e secundária podem ser definidos pelo usuário. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Versão Secundária <br/>            | O número da versão secundária. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | RVA de nome <br/>                 | O endereço da cadeia de caracteres ASCII que contém o nome da DLL. Esse endereço é relativo à base da imagem. <br/>                                                |
| 16 <br/> | 4 <br/> | Base ordinal <br/>             | O número ordinal inicial para exportações nesta imagem. Este campo especifica o número ordinal inicial para a tabela de endereços de exportação. Normalmente, ele é definido como 1. <br/> |
| 20 <br/> | 4 <br/> | Entradas da tabela de endereços <br/>    | O número de entradas na tabela de endereços de exportação. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Número de ponteiros de nome <br/>  | O número de entradas na tabela de ponteiros de nome. Esse também é o número de entradas na tabela ordinal. <br/>                                                     |
| 28 <br/> | 4 <br/> | Exportar RVA de tabela de endereços <br/> | O endereço da tabela de endereços de exportação, em relação à base da imagem. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | RVA do ponteiro de nome <br/>         | O endereço da tabela de ponteiros do nome de exportação, em relação à base da imagem. O tamanho da tabela é fornecido pelo campo número de ponteiros de nome. <br/>                       |
| 36 <br/> | 4 <br/> | RVA da tabela ordinal <br/>        | O endereço da tabela ordinal, em relação à base da imagem. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Exportar tabela de endereços

A tabela de endereços de exportação contém o endereço de pontos de entrada exportados e dados exportados e absolutos. Um número ordinal é usado como um índice na tabela de endereços de exportação.

Cada entrada na tabela de endereços de exportação é um campo que usa um dos dois formatos na tabela a seguir. Se o endereço especificado não estiver dentro da seção de exportação (conforme definido pelo endereço e pelo comprimento que são indicados no cabeçalho opcional), o campo será um RVA de exportação, que é um endereço real no código ou nos dados. Caso contrário, o campo é um RVA do encaminhador, que nomeia um símbolo em outra DLL.



| Deslocamento        | Tamanho          | Campo                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Exportar RVA <br/>    | O endereço do símbolo exportado quando carregado na memória, em relação à base da imagem. Por exemplo, o endereço de uma função exportada. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | RVA do encaminhador <br/> | O ponteiro para uma cadeia de caracteres ASCII terminada em nulo na seção exportar. Essa cadeia de caracteres deve estar dentro do intervalo fornecido pela entrada do diretório de dados da tabela de exportação. Consulte [diretórios de dados de cabeçalho opcionais (somente imagem)](#optional-header-data-directories-image-only). Essa cadeia de caracteres fornece o nome da DLL e o nome da exportação (por exemplo, "MYDLL. expfunc") ou o nome da DLL e o número ordinal da exportação (por exemplo, "MYDLL. \# 27 "). <br/> |



 

Um RVA do encaminhador exporta uma definição de alguma outra imagem, fazendo com que ela seja exibida como se estivesse sendo exportada pela imagem atual. Portanto, o símbolo é importado e exportado simultaneamente.

Por exemplo, em Kernel32.dll no Windows XP, a exportação chamada "HeapAlloc" é encaminhada para a cadeia de caracteres "NTDLL. RtlAllocateHeap." Isso permite que os aplicativos usem o módulo específico do Windows XP Ntdll.dll sem realmente conter referências de importação para ele. A tabela de importação do aplicativo refere-se apenas a Kernel32.dll. Portanto, o aplicativo não é específico do Windows XP e pode ser executado em qualquer sistema Win32.

#### <a name="export-name-pointer-table"></a>Exportar tabela de ponteiros de nome

A tabela de ponteiro de nome de exportação é uma matriz de endereços (RVAs) na tabela de nomes de exportação. Os ponteiros são 32 bits cada e são relativos à base da imagem. Os ponteiros são ordenados lexicalmente para permitir pesquisas binárias.

Um nome de exportação será definido somente se a tabela de ponteiro de nome de exportação contiver um ponteiro para ele.

#### <a name="export-ordinal-table"></a>Exportar tabela ordinal

A tabela ordinal de exportação é uma matriz de índices não polarizados de 16 bits na tabela de endereços de exportação. Os ordinais são tendenciosas pelo campo base ordinal da tabela exportar diretório. Em outras palavras, a base ordinal deve ser subtraída dos ordinais para obter índices verdadeiros na tabela de endereços de exportação.

A tabela de ponteiro de nome de exportação e a tabela de exportação ordinal formam duas matrizes paralelas que são separadas para permitir o alinhamento de campo natural. Essas duas tabelas, na verdade, funcionam como uma tabela, na qual a coluna de ponteiro de nome de exportação aponta para um nome público (exportado) e a coluna ordinal de exportação fornece o ordinal correspondente para esse nome público. Um membro da tabela de ponteiro de nome de exportação e um membro da tabela de exportação ordinal são associados com a mesma posição (índice) em suas respectivas matrizes.

Assim, quando a tabela de ponteiros do nome de exportação é pesquisada e uma cadeia de caracteres correspondente é encontrada na posição i, o algoritmo para localizar o RVA do símbolo e o ordinal polarizado é:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Ao procurar um símbolo por ordinal (tendenciosa), o algoritmo para localizar o RVA e o nome do símbolo é:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Exportar tabela de nomes

A tabela de nome de exportação contém os dados de cadeia de caracteres reais que foram apontados pela tabela de ponteiros do nome de exportação. As cadeias de caracteres nessa tabela são nomes públicos que outras imagens podem usar para importar os símbolos. Esses nomes de exportação públicos não são necessariamente os mesmos que os nomes de símbolos privados que os símbolos têm em seu próprio arquivo de imagem e código-fonte, embora possam ser.

Cada símbolo exportado tem um valor ordinal, que é apenas o índice na tabela de endereços de exportação. No entanto, o uso de nomes de exportação é opcional. Alguns, todos ou nenhum dos símbolos exportados podem ter nomes de exportação. Para símbolos exportados que têm nomes de exportação, as entradas correspondentes na tabela de ponteiro de nome de exportação e a tabela ordinal de exportação funcionam em conjunto para associar cada nome a um ordinal.

A estrutura da tabela de nome de exportação é uma série de cadeias de caracteres ASCII com terminação nula de comprimento variável.

### <a name="the-idata-section"></a>A seção. iData

Todos os arquivos de imagem que importam símbolos, incluindo praticamente todos os arquivos executáveis (EXE), têm uma seção. iData. Segue um layout de arquivo típico para as informações de importação:

-   Tabela de diretórios

    Entrada de diretório nula

-   Tabela de pesquisa de importação do DLL1

    Nulo

-   Tabela de pesquisa de importação do DLL2

    Nulo

-   Tabela de pesquisa de importação do DLL3

    Nulo

-   Tabela de Hint-Name

#### <a name="import-directory-table"></a>Importar tabela de diretórios

As informações de importação começam com a tabela de importação de diretório, que descreve o restante das informações de importação. A tabela importar diretório contém informações de endereço que são usadas para resolver referências de correção para os pontos de entrada dentro de uma imagem DLL. A tabela importar diretório consiste em uma matriz de entradas do diretório de importação, uma entrada para cada DLL à qual a imagem se refere. A última entrada de diretório está vazia (preenchida com valores nulos), que indica o final da tabela de diretórios.

Cada entrada do diretório de importação tem o seguinte formato:



| Deslocamento         | Tamanho          | Campo                                                 | Descrição                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importar RVA (características) da tabela de pesquisa <br/> | O RVA da tabela de pesquisa de importação. Esta tabela contém um nome ou ordinal para cada importação. (O nome "características" é usado em Winnt. h, mas não descreve mais este campo.) <br/> |
| 4 <br/>  | 4 <br/> | Carimbo de data/hora <br/>                           | O carimbo que é definido como zero até que a imagem seja associada. Depois que a imagem é associada, esse campo é definido como o carimbo de data/hora da DLL. <br/>                                          |
| 8 <br/>  | 4 <br/> | Cadeia de encaminhadores <br/>                           | O índice da primeira referência do encaminhador. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | RVA de nome <br/>                                  | O endereço de uma cadeia de caracteres ASCII que contém o nome da DLL. Esse endereço é relativo à base da imagem. <br/>                                                                   |
| 16 <br/> | 4 <br/> | Importar a tabela de endereços RVA (tabela de conversão) <br/>    | O RVA da tabela de endereços de importação. O conteúdo dessa tabela é idêntico ao conteúdo da tabela de pesquisa de importação até que a imagem seja associada. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importar tabela de pesquisa

Uma tabela de pesquisa de importação é uma matriz de números de 32 bits para PE32 ou uma matriz de números de 64 bits para PE32 +. Cada entrada usa o formato de campo de bits descrito na tabela a seguir. Nesse formato, o bit 31 é o bit mais significativo para PE32 e bit 63 é o bit mais significativo para PE32 +. A coleção dessas entradas descreve todas as importações de uma determinada DLL. A última entrada é definida como zero (NULL) para indicar o fim da tabela.



| Bit (s)            | Tamanho           | Campo de bits                       | Description                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Sinalizador de ordinal/nome <br/>   | Se esse bit for definido, importe por ordinal. Caso contrário, importe por nome. O bit é mascarado como 0x80000000 para PE32, 0x8000000000000000 para PE32 +. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Número ordinal <br/>      | Um número ordinal de 16 bits. Esse campo só será usado se o campo de bit do sinalizador ordinal/nome for 1 (importar por ordinal). O bits 30-15 ou 62-15 deve ser 0. <br/>                  |
| 30-0 <br/>  | 31 <br/> | Dica/nome da tabela RVA <br/> | Um RVA de 31 bits de uma entrada de tabela de dica/nome. Esse campo só será usado se o campo de bit do sinalizador ordinal/nome for 0 (importar por nome). Para PE32 + bits 62-31 deve ser zero. <br/> |



 

#### <a name="hintname-table"></a>Tabela de dica/nome

Uma tabela de dica/nome é suficiente para a seção de importação inteira. Cada entrada na tabela de dica/nome tem o seguinte formato:



| Deslocamento         | Tamanho                 | Campo            | Descrição                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Hint <br/> | Um índice na tabela de ponteiros do nome de exportação. Uma correspondência é tentada primeiro com esse valor. Se falhar, uma pesquisa binária será executada na tabela de ponteiro de nome de exportação da DLL. <br/>            |
| 2 <br/>  | variável <br/> | Nome <br/> | Uma cadeia de caracteres ASCII que contém o nome a ser importado. Essa é a cadeia de caracteres que deve ser correspondida ao nome público na DLL. Essa cadeia de caracteres diferencia maiúsculas de minúsculas e terminada por um byte nulo. <br/> |
| \* <br/> | 0 ou 1 <br/>   | Pad <br/>  | Um byte de teclado zero à direita que aparece após o byte nulo à direita, se necessário, para alinhar a próxima entrada em um limite par. <br/>                                                        |



 

#### <a name="import-address-table"></a>Importar tabela de endereços

A estrutura e o conteúdo da tabela de endereços de importação são idênticos aos da tabela de pesquisa de importação, até que o arquivo esteja associado. Durante a associação, as entradas na tabela de endereços de importação são substituídas pelos endereços de 32 bits (para PE32) ou 64 bits (para PE32 +) dos símbolos que estão sendo importados. Esses endereços são os endereços de memória reais dos símbolos, embora tecnicamente eles ainda sejam chamados de "endereços virtuais". O carregador normalmente processa a associação.

### <a name="the-pdata-section"></a>A seção. pData

A seção. pData contém uma matriz de entradas de tabela de função que são usadas para manipulação de exceção. Ele é apontado pela entrada da tabela de exceção no diretório de dados de imagem. As entradas devem ser classificadas de acordo com os endereços de função (o primeiro campo em cada estrutura) antes de serem emitidas na imagem final. A plataforma de destino determina quais das três variações de formato de entrada de tabela de função descritas abaixo são usadas.

Para imagens MIPS de 32 bits, as entradas da tabela de funções têm o seguinte formato:



| Deslocamento         | Tamanho          | Campo                          | Descrição                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Endereço inicial <br/>      | O VA da função correspondente. <br/>                              |
| 4 <br/>  | 4 <br/> | Endereço final <br/>        | O VA do final da função. <br/>                                 |
| 8 <br/>  | 4 <br/> | Manipulador de exceção <br/>  | O ponteiro para o manipulador de exceção a ser executado. <br/>               |
| 12 <br/> | 4 <br/> | Dados do manipulador <br/>       | O ponteiro para informações adicionais a serem passadas para o manipulador. <br/> |
| 16 <br/> | 4 <br/> | Endereço final do prólogo <br/> | O VA do final do prólogo da função. <br/>                        |



 

Para as plataformas ARM, PowerPC, SH3 e SH4 Windows CE, as entradas da tabela de funções têm o seguinte formato:



| Deslocamento        | Tamanho                | Campo                       | Descrição                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Endereço inicial <br/>   | O VA da função correspondente. <br/>                                                                         |
| 4 <br/> | 8 bits <br/>  | Comprimento do prólogo <br/>   | O número de instruções no prólogo da função. <br/>                                                          |
| 4 <br/> | 22 bits <br/> | Comprimento da função <br/> | O número de instruções na função. <br/>                                                                   |
| 4 <br/> | 1 bit <br/>   | Sinalizador de 32 bits <br/>     | Se definido, a função consiste em instruções de 32 bits. Se claro, a função consiste em instruções de 16 bits. <br/> |
| 4 <br/> | 1 bit <br/>   | Sinalizador de exceção <br/>  | Se definido, existe um manipulador de exceção para a função. Caso contrário, não existe nenhum manipulador de exceção. <br/>                 |



 

Para plataformas x64 e Itanium, as entradas da tabela de funções têm o seguinte formato:



| Deslocamento        | Tamanho          | Campo                          | Descrição                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Endereço inicial <br/>      | O RVA da função correspondente. <br/> |
| 4 <br/> | 4 <br/> | Endereço final <br/>        | O RVA do final da função. <br/>    |
| 8 <br/> | 4 <br/> | Informações de desenrolamento <br/> | O RVA das informações de desenrolamento. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>A seção. realocação (somente imagem)

A tabela de realocação base contém entradas para todas as realocações de base na imagem. O campo tabela de realocação base nos diretórios de dados de cabeçalho opcionais fornece o número de bytes na tabela de realocação base. Para obter mais informações, consulte [diretórios de dados de cabeçalho opcionais (somente imagem)](#optional-header-data-directories-image-only). A tabela de realocação base é dividida em blocos. Cada bloco representa as realocações de base para uma página de 4K. Cada bloco deve iniciar em um limite de 32 bits.

O carregador não é necessário para processar as relocalidades de base que são resolvidas pelo vinculador, a menos que a imagem de carga não possa ser carregada na base da imagem especificada no cabeçalho PE.

#### <a name="base-relocation-block"></a>Bloco de realocação de base

Cada bloco de realocação de base começa com a seguinte estrutura:



| Deslocamento        | Tamanho          | Campo                  | Descrição                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | RVA da página <br/>   | A imagem base mais a página RVA é adicionada a cada deslocamento para criar o VA em que a realocação de base deve ser aplicada. <br/>                         |
| 4 <br/> | 4 <br/> | Tamanho do bloco <br/> | O número total de bytes no bloco de realocação de base, incluindo os campos RVA da página e tamanho do bloco e os campos tipo/deslocamento a seguir. <br/> |



 

O campo tamanho do bloco é seguido por qualquer número de entradas de campo de tipo ou deslocamento. Cada entrada é uma palavra (2 bytes) e tem a seguinte estrutura:



| Deslocamento        | Tamanho                | Campo              | Descrição                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 bits <br/>  | Tipo <br/>   | Armazenados nos quatro bits superiores da palavra, um valor que indica o tipo de realocação de base a ser aplicado. Para obter mais informações, consulte [base de tipos de realocação](#base-relocation-types).<br/>                         |
| 0 <br/> | 12 bits <br/> | Deslocamento <br/> | Armazenados nos 12 bits restantes da palavra, um deslocamento do endereço inicial que foi especificado no campo RVA da página para o bloco. Esse deslocamento especifica onde a realocação de base deve ser aplicada. <br/> |



 

Para aplicar uma realocação de base, a diferença é calculada entre o endereço base preferencial e a base em que a imagem é realmente carregada. Se a imagem for carregada em sua base preferida, a diferença será zero e, portanto, as realocações básicas não precisarão ser aplicadas.

#### <a name="base-relocation-types"></a>Tipos de realocação base



| Constante                                       | Valor          | Descrição                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ absoluto com base em rel de imagem \_ <br/>        | 0 <br/>  | A realocação de base é ignorada. Esse tipo pode ser usado para preencher um bloco. <br/>                                                                                                                                                                                                                                                 |
| \_ \_ com base em rel de imagem \_ alta <br/>            | 1 <br/>  | A realocação de base adiciona os 16 bits superiores da diferença ao campo de 16 bits no deslocamento. O campo de 16 bits representa o valor alto de uma palavra de 32 bits. <br/>                                                                                                                                                               |
| \_com base em rel. de imagem \_ \_ baixa <br/>             | 2 <br/>  | A realocação de base adiciona os 16 bits baixos da diferença ao campo de 16 bits no deslocamento. O campo de 16 bits representa a metade inferior de uma palavra de 32 bits. <br/>                                                                                                                                                                  |
| \_ \_ HIGHLOW com base em rel de imagem \_ <br/>         | 3 <br/>  | A realocação de base aplica todos os 32 bits da diferença ao campo de 32 bits no deslocamento. <br/>                                                                                                                                                                                                                              |
| \_ \_ HIGHADJ com base em rel de imagem \_ <br/>         | 4 <br/>  | A realocação de base adiciona os 16 bits superiores da diferença ao campo de 16 bits no deslocamento. O campo de 16 bits representa o valor alto de uma palavra de 32 bits. Os 16 bits baixos do valor de 32 bits são armazenados na palavra de 16 bits que segue essa realocação base. Isso significa que essa realocação básica ocupa dois slots. <br/> |
| \_ \_ JMPADDR MIPS baseada em rel \_ de \_ imagem <br/>   | 5 <br/>  | A interpretação de realocação depende do tipo de computador. <br/> Quando o tipo de computador é MIPS, a realocação de base se aplica a uma instrução de salto de MIPS. <br/>                                                                                                                                                    |
| \_ \_ MOV32 ARM baseado em rel \_ de \_ imagem <br/>      | 5 <br/>  | Essa relocação só é significativa quando o tipo de computador é ARM ou Thumb. A realocação de base aplica o endereço de 32 bits de um símbolo em um par de instruções MOVW/MOVT consecutivas. <br/>                                                                                                                                 |
| \_ \_ \_ RISCV HIGH20 com base em rel de imagem \_ <br/>   | 5 <br/>  | Essa relocação só é significativa quando o tipo de computador é RISC-V. A realocação de base aplica-se aos altos 20 bits de um endereço absoluto de 32 bits. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Reservado, deve ser zero. <br/>                                                                                                                                                                                                                                                                                               |
| \_ \_ MOV32 Thumb com base em rel de imagem \_ \_ <br/>    | 7 <br/>  | Essa relocação só é significativa quando o tipo de computador é Thumb. A realocação de base aplica o endereço de 32 bits de um símbolo a um par de instruções MOVW/MOVT consecutivas. <br/>                                                                                                                                            |
| \_ \_ \_ RISCV LOW12I com base em rel de imagem \_ <br/>   | 7 <br/>  | Essa relocação só é significativa quando o tipo de computador é RISC-V. A realocação de base aplica-se aos 12 bits baixos de um endereço absoluto de 32 bits formado em formato de instrução de tipo RISC-V. <br/>                                                                                                                           |
| \_ \_ \_ RISCV LOW12S com base em rel de imagem \_ <br/>   | 8 <br/>  | Essa relocação só é significativa quando o tipo de computador é RISC-V. A realocação de base aplica-se aos 12 bits baixos de um endereço absoluto de 32 bits formado no formato de instrução RISC-V S-Type. <br/>                                                                                                                           |
| \_ \_ JMPADDR16 MIPS baseada em rel \_ de \_ imagem <br/> | 9 <br/>  | A realocação só é significativa quando o tipo de computador é MIPS. A realocação de base se aplica a uma instrução de salto MIPS16. <br/>                                                                                                                                                                                            |
| \_ \_ DIR64 com base em rel de imagem \_ <br/>           | 10 <br/> | A realocação de base aplica a diferença ao campo de 64 bits no deslocamento. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>A seção. TLS

A seção. TLS fornece suporte direto a PE e COFF para o armazenamento local de thread estático (TLS). O TLS é uma classe de armazenamento especial que o Windows dá suporte no, em que um objeto de dados não é uma variável automática (pilha), mas é local para cada thread individual que executa o código. Assim, cada thread pode manter um valor diferente para uma variável declarada usando TLS.

Observe que qualquer quantidade de dados TLS pode ser suportada usando as chamadas de API TlsAlloc, TlsFree, TlsSetValue e TlsGetValue. A implementação de PE ou COFF é uma abordagem alternativa para usar a API e tem a vantagem de ser mais simples do ponto de vista do programador de linguagem de alto nível. Essa implementação permite que os dados TLS sejam definidos e inicializados da mesma forma que as variáveis estáticas comuns em um programa. Por exemplo, no Visual C++, uma variável TLS estática pode ser definida da seguinte maneira, sem usar a API do Windows:

`__declspec (thread) int tlsFlag = 1;`

Para dar suporte a essa construção de programação, a seção PE e COFF. TLS especifica as seguintes informações: dados de inicialização, rotinas de retorno de chamada para a inicialização e encerramento por thread e o índice TLS, que são explicados na discussão a seguir.

> [!Note]
>
> Os objetos de dados TLS declarados estaticamente podem ser usados somente em arquivos de imagem carregados estaticamente. Esse fato torna não confiável usar dados TLS estáticos em uma DLL, a menos que você saiba que a DLL ou qualquer coisa vinculada estaticamente a ela nunca será carregada dinamicamente com a função de API LoadLibrary.

 

O código executável acessa um objeto de dados TLS estático por meio das seguintes etapas:

1.  No momento do link, o vinculador define o endereço do campo de índice do diretório TLS. Esse campo aponta para um local em que o programa espera receber o índice TLS.

    A biblioteca de tempo de execução da Microsoft facilita esse processo definindo uma imagem de memória do diretório TLS e dando a ela o nome especial " \_ \_ TLS \_ usado" (plataformas Intel x86) ou " \_ TLS \_ usado" (outras plataformas). O vinculador procura essa imagem de memória e usa os dados ali para criar o diretório TLS. Outros compiladores que dão suporte a TLS e trabalham com o vinculador da Microsoft devem usar essa mesma técnica.

2.  Quando um thread é criado, o carregador comunica o endereço da matriz TLS do thread, colocando o endereço do bloco de ambiente de thread (TEB) no registro FS. Um ponteiro para a matriz TLS está no deslocamento de 0x2C do início de TEB. Esse comportamento é específico do Intel x86.

3.  O carregador atribui o valor do índice TLS ao local indicado pelo endereço do campo de índice.

4.  O código executável recupera o índice TLS e também o local da matriz TLS.

5.  O código usa o índice TLS e o local da matriz TLS (multiplicando o índice por 4 e usando-o como um deslocamento para a matriz) para obter o endereço da área de dados TLS para o programa e o módulo especificados. Cada thread tem sua própria área de dados TLS, mas isso é transparente para o programa, que não precisa saber como os dados são alocados para threads individuais.

6.  Um objeto de dados TLS individual é acessado como um deslocamento fixo na área de dados TLS.

A matriz TLS é uma matriz de endereços que o sistema mantém para cada thread. Cada endereço nessa matriz fornece o local dos dados TLS para um determinado módulo (EXE ou DLL) dentro do programa. O índice TLS indica qual membro da matriz deve ser usado. O índice é um número (significativo somente para o sistema) que identifica o módulo.

#### <a name="the-tls-directory"></a>O diretório TLS

O diretório TLS tem o seguinte formato:



| Deslocamento (PE32/PE32 +) | Tamanho (PE32/PE32 +) | Campo                            | Descrição                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Início de dados brutos VA <br/>    | O endereço inicial do modelo TLS. O modelo é um bloco de dados que é usado para inicializar dados TLS. O sistema copia todos esses dados sempre que um thread é criado, portanto, ele não deve estar corrompido. Observe que esse endereço não é um RVA; é um endereço para o qual deve haver uma realocação base na seção. realocação. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | VA final de dados brutos <br/>      | O endereço do último byte do TLS, exceto para o preenchimento zero. Assim como no campo data de início do VA, esse é um VA, não um RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Endereço do índice <br/>     | O local para receber o índice TLS, que o carregador atribui. Esse local está em uma seção de dados comum, portanto, pode receber um nome simbólico acessível ao programa. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Endereço de retornos de chamada <br/> | O ponteiro para uma matriz de funções de retorno de chamada TLS. A matriz é terminada em nulo, portanto, se não houver suporte para nenhuma função de retorno de chamada, esse campo apontará para 4 bytes definido como zero. Para obter informações sobre o protótipo para essas funções, consulte [funções de retorno de chamada de TLS](#tls-callback-functions).<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Tamanho do preenchimento zero <br/>    | O tamanho em bytes do modelo, além dos dados inicializados, delimitados pelos campos VA data de início e data final brutos de dados brutos. O tamanho total do modelo deve ser igual ao tamanho total dos dados TLS no arquivo de imagem. O preenchimento zero é a quantidade de dados que vem após os dados inicializados sem zero. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Características <br/>      | Os quatro bits \[ 23:20 \] descrevem as informações de alinhamento. Os valores possíveis são aqueles definidos como \_ \_ alinhamento \_ \* de SCN de imagem, que também são usados para descrever o alinhamento da seção em arquivos de objeto. Os outros 28 bits são reservados para uso futuro. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>Funções de retorno de chamada TLS

O programa pode fornecer uma ou mais funções de retorno de chamada TLS para dar suporte à inicialização e terminação adicionais para objetos de dados TLS. Um uso típico para tal função de retorno de chamada seria chamar construtores e destruidores para objetos.

Embora normalmente não haja mais de uma função de retorno de chamada, um retorno de chamada é implementado como uma matriz para possibilitar a adição de funções de retorno de chamada adicionais, se desejado. Se houver mais de uma função de retorno de chamada, cada função será chamada na ordem em que seu endereço aparece na matriz. Um ponteiro nulo encerra a matriz. É perfeitamente válido ter uma lista vazia (nenhum retorno de chamada com suporte); nesse caso, a matriz de retorno de chamada tem exatamente um membro-um ponteiro nulo.

O protótipo de uma função de retorno de chamada (apontado por um ponteiro do tipo \_ retorno de chamada PIMAGE TLS \_ ) tem os mesmos parâmetros que uma função de ponto de entrada de dll:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



O parâmetro reservado deve ser definido como zero. O parâmetro Reason pode assumir os seguintes valores:



| Configuração                          | Valor         | Descrição                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| \_anexar processo de dll \_ <br/> | 1 <br/> | Um novo processo foi iniciado, incluindo o primeiro thread. <br/>                                   |
| \_anexação de thread de dll \_ <br/>  | 2 <br/> | Um novo thread foi criado. Essa notificação é enviada para todos, exceto para o primeiro thread. <br/>      |
| desanexação de thread de DLL \_ \_ <br/>  | 3 <br/> | Um thread está prestes a ser encerrado. Essa notificação é enviada para todos, exceto para o primeiro thread. <br/> |
| desanexar processo de DLL \_ \_ <br/> | 0 <br/> | Um processo está prestes a terminar, incluindo o thread original. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>A estrutura de configuração de carregamento (somente imagem)

A estrutura de configuração de carregamento (diretório de configuração de carregamento de imagem \_ \_ \_ ) foi usada anteriormente em casos muito limitados no próprio sistema operacional Windows NT para descrever vários recursos muito difíceis ou muito grandes para descrever no cabeçalho do arquivo ou no cabeçalho opcional da imagem. As versões atuais do Microsoft linker e do Windows XP e versões posteriores do Windows usam uma nova versão desta estrutura para sistemas baseados em x86 de 32 bits que incluem a tecnologia SEH reservada. Isso fornece uma lista de manipuladores de exceção estruturados seguros que o sistema operacional usa durante a expedição de exceção. Se o endereço do manipulador residir no intervalo de VA da imagem e estiver marcado como reconhecimento de SEH reservado (ou seja, a imagem \_ DLLCHARACTERISTICS \_ nenhum \_ Seh está clara no campo DLLCHARACTERISTICS do cabeçalho opcional, conforme descrito anteriormente), o manipulador deverá estar na lista de manipuladores confiáveis conhecidos para essa imagem. Caso contrário, o sistema operacional encerrará o aplicativo. Isso ajuda a evitar a exploração de "seqüestro de manipulador de exceção x86" que foi usada no passado para assumir o controle do sistema operacional.

O Microsoft linker fornece automaticamente uma estrutura de configuração de carregamento padrão para incluir os dados de SEH reservados. Se o código de usuário já fornecer uma estrutura de configuração de carregamento, ele deverá incluir os novos campos de SEH reservados. Caso contrário, o vinculador não poderá incluir os dados SEH reservados e a imagem não será marcada como contendo SEH reservado.

#### <a name="load-configuration-directory"></a>Carregar diretório de configuração

A entrada do diretório de dados para uma estrutura de configuração de carga SEH semireservada deve especificar um tamanho específico da estrutura de configuração de carga porque o carregador do sistema operacional sempre espera que seja um determinado valor. Nesse sentido, o tamanho é, na verdade, apenas uma verificação de versão. Para compatibilidade com o Windows XP e versões anteriores do Windows, o tamanho deve ser 64 para imagens x86.

#### <a name="load-configuration-layout"></a>Carregar layout de configuração

A estrutura de configuração de carregamento tem o seguinte layout para arquivos PE de 32 bits e de 64 bits:



| Deslocamento              | Tamanho            | Campo                                      | Descrição                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Características <br/>                | Sinalizadores que indicam os atributos do arquivo, atualmente não utilizados. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Valor de carimbo de data e hora. O valor é representado no número de segundos decorridos desde a meia-noite (00:00:00), 1º de janeiro de 1970, horário coordenado universal, de acordo com o relógio do sistema. O carimbo de data/hora pode ser impresso usando a função de tempo C Runtime (CRT). <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Número de versão principal. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Número de versão secundária. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Os sinalizadores do carregador global a serem desmarcados para esse processo, pois o carregador inicia o processo. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Os sinalizadores do carregador global a serem definidos para esse processo como o carregador inicia o processo. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | O valor de tempo limite padrão a ser usado para as seções críticas do processo que são abandonadas. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Memória que deve ser liberada antes de ser retornada ao sistema, em bytes. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Quantidade total de memória livre, em bytes. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[x86 apenas \] o VA de uma lista de endereços em que o prefixo de bloqueio é usado para que eles possam ser substituídos por Nop em máquinas de processador único. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Tamanho máximo de alocação, em bytes. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Tamanho máximo da memória virtual, em bytes. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | Definir esse campo como um valor diferente de zero é equivalente a chamar SetProcessAffinityMask com esse valor durante a inicialização do processo (somente. exe) <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Processar sinalizadores de heap que correspondem ao primeiro argumento da função HeapCreate. Esses sinalizadores se aplicam ao heap de processo que é criado durante a inicialização do processo. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | O identificador da versão service pack. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Reservado <br/>                       | Deve ser zero. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | Editarlist <br/>                       | Reservado para uso pelo sistema. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Um ponteiro para um cookie que é usado pela implementação de Visual C++ ou GS. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[x86 apenas \] o VA da tabela classificada de RVAs de cada manipulador se válido e exclusivo na imagem. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[x86 apenas \] a contagem de manipuladores exclusivos na tabela. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | O VA em que o ponteiro de função de verificação de proteção do fluxo de controle é armazenado. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | O VA em que o ponteiro de função de expedição da proteção de fluxo de controle é armazenado. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | O VA da tabela classificada de RVAs de cada função de proteção de fluxo de controle na imagem. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | A contagem de RVAs exclusivos na tabela acima. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | Sinalizadores relacionados à proteção do fluxo de controle. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Informações de integridade do código. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | O VA em que o endereço de proteção de fluxo de controle obtido na tabela IAT é armazenado. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | A contagem de RVAs exclusivos na tabela acima. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | O VA em que a tabela de destino de salto longo de proteção de fluxo de controle é armazenada. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | A contagem de RVAs exclusivos na tabela acima. <br/>                                                                                                                                                                                                                                    |



 

O campo GuardFlags contém uma combinação de um ou mais dos seguintes sinalizadores e subcampos:

-   O módulo executa verificações de integridade de fluxo de controle usando o suporte fornecido pelo sistema.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   O módulo executa o fluxo de controle e as verificações de integridade de gravação.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   O módulo contém metadados de destino de fluxo de controle válidos.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   O módulo não faz uso do cookie de segurança/GS.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   O módulo dá suporte à carga de atraso somente leitura IAT.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   DELAYLOAD importar tabela em sua própria seção. didat (com nada mais nele) que pode ser protegida livremente.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   O módulo contém informações de exportação suprimidas. Isso também infere que o endereço obtido pela tabela IAT também está presente na configuração de carga.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   O módulo permite a supressão de exportações.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   O módulo contém informações de destino do longjmp.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Máscara do subcampo que contém o stride das entradas da tabela da função de proteção do fluxo de controle (ou seja, a contagem adicional de bytes por entrada de tabela).

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Além disso, o cabeçalho SDK do Windows Winnt. h define essa macro para a quantidade de bits a fim de deslocar o valor GuardFlags para justificar à direita a função de proteção de fluxo de controle Stride da tabela:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>A seção. rsrc

Os recursos são indexados por uma estrutura de árvore com classificação binária de vários níveis. O design geral pode incorporar 2 \* \* 31 níveis. Por convenção, no entanto, o Windows usa três níveis:

<dl> Tipo  
Nome  
Idioma  
</dl>

Uma série de tabelas de diretório de recursos relaciona todos os níveis da seguinte maneira: cada tabela de diretório é seguida por uma série de entradas de diretório que fornecem o nome ou identificador (ID) para esse nível (tipo, nome ou nível de linguagem) e um endereço de uma descrição de dados ou outra tabela de diretório. Se o endereço apontar para uma descrição de dados, os dados serão uma folha na árvore. Se o endereço apontar para outra tabela de diretório, essa tabela listará as entradas de diretório no próximo nível abaixo.

O tipo, o nome e as IDs de idioma de uma folha são determinados pelo caminho que é usado pelas tabelas de diretório para alcançar a folha. A primeira tabela determina a ID de tipo, a segunda tabela (apontada pela entrada de diretório na primeira tabela) determina a ID de nome e a terceira tabela determina a ID de idioma.

A estrutura geral da seção. rsrc é:



| Dados                                                                   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tabelas de diretório de recursos (e entradas de diretório de recursos) <br/> | Uma série de tabelas, uma para cada grupo de nós na árvore. Todos os nós de nível superior (tipo) são listados na primeira tabela. As entradas nesta tabela apontam para tabelas de segundo nível. Cada árvore de segundo nível tem a mesma ID de tipo, mas IDs de nome diferentes. Árvores de terceiro nível têm o mesmo tipo e IDs de nome, mas IDs de idioma diferentes. <br/> Cada tabela individual é imediatamente seguida por entradas de diretório, nas quais cada entrada tem um nome ou identificador numérico e um ponteiro para uma descrição de dados ou uma tabela no nível inferior seguinte. <br/> |
| Cadeias de caracteres do diretório de recursos <br/>                                 | Cadeias de caracteres Unicode alinhadas em dois bytes, que servem como dados de cadeias apontados por entradas de diretório. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Descrição dos dados do recurso <br/>                                  | Uma matriz de registros, apontada por tabelas, que descreve o tamanho real e o local dos dados do recurso. Esses registros são as folhas na árvore de descrição de recursos. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Dados de recurso <br/>                                              | Dados brutos da seção de recursos. As informações de tamanho e local no campo descrições de dados de recurso delimitam as regiões individuais dos dados do recurso. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Tabela de diretório de recursos

Cada tabela de diretório de recursos tem o formato a seguir. Essa estrutura de dados deve ser considerada o título de uma tabela porque a tabela realmente consiste em entradas de diretório (descritas na seção 6.9.2, "entradas do diretório de recursos") e esta estrutura:



| Deslocamento         | Tamanho          | Campo                              | Descrição                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Características <br/>        | Sinalizadores de recurso. Este campo é reservado para uso futuro. Ele está definido como zero no momento. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Carimbo de data/hora <br/>        | A hora em que os dados de recurso foram criados pelo compilador de recurso. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Versão Principal <br/>          | O número de versão principal, definido pelo usuário. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Versão Secundária <br/>          | O número de versão secundária, definido pelo usuário. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Número de entradas de nome <br/> | O número de entradas de diretório imediatamente após a tabela que usam cadeias de caracteres para identificar entradas de tipo, nome ou idioma (dependendo do nível da tabela). <br/> |
| 14 <br/> | 2 <br/> | Número de entradas de ID <br/>   | O número de entradas de diretório imediatamente após as entradas de nome que usam IDs numéricas para entradas de tipo, nome ou idioma. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Entradas do diretório de recursos

As entradas de diretório compõem as linhas de uma tabela. Cada entrada do diretório de recursos tem o formato a seguir. Se a entrada é um nome ou uma entrada de ID é indicada pela tabela de diretório de recursos, que indica quantas entradas de nome e ID são seguidas (Lembre-se de que todas as entradas de nome precedem todas as entradas de ID da tabela). Todas as entradas da tabela são classificadas em ordem crescente: as entradas de nome por cadeia de caracteres que diferencia maiúsculas de minúsculas e as entradas de ID por valor numérico. Os deslocamentos são relativos ao endereço na entrada do \_ diretório de imagem \_ \_ DataDirectory de recursos. Consulte [emparelhamento dentro do PE: um tour do formato de arquivo executável portátil do Win32](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) para obter mais informações.



| Deslocamento        | Tamanho          | Campo                           | Descrição                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Deslocamento de nome <br/>         | O deslocamento de uma cadeia de caracteres que fornece o tipo, o nome ou a entrada de ID de idioma, dependendo do nível da tabela. <br/>     |
| 0 <br/> | 4 <br/> | ID de inteiro <br/>          | Um inteiro de 32 bits que identifica o tipo, o nome ou a entrada de ID de idioma. <br/>                                   |
| 4 <br/> | 4 <br/> | Deslocamento de entrada de dados <br/>   | Alto bit 0. Endereço de uma entrada de dados de recurso (uma folha). <br/>                                                   |
| 4 <br/> | 4 <br/> | Deslocamento de subdiretório <br/> | Alto bit 1. Os 31 bits inferiores são o endereço de outra tabela de diretório de recursos (o próximo nível abaixo). <br/> |



 

#### <a name="resource-directory-string"></a>Cadeia de caracteres do diretório de recursos

A área de cadeia do diretório de recursos consiste em cadeias de caracteres Unicode, que são alinhadas ao Word. Essas cadeias de caracteres são armazenadas juntas após a última entrada do diretório de recursos e antes da primeira entrada de dados do recurso. Isso minimiza o impacto dessas cadeias de caracteres de comprimento variável no alinhamento das entradas de diretório de tamanho fixo. Cada cadeia de caracteres do diretório de recursos tem o seguinte formato:



| Deslocamento        | Tamanho                 | Campo                      | Descrição                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Comprimento <br/>         | O tamanho da cadeia de caracteres, não incluindo o próprio campo de comprimento. <br/> |
| 2 <br/> | variável <br/> | Cadeia de caracteres Unicode <br/> | Os dados de cadeia de caracteres Unicode de comprimento variável, alinhados por palavra. <br/>     |



 

#### <a name="resource-data-entry"></a>Entrada de dados do recurso

Cada entrada de dados de recurso descreve uma unidade real de dados brutos na área de dados do recurso. Uma entrada de dados de recurso tem o seguinte formato:



| Deslocamento         | Tamanho          | Campo                            | Descrição                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | RVA de dados <br/>             | O endereço de uma unidade de dados de recurso na área de dados do recurso. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Tamanho <br/>                 | O tamanho, em bytes, dos dados de recurso que é apontado pelo campo RVA de dados. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | A página de código usada para decodificar valores de ponto de código dentro dos dados do recurso. Normalmente, a página de código seria a página de código Unicode. <br/> |
| 12 <br/> | 4 <br/> | Reservado, deve ser 0. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>A seção. cormeta (somente objeto)

Os metadados CLR são armazenados nesta seção. Ele é usado para indicar que o arquivo de objeto contém código gerenciado. O formato dos metadados não é documentado, mas pode ser enviado para as interfaces CLR para lidar com metadados.

### <a name="the-sxdata-section"></a>A seção. sxdata

Os manipuladores de exceção válidos de um objeto são listados na seção **. sxdata** desse objeto. A seção está marcada como IMAGE \_ SCN \_ lnk \_ info. Ele contém o índice de símbolo COFF de cada manipulador válido, usando 4 bytes por índice.

Além disso, o compilador marca um objeto COFF como SEH registrado emitindo o símbolo absoluto " @feat.00 " com o LSB do campo de valor definido como 1. Um objeto COFF sem manipuladores SEH registrados teria o @feat.00 símbolo "", mas não **. sxdata** seção.

## <a name="archive-library-file-format"></a>Formato de arquivo de arquivamento (biblioteca)

- [Assinatura de arquivo morto](#archive-file-signature)
- [Arquivar cabeçalhos de membro](#archive-member-headers)
- [Primeiro membro do vinculador](#first-linker-member)
- [Segundo membro do vinculador](#second-linker-member)
- [Membro longnames](#longnames-member)

O formato de arquivo COFF fornece um mecanismo padrão para armazenar coleções de arquivos de objeto. Essas coleções são normalmente chamadas de bibliotecas na documentação de programação.

Os primeiros 8 bytes de um arquivo consistem na assinatura do arquivo. O restante do arquivo consiste em uma série de membros de arquivamento, da seguinte maneira:

-   O primeiro e o segundo Membros são "membros do vinculador". Cada um desses membros tem seu próprio formato, conforme descrito em seção [tipo de nome de importação](#import-name-type). Normalmente, um vinculador coloca informações nesses membros de arquivamento. Os membros do vinculador contêm o diretório do arquivo morto.

-   O terceiro membro é o membro "longnames". Esse membro consiste em uma série de cadeias de caracteres ASCII com terminação nula, nas quais cada cadeia de caracteres é o nome de outro membro de arquivo.

-   O restante do arquivo consiste em membros padrão (arquivo de objeto). Cada um desses membros contém o conteúdo de um arquivo de objeto em sua totalidade.

Um cabeçalho de membro de arquivo precede cada membro. A lista a seguir mostra a estrutura geral de um arquivo morto:

-   Assinatura: "! &lt; Arch &gt; \\ n "
-   parâmetro

    <dl> primeiro membro do vinculador  
    </dl>

-   parâmetro

    <dl> 2º membro do vinculador  
    </dl>

-   parâmetro

    <dl> Membro longnames  
    </dl>

-   parâmetro

    <dl> Conteúdo do arquivo OBJ 1  
    (Formato COFF)  
    </dl>

-   parâmetro

    <dl> Conteúdo do arquivo OBJ 2  
    (Formato COFF)  
    </dl>

### <a name="archive-file-signature"></a>Assinatura de arquivo morto

A assinatura do arquivo morto identifica o tipo de arquivo. Qualquer utilitário (por exemplo, um vinculador) que usa um arquivo morto como entrada pode verificar o tipo de arquivo lendo essa assinatura. A assinatura consiste nos seguintes caracteres ASCII, nos quais cada caractere abaixo é representado literalmente, exceto pelo caractere de nova linha ( \\ n):

`!<arch>\n`

### <a name="archive-member-headers"></a>Arquivar cabeçalhos de membro

Cada membro (vinculador, longonames ou membro de arquivo de objeto) é precedido por um cabeçalho. Um cabeçalho de membro de arquivo tem o seguinte formato, no qual cada campo é uma cadeia de caracteres de texto ASCII que é justificada à esquerda e preenchida com espaços no final do campo. Não há nenhum caractere nulo de encerramento em nenhum desses campos.

Cada cabeçalho de membro começa no primeiro endereço par após o final do membro de arquivo anterior.



| Deslocamento         | Tamanho           | Campo                     | Descrição                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Nome <br/>          | O nome do membro de arquivo, com uma barra (/) anexada para encerrar o nome. Se o primeiro caractere for uma barra, o nome terá uma interpretação especial, conforme descrito na tabela a seguir. <br/> |
| 16 <br/> | 12 <br/> | Data <br/>          | A data e a hora em que o membro de arquivo foi criado: esta é a representação decimal ASCII do número de segundos desde 1/1/1970 UCT. <br/>                                                    |
| 28 <br/> | 6 <br/>  | ID do Usuário <br/>       | Uma representação decimal ASCII da ID de usuário. Esse campo não contém um valor significativo em plataformas do Windows porque as ferramentas da Microsoft emitem todos os espaços em branco. <br/>                                    |
| 34 <br/> | 6 <br/>  | ID do Grupo <br/>      | Uma representação decimal ASCII da ID do grupo. Esse campo não contém um valor significativo em plataformas do Windows porque as ferramentas da Microsoft emitem todos os espaços em branco. <br/>                                   |
| 40 <br/> | 8 <br/>  | Mode <br/>          | Uma representação octal ASCII do modo de arquivo do membro. Esse é o \_ valor do modo St da função de tempo de execução C \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Tamanho <br/>          | Uma representação decimal ASCII do tamanho total do membro de arquivo morto, sem incluir o tamanho do cabeçalho. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Fim do cabeçalho <br/> | Os dois bytes na cadeia de caracteres C "̃ \\ n" (0X60 0x0A). <br/>                                                                                                                                               |



 

O campo nome tem um dos formatos mostrados na tabela a seguir. Como mencionado anteriormente, cada uma dessas cadeias de caracteres é justificada à esquerda e preenchida com espaços à direita dentro de um campo de 16 bytes:



| Conteúdo do campo nome | Description                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nomes <br/>      | O nome do membro de arquivo morto. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | O membro de arquivo morto é um dos dois membros do vinculador. Ambos os membros do vinculador têm esse nome. <br/>                                                                                                                                                                                          |
| // <br/>         | O membro de arquivo é o membro longnames, que consiste em uma série de cadeias de caracteres ASCII com terminação nula. O membro longnames é o terceiro membro de arquivo morto e deve estar sempre presente mesmo se o conteúdo estiver vazio. <br/>                                                                     |
| /n <br/>         | O nome do membro de arquivo está localizado no deslocamento n dentro do membro longnames. O número n é a representação decimal do deslocamento. Por exemplo: "/26" indica que o nome do membro de arquivo está localizado 26 bytes além do início do conteúdo do membro de longnames. <br/> |



 

### <a name="first-linker-member"></a>Primeiro membro do vinculador

O nome do primeiro membro do vinculador é "/". O primeiro membro do vinculador está incluído para compatibilidade com versões anteriores. Ele não é usado por vinculadores atuais, mas seu formato deve estar correto. Esse membro do vinculador fornece um diretório de nomes de símbolo, assim como o segundo membro do vinculador. Para cada símbolo, as informações indicam onde encontrar o membro de arquivo que contém o símbolo.

O primeiro membro do vinculador tem o formato a seguir. Essas informações são exibidas após o cabeçalho:



| Deslocamento         | Tamanho               | Campo                         | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Número de símbolos <br/> | O Long sem sinal que contém o número de símbolos indexados. Esse número é armazenado no formato big-endian. Cada membro do arquivo de objeto normalmente define um ou mais símbolos externos. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Deslocamentos <br/>           | Uma matriz de deslocamentos de arquivo para arquivar cabeçalhos de membro, em que n é igual ao campo número de símbolos. Cada número na matriz é um Long não assinado armazenado no formato big endian. Para cada símbolo que é nomeado na tabela de cadeia de caracteres, o elemento correspondente na matriz de deslocamentos fornece o local do membro de arquivo que contém o símbolo. <br/> |
| \* <br/> | \* <br/>     | Tabela de cadeias de caracteres <br/>      | Uma série de cadeias de caracteres terminadas em nulo que nomeiem todos os símbolos no diretório. Cada cadeia de caracteres começa imediatamente após o caractere nulo na cadeia de caracteres anterior. O número de cadeias de caracteres deve ser igual ao valor do campo número de símbolos. <br/>                                                                                                       |



 

Os elementos na matriz de deslocamentos devem ser organizados em ordem crescente. Esse fato significa que os símbolos na tabela de cadeia de caracteres devem ser organizados de acordo com a ordem dos membros de arquivamento. Por exemplo, todos os símbolos no primeiro membro do arquivo de objeto teriam que ser listados antes dos símbolos no segundo arquivo de objeto.

### <a name="second-linker-member"></a>Segundo membro do vinculador

O segundo membro do vinculador tem o nome "/" como o primeiro membro do vinculador. Embora ambos os membros do vinculador forneçam um diretório de símbolos e membros de arquivo que os contêm, o segundo membro do vinculador é usado em preferência ao primeiro por todos os vinculadores atuais. O segundo membro do vinculador inclui nomes de símbolo na ordem lexical, o que permite uma pesquisa mais rápida por nome.

O segundo membro tem o formato a seguir. Essas informações são exibidas após o cabeçalho:



| Deslocamento         | Tamanho               | Campo                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Número de membros <br/> | Um Long sem sinal que contém o número de membros de arquivo. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Deslocamentos <br/>           | Uma matriz de deslocamentos de arquivo para arquivar cabeçalhos de membro, organizados em ordem crescente. Cada deslocamento é um longo não assinado. O número m é igual ao valor do campo número de membros. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Número de símbolos <br/> | Um Long sem sinal que contém o número de símbolos indexados. Cada membro do arquivo de objeto normalmente define um ou mais símbolos externos. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Índices <br/>           | Uma matriz de índices baseados em 1 (sem sinal curto) que mapeia nomes de símbolos para arquivar deslocamentos de membro. O número n é igual ao número de símbolos do campo. Para cada símbolo que é nomeado na tabela de cadeia de caracteres, o elemento correspondente na matriz de índices fornece um índice para a matriz de deslocamentos. A matriz de deslocamentos, por sua vez, fornece o local do membro de arquivo que contém o símbolo. <br/> |
| \* <br/> | \* <br/>     | Tabela de cadeias de caracteres <br/>      | Uma série de cadeias de caracteres terminadas em nulo que nomeiem todos os símbolos no diretório. Cada cadeia de caracteres começa imediatamente após o byte nulo na cadeia de caracteres anterior. O número de cadeias de caracteres deve ser igual ao valor do campo número de símbolos. Esta tabela lista todos os nomes de símbolo em ordem lexical crescente. <br/>                                                                             |



 

### <a name="longnames-member"></a>Membro longnames

O nome do membro longnames é "//". O membro longnames é uma série de cadeias de caracteres de nomes de membro de arquivo. Um nome aparece aqui somente quando não há espaço suficiente no campo nome (16 bytes). O membro longnames é opcional. Ele pode estar vazio com apenas um cabeçalho ou pode estar completamente ausente sem até mesmo um cabeçalho.

As cadeias de caracteres são terminadas em nulo. Cada cadeia de caracteres começa imediatamente após o byte nulo na cadeia de caracteres anterior.

## <a name="import-library-format"></a>Importar formato de biblioteca

- [Importar cabeçalho](#import-header)
- [Tipo de importação](#import-type)

Bibliotecas de importação tradicionais, ou seja, bibliotecas que descrevem as exportações de uma imagem para uso por outra, normalmente seguem o layout descrito na seção 7, [formato de arquivo morto (biblioteca)](#archive-library-file-format). A principal diferença é que os membros da biblioteca de importação contêm arquivos pseudo-objeto em vez de verdadeiros, em que cada membro inclui as contribuições de seção necessárias para criar as tabelas de importação que são descritas na seção 6,4, [a seção. iData](#the-idata-section) o vinculador gera esse arquivo ao compilar o aplicativo de exportação.

As contribuições de seção para uma importação podem ser inferidas de um pequeno conjunto de informações. O vinculador pode gerar as informações completas e detalhadas na biblioteca de importação para cada membro no momento da criação da biblioteca ou gravar apenas as informações canônicas na biblioteca e permitir que o aplicativo que o usa posteriormente gere os dados necessários em tempo real.

Em uma biblioteca de importação com o formato longo, um único membro contém as seguintes informações:

<dl> Cabeçalho de membro de arquivo  
Cabeçalho do arquivo  
Cabeçalhos de seção  
Dados que correspondem a cada um dos cabeçalhos de seção  
Tabela de símbolos COFF  
Cadeias de caracteres  
  
</dl>

Por outro lado, uma biblioteca de importação curta é escrita da seguinte maneira:

<dl> Cabeçalho de membro de arquivo  
Importar cabeçalho  
Cadeia de nome de importação terminada em nulo  
Cadeia de caracteres de nome de DLL terminada em nulo  
</dl>

Essas são informações suficientes para reconstruir com precisão todo o conteúdo do membro no momento de seu uso.

### <a name="import-header"></a>Importar cabeçalho

O cabeçalho de importação contém os seguintes campos e deslocamentos:



| Deslocamento         | Tamanho                | Campo                       | Descrição                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | O computador do arquivo de imagem deve ser \_ \_ \_ desconhecido. Para obter mais informações, consulte [tipos de máquina](#machine-types). <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Deve ser 0xFFFF. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Versão <br/>         | A versão da estrutura. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Computador <br/>         | O número que identifica o tipo de computador de destino. Para obter mais informações, consulte [tipos de máquina](#machine-types).<br/> |
| 8 <br/>  | 4 <br/>       | Carimbo de Time-Date <br/> | A hora e a data em que o arquivo foi criado. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Tamanho dos dados <br/>    | O tamanho das cadeias de caracteres que seguem o cabeçalho. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinal/dica <br/>    | O ordinal ou a dica para a importação, determinado pelo valor no campo tipo de nome. <br/>                   |
| 18 <br/> | 2 bits <br/>  | Tipo <br/>            | O tipo de importação. Para obter valores e descrições específicas, consulte [tipo de importação](#import-type).<br/>                           |
|                | 3 bits <br/>  | Tipo de nome <br/>       | O tipo de nome de importação. Para obter mais informações, consulte [importar tipo de nome](#import-name-type). <br/>                           |
|                | 11 bits <br/> | Reservado <br/>        | Reservado, deve ser 0. <br/>                                                                                             |



 

Essa estrutura é seguida por duas cadeias de caracteres terminadas em nulo que descrevem o nome do símbolo importado e a DLL da qual ele veio.

### <a name="import-type"></a>Tipo de importação

Os valores a seguir são definidos para o campo de tipo no cabeçalho de importação:

| Constante                  | Valor         | Descrição                                      |
|---------------------------|---------------|--------------------------------------------------|
| IMPORTAR \_ código <br/>  | 0 <br/> | Código executável. <br/>                     |
| IMPORTAR \_ dados <br/>  | 1 <br/> | Dados. <br/>                                |
| IMPORTAR \_ const <br/> | 2 <br/> | Especificado como CONST no arquivo. def. <br/> |

Esses valores são usados para determinar quais contribuições de seção devem ser geradas pela ferramenta que usa a biblioteca se ela precisar acessar esses dados.

### <a name="import-name-type"></a>Tipo de nome de importação

O nome do símbolo de importação terminada em nulo imediatamente segue seu cabeçalho de importação associado. Os valores a seguir são definidos para o campo de tipo de nome no cabeçalho de importação. Eles indicam como o nome deve ser usado para gerar os símbolos corretos que representam a importação:

| Constante | Valor | Descrição |
| - | - | - |
| IMPORTAR \_ ORDINAL | 0 | A importação é por ordinal. Isso indica que o valor no campo ordinal/dica do cabeçalho de importação é o ordinal da importação. Se essa constante não for especificada, o campo ordinal/Hint sempre deverá ser interpretado como a dica da importação. |
| nome da importação \_ | 1 | O nome da importação é idêntico ao nome do símbolo público. |
| nome de importação \_ \_ NoPrefix | 2 | O nome da importação é o nome do símbolo público, mas ignorando a entrelinha?, @ ou, opcionalmente \_ . |
| IMPORTAR \_ nome \_ desdecorado | 3 | O nome da importação é o nome do símbolo público, mas ignorando a entrelinha?, @ ou, opcionalmente \_ , e truncando no primeiro @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Apêndice A: calculando o hash de imagem do Authenticode PE

- [O que é um hash de imagem Authenticode do PE?](#what-is-an-authenticode-pe-image-hash)
- [O que é abordado em um hash de imagem do Authenticode PE?](#what-is-covered-in-an-authenticode-pe-image-hash)

Espera-se que vários certificados de atributo sejam usados para verificar a integridade das imagens. No entanto, o mais comum é a assinatura Authenticode. Uma assinatura Authenticode pode ser usada para verificar se as seções relevantes de um arquivo de imagem PE não foram alteradas de nenhuma forma a partir do formulário original do arquivo. Para realizar essa tarefa, as assinaturas Authenticode contêm algo chamado de hash de imagem PE

### <a name="what-is-an-authenticode-pe-image-hash"></a>O que é um hash de imagem Authenticode do PE?

O hash de imagem do PE do Authenticode, ou hash de arquivo para curto, é semelhante a uma soma de verificação de arquivo, pois produz um valor pequeno que se relaciona com a integridade de um arquivo. Uma soma de verificação é produzida por um algoritmo simples e é usada principalmente para detectar falhas de memória. Ou seja, ele é usado para detectar se um bloco de memória em disco ficou insatisfatório e os valores armazenados ali foram corrompidos. Um hash de arquivo é semelhante a uma soma de verificação, pois ele também detecta corrupção de arquivo. No entanto, ao contrário da maioria dos algoritmos de soma de verificação, é muito difícil modificar um arquivo para que ele tenha o mesmo hash de arquivo que seu formulário original (não modificado). Ou seja, uma soma de verificação destina-se a detectar falhas de memória simples que levam a danos, mas um hash de arquivo pode ser usado para detectar modificações intencionais e até mesmo sutis em um arquivo, como aqueles introduzidos por vírus, hackers ou programas de cavalo de Troia.

Em uma assinatura Authenticode, o hash de arquivo é assinado digitalmente usando uma chave privada conhecida somente pelo signatário do arquivo. Um consumidor de software pode verificar a integridade do arquivo calculando o valor de hash do arquivo e comparando-o com o valor do hash assinado contido na assinatura digital Authenticode. Se os hashes de arquivo não corresponderem, parte do arquivo coberto pelo hash de imagem PE foi modificada.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>O que é abordado em um hash de imagem do Authenticode PE?

Não é possível ou desejável incluir todos os dados de arquivo de imagem no cálculo do hash de imagem PE. Às vezes, ele simplesmente apresenta características indesejáveis (por exemplo, as informações de depuração não podem ser removidas dos arquivos lançados publicamente); às vezes, é simplesmente impossível. Por exemplo, não é possível incluir todas as informações em um arquivo de imagem em uma assinatura Authenticode, em seguida, inserir a assinatura Authenticode que contém o hash de imagem PE na imagem PE e, posteriormente, ser capaz de gerar um hash de imagem PE idêntico incluindo todos os dados do arquivo de imagem no cálculo novamente, porque o arquivo agora contém a assinatura Authenticode que não estava originalmente lá.

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Processo para gerar o hash de imagem do Authenticode PE

Esta seção descreve como um hash de imagem PE é calculado e quais partes da imagem PE podem ser modificadas sem invalidar a assinatura Authenticode.

> [!NOTE]
> O hash de imagem PE para um arquivo específico pode ser incluído em um arquivo de catálogo separado sem incluir um certificado de atributo dentro do arquivo com hash. Isso é relevante, pois torna-se possível invalidar o hash de imagem PE em um arquivo de catálogo assinado por Authenticode, modificando uma imagem PE que não contenha realmente uma assinatura Authenticode.

Todos os dados em seções da imagem do PE especificados na tabela da seção são codificados em sua totalidade, exceto pelos seguintes intervalos de exclusão:

- **O campo de soma de verificação de arquivo dos campos específicos do Windows do cabeçalho opcional.** Essa soma de verificação inclui o arquivo inteiro (incluindo qualquer certificado de atributo no arquivo). Em todas as chances, a soma de verificação será diferente do valor original após a inserção da assinatura Authenticode.

- **Informações relacionadas aos certificados de atributo**. As áreas da imagem PE relacionadas à assinatura Authenticode não são incluídas no cálculo do hash de imagem do PE porque as assinaturas Authenticode podem ser adicionadas ou removidas de uma imagem sem afetar a integridade geral da imagem. Isso não é um problema, pois há cenários de usuário que dependem da reassinatura de imagens PE ou da adição de um carimbo de data/hora. O Authenticode exclui as seguintes informações do cálculo de hash:

  - O campo da tabela de certificados dos diretórios de dados de cabeçalho opcionais.

  - A tabela de certificados e os certificados correspondentes apontados pelo campo da tabela de certificados listados imediatamente acima.

  Para calcular o hash de imagem do PE, os pedidos de Authenticode as seções especificadas na tabela por intervalo de endereços, em seguida, geram hash na sequência resultante de bytes, passando os intervalos de exclusão.

- **Informações anteriores ao final da última seção.** A área após a última seção (definida pelo deslocamento mais alto) não tem hash. Essa área geralmente contém informações de depuração. Informações de depuração geralmente podem ser consideradas consultoria para depuradores; Ele não afeta a integridade real do programa executável. É literalmente possível remover informações de depuração de uma imagem depois que um produto é entregue e não afeta a funcionalidade do programa. Na verdade, isso às vezes é feito como uma medida de salvamento de disco. Vale a pena observar que as informações de depuração contidas nas seções especificadas da imagem PE não podem ser removidas sem invalidar a assinatura Authenticode.

Você pode usar as ferramentas MakeCert e SignTool fornecidas no SDK da plataforma Windows para experimentar a criação e a verificação de assinaturas Authenticode. Para obter mais informações, consulte a referência abaixo.

## <a name="references"></a>Referências

[Downloads e ferramentas para Windows (inclui o SDK do Windows)](https://developer.microsoft.com/windows/downloads)

[Criando, exibindo e gerenciando certificados](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Passo a passos de assinatura de código no modo kernel (. doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Formato de assinatura do executável portátil do Windows Authenticode (. docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[Funções do ImageHlp](/windows/desktop/Debug/imagehlp-functions)