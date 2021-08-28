---
description: Este tópico descreve dois utilitários usados para criar aplicativos de MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilitários de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9bb8a8608c97b700beebb53ce95fdf4b85c4d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481502"
---
# <a name="resource-utilities"></a>Utilitários de recursos

Este tópico descreve dois utilitários usados para criar aplicativos de MUI. Embora o LTDCT seja uma ferramenta específica da MUI, a MUI também usa o utilitário do compilador Windows RC padrão. Instruções para usar esses utilitários são fornecidas [em Localizando recursos e criando o aplicativo](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilitário DEMOSCT

O Muirct.exe (Muirct.exe) é um utilitário de linha de comando para dividir um arquivo executável padrão em um arquivo LN e arquivos de recurso específicos de linguagem (ou seja, localizáveis). Cada um dos arquivos resultantes contém dados de configuração de recurso para associação de arquivos. O LTDCT está incluído no SDK do Microsoft Windows para Windows Vista.

> [!Note]  
> A partir do Windows Vista, o carregador de recursos win32 é atualizado para carregar recursos de arquivos específicos do idioma, bem como de arquivos LN.

 

### <a name="muirct-usages"></a>Usos de LTDCT

1.  Dividir binário em arquivo binário principal e mui com base no arquivo de \_ configuração rc.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extraia a verificação do arquivo de \_ verificação e insira-a no arquivo de \_ saída.

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calcule a verificação com base no arquivo de verificação \_ e insira-a no arquivo de \_ saída.

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Despejar conteúdo de dados de configuração de recurso do arquivo de \_ entrada.

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Sintaxe DE LTDCT

O LTDCT pode tomar a direção das opções de linha de comando e/ou de um arquivo de configuração de recurso, especificado usando a opção -q.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Opções e argumentos**




| | | -h|-? | Mostra a tela de ajuda. | | -c | Especifica o valor de checksum_file do qual extrair ou calcular a aplicação de verificação de recursos. Checksum_file deve ser um arquivo binário Win32 contendo recursos localizáveis. Se checksum_file contiver recursos para mais de um idioma, a opção -b deverá ser usada para especificar qual deles deve ser usado, caso contrário, oEICT falhará. <br /> | | -b | Especifica o idioma a ser usado quando o checksum_file especificado com -c contém recursos em vários idiomas. Essa opção só pode ser usada em conjunto com a opção -c. O identificador de idioma pode estar em formato decimal ou hexadecimal. O LTDCT falhará se o checksum_file contiver recursos em vários idiomas e -b não for especificado ou se o idioma especificado pela opção -b não puder ser encontrado no checksum_file. <br /> | | -g | Especifica a ID de idioma a ser incluída como o idioma de fallback final na seção de dados de configuração de recursos do arquivo LN. Se o carregador de recursos não conseguir carregar um arquivo .mui solicitado dos idiomas de interface do usuário preferenciais do thread, ele usará o idioma de fallback final como sua última tentativa. O valor langID pode ser especificado em formato decimal ou hexadecimal. Por exemplo, inglês (Estados Unidos) pode ser especificado por -g 0x409 ou -g 1033. <br /> | | -q | Especifica que o source_file deve ser dividido no output_LN_file e no output_MUI_file de acordo com o layout rc_config arquivo. O rc_config arquivo é um arquivo formatado em XML que especifica quais recursos serão extraídos para o arquivo .mui e que serão deixados no arquivo LN. O rc_config pode especificar a distribuição de tipos de recursos e itens nomeados individuais entre os output_LN_file e output_MUI_file. O source_file deve ser um binário Win32 que contenha recursos em um único idioma, caso contrário, o TAMBÉM FALHARá. O LTDCT não dividirá o arquivo se ele for neutro no idioma, o que é indicado por ter apenas o valor da ID de idioma 0 no arquivo. Os output_LN_file e output_mui_file são os nomes do arquivo .mui e neutro de idioma no qual o source_file é dividido. Esses nomes de arquivo são opcionais. Se eles não são especificados, o LTDCT anexa as extensões .ln e .mui ao source_file. Normalmente, você deve remover a extensão ".ln" antes de implantar o arquivo. O LTDCT associa o output_LN_file e output_MUI_file calculando uma verificação com base no nome do source_file e na versão do arquivo e inserindo o resultado na seção de configuração de recursos de cada arquivo de saída. Quando usado em conjunto com a opção -c, a opção -q tem precedência. Se o arquivo rc_config fornecido com a opção -q contiver uma ata de verificação, o PROTOCOLCT ignorará a opção -c e inserirá o valor da verificação do valor, rc_config arquivo nos arquivos LN e.mui. Se nenhum valor de verificação for encontrado no rc_config, o LTDCT calculará a verificação de recursos com base no comportamento da opção -c. <br /> | | -v | Especifica o nível de detalhamento para registro em log. Especifique 1 para imprimir todas as mensagens de erro básicas e os resultados da operação. Especifique 2 para incluir também as informações de recurso (tipo, nome, identificador de idioma) incluídas no arquivo .mui e no arquivo LN. O padrão é -v 1 <br /> | | -x | Especifica a ID de idioma com a qual o LTDCT marca todos os tipos de recursos adicionados à seção de recursos do arquivo .mui. O valor langID pode ser especificado em formato decimal ou hexadecimal. Por exemplo, inglês (Estados Unidos) pode ser especificado por -x 0x409 ou -x 1033. <br /> | | -e | Extrai a verificação de recurso contida no checksum_file fornecido com a opção -c e insere-a no output_file. Quando -e é especificado, o LTDCT ignora todas as opções que não sejam a opção -c. Nesse caso, o checksum_file deve ser um arquivo binário Win32 que contém uma seção de dados de configuração de recurso com um valor de verificação. O output_file deve ser um arquivo LN ou arquivo .mui existente. <br /> | | -z | Calcula e insere dados de verificação de recursos no arquivo de saída especificado. O LTDCT baseia o cálculo de verificação na entrada fornecida com a opção -c e a opção opcional -b. Se você especificar um arquivo de saída para a opção -z que não existe, o SEMPRECT será final com uma falha.<br /> Exemplo: calcula a verificação com base em recursos localizáveis no Notepad.exe e insere a verificação no arquivo de saída Notepad2.exe.<br /><code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br /> | | -f | Permite a criação de um arquivo .mui com o recurso de versão sendo o único recurso localizável. Por padrão, o LTDCT não permite isso.<br /> | | -d | Localiza e exibe dados de configuração de recursos inseridos no arquivo de origem. Quando você especifica essa opção, o LTDCT ignora todas as outras opções de linha de comando.<br /> | | -m | Especifica o número de versão a ser usado ao calcular a verificação para associar o output_LN_file e output_MUI_file. <br /> | | source_filename | Nome do arquivo de origem binária localizado; curingas não podem ser usados. Esse arquivo só pode conter recursos em um idioma. Se houver recursos em vários idiomas no arquivo, o LTDCT falhará, a menos que a opção -b seja usada. Se o arquivo contiver recursos com identificadores de idioma que têm apenas o valor 0, o PROTOCOLCT não dividirá o arquivo porque um identificador de idioma 0 indicará um idioma neutro.<br /> Para a opção -d, source_filename é um arquivo LN ou um arquivo de recurso específico de idioma para o qual o SEMPRECT deve exibir dados de configuração de recursos. <br /> | | language_neutral_filename | Opcional. Nome do arquivo LN. Se você não especificar o nome desse arquivo, o LTDCT anexa uma segunda extensão ".ln" ao nome do arquivo de origem a ser usado como o nome de arquivo neutro em idioma. Normalmente, você deve remover a extensão ".ln" antes de implantar o arquivo.<blockquote>[!Note]<br />O arquivo LN não deve conter cadeias de caracteres ou menus. Você deve removê-los manualmente.</blockquote><br /> | | mui_filename | Opcional. Nome do arquivo de recurso específico do idioma. Se você não especificar um nome, o LTDCT anexa uma segunda extensão ".mui" ao nome do arquivo de origem a ser usado como o nome do arquivo. Normalmente, o LTDCT cria um arquivo de recurso específico do idioma. No entanto, ele não criará um arquivo de recurso se qualquer uma das seguintes condições existir:<br /><ul><li>Nenhum recurso localizável está no arquivo binário original.</li><li>O único idioma de recurso encontrado no arquivo binário original é o idioma neutro.</li><li>O arquivo binário original tem recursos para mais de um idioma, sem contar o idioma neutro. Se o arquivo binário contiver recursos para dois idiomas e um deles for o idioma neutro, o utilitário considerará o arquivo monolíngue e criará um arquivo de recurso específico de idioma se houver recursos localizáveis.</li></ul> | 




 

### <a name="muirct-language-output"></a>Saída de idioma DEMOSCT

O LTDCT escolhe o valor do atributo "UltimateFallbackLanguage" a ser inserido nos dados de configuração de recurso de arquivo LN com base na seguinte ordem, da prioridade mais alta à mais baixa:

1.  Atributo "UltimateFallbackLanguage" no arquivo de configuração de recurso de origem, se um for passado como entrada.
2.  O idioma especificado com a opção -g.
3.  Idioma do arquivo de entrada.

O LTDCT escolhe o valor do atributo "language" a ser inserido nos dados de configuração do recurso de arquivo .mui com base na seguinte ordem:

1.  Atributo "language" no arquivo de configuração de recurso de origem, se um for passado como entrada.
2.  O idioma especificado pela opção -x (forçar idioma).
3.  Idioma do arquivo de entrada.

### <a name="muirct-checksum-handling"></a>Manipulação de checksum DEMOSCT

O sistema operacional normalmente calcula a verificação sobre os recursos específicos do idioma em um arquivo, a menos que você especifique a verificação por meio de um arquivo de configuração de recurso. Desde que a verificação seja a mesma para o arquivo LN e todos os arquivos de recursos específicos de idioma associados, e o atributo de idioma na configuração de recurso no LN e na combinação dependente de idioma, o carregador de recursos pode carregar recursos com êxito.

O LTDCT dá suporte a vários métodos para colocar as verificações apropriadas nos dados de configuração de recursos:

1.  Crie um executável para cada idioma, contendo o código e os recursos. Depois disso, use o LTDCT para dividir cada um desses arquivos em um arquivo LN e um arquivo de recurso específico de idioma. O LTDCT é executado várias vezes, uma vez para gerar um arquivo de recurso para cada idioma. Você pode executar o build das seguintes maneiras:
    1.  Use a opção -q para especificar um valor de verificação no arquivo de configuração de recurso. O LTDCT coloca esse valor em todos os arquivos LN e arquivos de recurso específicos de idioma produzidos. Você precisa adotar uma estratégia para escolher esse valor, conforme descrito posteriormente neste tópico.
    2.  Use a opção -c (e, opcionalmente, a opção -b) para escolher um único idioma com recursos dos quais o TAMBÉM EXTRAi a verificação.
    3.  Use a opção -z para escolher um único idioma com recursos dos quais o SEMPRE EXTRAi a verificação. Aplique essa verificação depois que os arquivos foram construídos usando outros métodos.
2.  Crie um executável que contém o código e os recursos para um único idioma. Depois disso, use o LTDCT para dividir os recursos entre o arquivo LN e o arquivo de recurso específico do idioma. Por fim, use uma ferramenta de localização binária para modificar o arquivo de recurso resultante para cada idioma.

A convenção mais comum para manipulação de verificação é basear a verificação nos recursos de inglês (Estados Unidos). Você é livre para adotar uma convenção diferente, desde que seja consistente para cada arquivo LN. Por exemplo, é perfeitamente aceitável para uma empresa de desenvolvimento de software basear suas verificações no software que ele se baseia em recursos francês (França) em vez de recursos em inglês (Estados Unidos), desde que todos os aplicativos tenham recursos em francês (França) nos quais basear as verificações. Também é aceitável usar o arquivo de configuração de recurso para atribuir um valor hexadecimal arbitrário de até 16 dígitos hexadecimais como uma verificação. Essa última estratégia impede o uso efetivo das opções -z, -c e -b de LTDCT. Ele requer a adoção de um método usando [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) ou alguma outra ferramenta para gerar valores de verificação. Essa estratégia também exige que você desmarque uma política para determinar quando modificar o valor ao adicionar novos recursos localizáveis.

Para aplicar a verificação de inglês (Estados Unidos) a todos os arquivos, você pode usar qualquer um dos métodos de manipulação de verificação descritos acima. Por exemplo, você pode gerar o arquivo LN e o arquivo de recurso específico do idioma para inglês (Estados Unidos) e, em seguida, usar a opçãoEICT -d para obter a verificação resultante. Você pode copiar essa verificação para o arquivo de configuração de recurso e usar a opção -q com o PROTOCOLCT para aplicar a verificação a todos os outros arquivos.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Uso de um arquivo de configuração de recurso com o TAMBÉMCT

Você pode especificar dados de configuração de recurso ao usar oVOLCT. Se você fornecer explicitamente um arquivo de configuração de recurso, cada arquivo de recurso específico do idioma terá dados de configuração de recurso, assim como qualquer arquivo LN com um arquivo de recurso associado. Por exemplo:

-   Se você usar a opção -q para especificar um arquivo de configuração de recurso, mas não houver recursos localizáveis no arquivo de origem de entrada, nenhum arquivo de recurso específico de idioma será gerado e o arquivo LN resultante não conterá dados de configuração de recurso. Além disso, se o arquivo de origem de entrada tiver recursos multilíngues, o PROTOCOLCT não dividirá o arquivo.

> [!Note]  
> Atualmente, o comportamento de PROTOCOLCT é inconsistente quando o elemento neutralResources do arquivo de configuração de recurso não contém nenhum elemento resourceType e o elemento localizedResources contém cadeias de caracteres e menus, por exemplo. Nesse caso, o LTDCT divide os recursos da seguinte forma:
>
> -   Todos os recursos no binário original (incluindo cadeias de caracteres e menus), além dos recursos de MUI, são colocados no arquivo LN.
> -   Cadeias de caracteres, menus e recursos de MUI são colocados no arquivo de recurso específico do idioma apropriado.

 

### <a name="examples-for-using-muirct"></a>Exemplos para usar o LTDCT

**Exemplos de uso padrão**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Exemplo de saída de arquivo LN usando a opção -d**

Aqui está um exemplo da saída de dados de configuração de recurso de um arquivo LN, Shell32.dll, usando a opção -d com o PROTOCOLCT:


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



**Exemplo de Language-Specific de arquivo de recurso usando a opção -d**

Aqui está um exemplo da saída de dados de configuração de recurso de um arquivo .mui, Shell32.dll.mui, usando a opção -d para PROTOCOLCT:


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a>Utilitário do compilador RC

O Compilador RC (Rc.exe) é um utilitário de linha de comando para compilar um arquivo de script de definição de recurso (extensão .rc) em arquivos de recurso (extensão .res). O Compilador RC está incluído no SDK do Windows. Este documento explica apenas o uso do Compilador RC com recursos relacionados à MUI do carregador de recursos. Para obter informações completas sobre o compilador, consulte [About Resource Files](../menurc/about-resource-files.md).

O Compilador RC permite que você crie, de um único conjunto de fontes, um arquivo LN e um arquivo de recurso específico de idioma separado. Quanto ao LTDCT, os arquivos são associados por dados de configuração de recurso.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>Sintaxe do compilador RC usada para recursos de MUI

As opções do compilador RC são definidas em detalhes [em Usando RC](../menurc/using-rc-the-rc-command-line-.md). Esta seção define apenas as opções usadas para criar recursos de MUI. Lembre-se de que cada opção não faz maiúsculas de minúsculas. Presume-se que os tipos de recursos sejam neutros em idioma, a menos que indicado de outra forma.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Opções e argumentos**




| | | -h|-? | Mostra a tela de ajuda. | | -fm | Usa o arquivo de recurso especificado para recursos específicos do idioma. Normalmente, o compilador de recursos cria um arquivo de recurso específico de linguagem. No entanto, ele não criará o arquivo se qualquer uma das seguintes condições existir:<br /><ul><li>Não há recursos localizáveis no arquivo .rc.</li><li>O único idioma de recurso encontrado no arquivo .rc é o idioma neutro.</li><li>O arquivo .rc tem recursos para mais de um idioma, sem contar o idioma neutro. Se o arquivo .rc contiver recursos para dois idiomas e um deles for o idioma neutro, o compilador considerará o arquivo como monolíngue. Se houver recursos localizáveis, o compilador criará um arquivo de recurso específico de linguagem.</li></ul> | | -q | Usa o arquivo de configuração de recurso especificado para obter os tipos de recursos a ser colocado no arquivo de recurso específico do idioma e no arquivo LN. Para obter mais informações, consulte <a href="preparing-a-resource-configuration-file.md">Preparando um arquivo de configuração de recurso</a>. Como alternativa a essa opção, você pode usar as opções -j e -k, mas é preferível usar um arquivo de configuração de recurso. <br /> Usando a opção -q com um arquivo de configuração de recurso, você pode implementar uma divisão baseada em item e fornecer atributos que acabarão com a configuração de recurso binário no LN e no arquivo de recurso específico de idioma. Essa divisão não é possível usando as opções -j e -k.<blockquote>[!Note]<br />O processo de divisão do compilador RC não funcionará corretamente se você armazenar recursos e informações de versão em arquivos de configuração de recursos diferentes. Nesse caso, o Compilador RC não divide as informações de versão. Portanto, ocorre um erro de vinculador durante a vinculação do arquivo de recurso específico do idioma porque o arquivo não tem recursos de versão.</blockquote><br /><br /> | | -g | Especifica o identificador de <a href="language-identifiers.md">idioma de fallback</a> final em hexadecimal.<br /> | | -g1 | Cria um arquivo .res da MUI mesmo que o recurso VERSION seja o único conteúdo localizável. Por padrão, o Compilador RC não produzirá um arquivo .res se VERSION for o único recurso localizável.<br /> | | -g2 | Especifica o número de versão personalizado a ser usado ao calcular a verificação.<br /> | | mui_res_name | Arquivo de recurso para recursos específicos do idioma.<br /> | | rc_config_file_name | Arquivo de configuração de recurso.<br /> | | langid | Identificador de idioma.<br /> | | versão | Número de versão personalizado, em um formato como "6.2.0.0".<br /> | 




 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Exemplo de como usar o compilador RC para criar recursos de MUI

Para ilustrar a operação do compilador RC com recursos de MUI, vamos examinar a seguinte linha de comando para o arquivo de recurso Myfile.rc:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Essa linha de comando faz com que o Compilador RC faça o seguinte:

-   Crie o arquivo de recurso específico de idioma Myfile res.res e um arquivo de recurso neutro em idioma que assume Como padrão Myfile.res, com base no nome do \_ arquivo .rc.
-   Adicione os tipos de recurso 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY TYPE ao arquivo .res específico da linguagem se eles estão no \_ arquivo .rc.
-   Adicione o tipo de recurso 16, juntamente com todos os outros tipos de recursos descritos no arquivo de recurso ao arquivo .res com neutralidade de idioma e ao arquivo .res específico do idioma. Observe que, neste exemplo, o tipo de recurso 16 está sendo adicionado em dois locais.
-   Escolha o valor do atributo "UltimateFallbackLanguage" para inserir nos dados de configuração de recurso de arquivo LN com base nos seguintes critérios, ordenados da prioridade mais alta para a mais baixa:
    -   Atributo "UltimateFallbackLanguage" no arquivo de configuração de recurso se um for passado como entrada.
    -   Valor do atributo de linguagem a ser inserido nos dados de configuração de recursos com base na ordem da linguagem do compilador RC (idioma neutro e idioma específico do idioma). As considerações incluem o idioma no arquivo .rc, o valor do idioma da opção -gl e o identificador 0x0409 para inglês (Estados Unidos).

## <a name="remarks"></a>Comentários

Se você incluir qualquer tipo de recurso ICON(3), DIALOG(5), STRING(6) ou VERSION(16) no elemento neutralResources, será preciso duplicar essa entrada no elemento localizedResources no arquivo de configuração de recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface de Usuário Multilíngue Referência](multilingual-user-interface-reference.md)
</dt> <dt>

[Gerenciamento de Recursos da MUI](mui-resource-management.md)
</dt> <dt>

[Localizando recursos e criando o aplicativo](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
