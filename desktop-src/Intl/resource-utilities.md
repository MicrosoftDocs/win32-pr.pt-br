---
description: Este tópico descreve dois utilitários usados para criar aplicativos MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilitários de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922335"
---
# <a name="resource-utilities"></a>Utilitários de recursos

Este tópico descreve dois utilitários usados para criar aplicativos MUI. Embora o MUIRCT seja uma ferramenta específica de MUI, o MUI também utiliza o utilitário de compilador padrão do Windows RC. As instruções para usar esses utilitários são fornecidas em [localizando recursos e compilando o aplicativo](localizing-resources-and-building-the-application.md).

## <a name="muirct-utility"></a>Utilitário MUIRCT

MUIRCT (Muirct.exe) é um utilitário de linha de comando para dividir um arquivo executável padrão em um arquivo LN e arquivos de recurso específicos a um idioma (ou seja, localizável). Cada um dos arquivos resultantes contém dados de configuração de recursos para a associação de arquivos. O MUIRCT está incluído no SDK do Microsoft Windows para o Windows Vista.

> [!Note]  
> A partir do Windows Vista, o carregador de recursos do Win32 é atualizado para carregar recursos de arquivos específicos do idioma, bem como de arquivos LN.

 

### <a name="muirct-usages"></a>Usos de MUIRCT

1.  Dividir Binary em arquivo binário principal e mui com base no \_ arquivo de configuração RC.

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  Extrair soma de verificação do arquivo de soma de verificação \_ e inseri-la no arquivo de saída \_ .

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  Calcule soma de verificação com base no arquivo de soma de verificação \_ e insira-a no arquivo de saída \_ .

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  Despeja o conteúdo dos dados de configuração do recurso do arquivo de entrada \_ .

    `Muirct -d input_file`

### <a name="muirct-syntax"></a>Sintaxe de MUIRCT

MUIRCT pode tomar a direção das opções de linha de comando e/ou de um arquivo de configuração de recurso, especificado usando a opção-q.


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



**Opções e argumentos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Mostra a tela de ajuda.</td>
</tr>
<tr class="even">
<td>-c</td>
<td>Especifica o checksum_file de entrada do qual extrair ou calcular a soma de verificação do recurso. Checksum_file deve ser um arquivo binário Win32 contendo recursos localizáveis. Se checksum_file contiver recursos para mais de um idioma, a opção-b deverá ser usada para especificar quais deles devem ser usados caso contrário, MUIRCT falhará. <br/></td>
</tr>
<tr class="odd">
<td>-b</td>
<td>Especifica o idioma a ser usado quando o checksum_file especificado com-c contém recursos em vários idiomas. Essa opção só pode ser usada em conjunto com a opção-c. O identificador de idioma pode estar no formato decimal ou hexadecimal. MUIRCT falhará se o checksum_file contiver recursos em vários idiomas e-b não for especificado ou se o idioma especificado pela opção-b não puder ser encontrado no checksum_file. <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Especifica a ID de idioma a ser incluída como o idioma de fallback final na seção de dados de configuração de recurso do arquivo LN. Se o carregador de recursos não carregar um arquivo. mui solicitado dos idiomas de interface do usuário preferenciais do thread, ele usará o idioma de fallback final como sua última tentativa. O valor de LangID pode ser especificado em formato decimal ou hexadecimal. Por exemplo, inglês (Estados Unidos) pode ser especificado por-g 0x409 ou-g 1033. <br/></td>
</tr>
<tr class="odd">
<td>-Q</td>
<td>Especifica que o source_file deve ser dividido no output_LN_file e o output_MUI_file de acordo com o layout do arquivo de rc_config. O arquivo de rc_config é um arquivo formatado XML que especifica quais recursos serão extraídos para o arquivo. mui e que serão deixados no arquivo LN. O rc_config pode especificar a distribuição de tipos de recursos e itens nomeados individuais entre o output_LN_file e output_MUI_file. O source_file deve ser um binário do Win32 que contém recursos em um único idioma, caso contrário, o MUIRCT falhará. MUIRCT não dividirá o arquivo se for um idioma neutro, que é indicado por ter apenas o valor de ID de idioma 0 no arquivo. O output_LN_file e output_mui_file são os nomes do arquivo de idioma neutro e. mui no qual o source_file é dividido. Esses nomes de arquivo são opcionais. Se eles não forem especificados, o MUIRCT acrescentará as extensões. ln e. mui a source_file. Normalmente, você deve remover a &quot; extensão. ln &quot; antes de implantar o arquivo. MUIRCT associa a output_LN_file e output_MUI_file calculando uma soma de verificação com base no nome do source_file e na versão do arquivo e inserindo o resultado na seção de configuração do recurso de cada arquivo de saída. Quando usado em conjunto com a opção-c, a opção-q tem precedência. Se o arquivo de rc_config fornecido com a opção-q contiver uma soma de verificação, MUIRCT ignorará a opção-c e inserirá o valor da soma de verificação do valor, rc_config arquivo nos arquivos LN e. mui. Se nenhum valor de soma de verificação for encontrado no rc_config, MUIRCT calculará a soma de verificação do recurso com base no comportamento da opção-c. <br/></td>
</tr>
<tr class="even">
<td>-v</td>
<td>Especifica o nível de detalhamento para registro em log. Especifique 1 para imprimir todas as mensagens de erro e os resultados de operação básicos. Especifique 2 para incluir também as informações de recurso (tipo, nome, identificador de idioma) incluídas no arquivo. mui e no arquivo LN. O padrão é-v 1 <br/></td>
</tr>
<tr class="odd">
<td>-X</td>
<td>Especifica a ID de idioma com a qual MUIRCT marca todos os tipos de recursos adicionados à seção de recursos do arquivo. mui. O valor de LangID pode ser especificado em formato decimal ou hexadecimal. Por exemplo, inglês (Estados Unidos) pode ser especificado por-x 0x409 ou-x 1033. <br/></td>
</tr>
<tr class="even">
<td>-E</td>
<td>Extrai a soma de verificação de recurso contida na checksum_file fornecida com a opção-c e a insere no output_file especificado. Quando-e é especificado, o MUIRCT ignora todas as opções diferentes da opção-c. Nesse caso, o checksum_file deve ser um arquivo binário Win32 que contém uma seção de dados de configuração de recurso com um valor de soma de verificação. O output_file deve ser um arquivo LN ou. mui existente. <br/></td>
</tr>
<tr class="odd">
<td>-Z</td>
<td>Calcula e insere os dados de soma de verificação do recurso no arquivo de saída especificado. MUIRCT baseia o cálculo da soma de verificação na entrada fornecida com a opção-c e a opção-b opcional. Se você especificar um arquivo de saída para a opção-z que não existe, o MUIRCT será fechado com uma falha.<br/> Exemplo: calcula a soma de verificação com base em recursos localizáveis em Notepad.exe e insere a soma de verificação no arquivo de saída Notepad2.exe.<br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td>-f</td>
<td>Habilita a criação de um arquivo. mui com o recurso de versão que é o único recurso localizável. Por padrão, o MUIRCT não permite isso.<br/></td>
</tr>
<tr class="odd">
<td>-d</td>
<td>Localiza e exibe dados de configuração de recursos inseridos no arquivo de origem. Quando você especifica essa opção, o MUIRCT ignora todas as outras opções de linha de comando.<br/></td>
</tr>
<tr class="even">
<td>-M</td>
<td>Especifica o número de versão a ser usado ao calcular a soma de verificação para associar o output_LN_file e output_MUI_file. <br/></td>
</tr>
<tr class="odd">
<td>source_filename</td>
<td>Nome do arquivo de origem binário localizado; caracteres curinga não podem ser usados. Este arquivo só pode conter recursos em um idioma. Se houver recursos em vários idiomas no arquivo, MUIRCT falhará, a menos que a opção-b seja usada. Se o arquivo contiver recursos com identificadores de idioma com somente o valor 0, o MUIRCT não dividirá o arquivo porque um identificador de idioma 0 indica uma linguagem neutra.<br/> Para a opção-d, source_filename é um arquivo LN ou um arquivo de recurso específico a um idioma para o qual MUIRCT é para exibir dados de configuração de recurso. <br/></td>
</tr>
<tr class="even">
<td>language_neutral_filename</td>
<td>Opcional. Nome do arquivo LN. Se você não especificar o nome desse arquivo, o MUIRCT acrescentará uma segunda extensão &quot; . ln &quot; ao nome do arquivo de origem a ser usado como o nome do arquivo com neutralidade de idioma. Normalmente, você deve remover a &quot; extensão. ln &quot; antes de implantar o arquivo.
<blockquote>
[!Note]<br />
O arquivo LN não deve conter cadeias de caracteres ou menus. Você deve removê-los manualmente.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>mui_filename</td>
<td>Opcional. Nome do arquivo de recurso específico do idioma. Se você não especificar um nome, o MUIRCT acrescentará uma segunda extensão &quot; . mui &quot; ao nome do arquivo de origem a ser usado como o nome do arquivo. Normalmente, o MUIRCT cria um arquivo de recursos específico do idioma. No entanto, ele não cria um arquivo de recurso se alguma das seguintes condições existir:<br/>
<ul>
<li>Não há recursos localizáveis no arquivo binário original.</li>
<li>O único idioma de recurso encontrado no arquivo binário original é o idioma neutro.</li>
<li>O arquivo binário original tem recursos para mais de um idioma, não contando a linguagem neutra. Se o arquivo binário contiver recursos para dois idiomas, e um deles for o idioma neutro, o utilitário considerará o arquivo como multilíngue e criará um arquivo de recursos específico do idioma se houver recursos localizáveis.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a>Saída da linguagem MUIRCT

MUIRCT escolhe o valor do atributo "UltimateFallbackLanguage" para inserir nos dados de configuração de recursos do arquivo LN com base na seguinte ordem, da prioridade mais alta para a mais baixa:

1.  O atributo "UltimateFallbackLanguage" no arquivo de configuração de recurso de origem, se um for passado como entrada.
2.  O idioma especificado com a opção-g.
3.  Idioma do arquivo de entrada.

MUIRCT escolhe o valor do atributo "Language" para inserir nos dados de configuração do recurso de arquivo. mui com base na seguinte ordem:

1.  atributo "Language" no arquivo de configuração de recurso de origem, se um for passado como entrada.
2.  O idioma especificado pela opção-x (forçar idioma).
3.  Idioma do arquivo de entrada.

### <a name="muirct-checksum-handling"></a>Manipulação de soma de verificação MUIRCT

O sistema operacional normalmente calcula a soma de verificação sobre os recursos específicos do idioma em um arquivo, a menos que você especifique a soma de verificação por meio de um arquivo de configuração de recurso. Contanto que a soma de verificação seja a mesma para o arquivo LN e todos os arquivos de recursos específicos de idioma associados, e o atributo language na configuração de recurso no LN e a correspondência dependente de idioma, o carregador de recursos poderá carregar recursos com êxito.

O MUIRCT dá suporte a vários métodos para colocar as somas de verificação apropriadas nos dados de configuração do recurso:

1.  Crie um executável para cada idioma, contendo código e recursos. Depois disso, use MUIRCT para dividir cada um desses arquivos em um arquivo LN e um arquivo de recurso específico a um idioma. MUIRCT é executado várias vezes, uma vez para gerar um arquivo de recurso para cada idioma. Você pode executar a compilação das seguintes maneiras:
    1.  Use a opção-q para especificar um valor de soma de verificação no arquivo de configuração de recurso. MUIRCT coloca esse valor em todos os arquivos LN e arquivos de recursos específicos de idioma produzidos. Você precisa adotar uma estratégia para escolher esse valor, conforme descrito posteriormente neste tópico.
    2.  Use a opção-c (e, opcionalmente, a opção-b) para escolher um único idioma com recursos dos quais o MUIRCT Extraia a soma de verificação.
    3.  Use a opção-z para escolher um único idioma com recursos dos quais o MUIRCT sempre extrai a soma de verificação. Aplique essa soma de verificação depois que os arquivos tiverem sido criados usando outros métodos.
2.  Crie um executável contendo código e recursos para uma única linguagem. Depois disso, use MUIRCT para dividir os recursos entre o arquivo LN e o arquivo de recursos específicos do idioma. Por fim, use uma ferramenta de localização binária para modificar o arquivo de recurso resultante para cada idioma.

A Convenção mais comum para manipulação de soma de verificação é basear a soma de verificação nos recursos em inglês (Estados Unidos). Você tem a liberdade de adotar uma convenção diferente, desde que seja consistente para cada arquivo LN. Por exemplo, é perfeitamente aceitável que uma empresa de desenvolvimento de software baseie suas somas de verificação no software que ele cria em recursos franceses (França) em vez de recursos em inglês (Estados Unidos), desde que todos os aplicativos tenham recursos franceses (França) nos quais basear as somas de verificação. Também é aceitável usar o arquivo de configuração de recurso para atribuir um valor hexadecimal arbitrário de até 16 dígitos hexadecimais como uma soma de verificação. Essa última estratégia impede o uso efetivo das opções-z,-c e-b de MUIRCT. Ele requer a adoção de um método usando o [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) ou alguma outra ferramenta para gerar valores de soma de verificação. Essa estratégia também exige que você configure uma política para determinar quando modificar o valor ao adicionar novos recursos localizáveis.

Para aplicar a soma de verificação em inglês (Estados Unidos) a todos os arquivos, você pode usar qualquer um dos métodos de manipulação de soma de verificação descritos acima. Por exemplo, você pode gerar o arquivo LN e o arquivo de recursos específicos do idioma para inglês (Estados Unidos) e, em seguida, usar a opção MUIRCT-d para obter a soma de verificação resultante. Você pode copiar essa soma de verificação em seu arquivo de configuração de recurso e usar a opção-q com MUIRCT para aplicar a soma de verificação a todos os outros arquivos.

### <a name="use-of-a-resource-configuration-file-with-muirct"></a>Uso de um arquivo de configuração de recurso com MUIRCT

Você pode especificar os dados de configuração do recurso ao usar o MUIRCT. Se você fornecer ou não explicitamente um arquivo de configuração de recurso, cada arquivo de recurso específico de idioma tem dados de configuração de recursos, assim como qualquer arquivo LN com um arquivo de recurso associado. Por exemplo:

-   Se você usar a opção-q para especificar um arquivo de configuração de recurso, mas não houver recursos localizáveis no arquivo de origem de entrada, nenhum arquivo de recurso específico de idioma será gerado e o arquivo LN resultante não conterá dados de configuração de recursos. Além disso, se o arquivo de origem de entrada tiver recursos multilíngües, o MUIRCT não dividirá o arquivo.

> [!Note]  
> Atualmente, o comportamento de MUIRCT é inconsistente quando o elemento neutralResources do arquivo de configuração de recurso não contém nenhum elemento resourceType e o elemento localizedResources contém cadeias de caracteres e menus, por exemplo. Nesse caso, o MUIRCT divide os recursos da seguinte maneira:
>
> -   Todos os recursos no binário original (incluindo cadeias de caracteres e menus), além dos recursos do MUI, são colocados no arquivo LN.
> -   As cadeias de caracteres, os menus e os recursos do MUI são colocados no arquivo de recursos específico do idioma apropriado.

 

### <a name="examples-for-using-muirct"></a>Exemplos de uso de MUIRCT

**Exemplos de uso padrão**


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



**Exemplo de saída de arquivo LN usando a opção-d**

Aqui está um exemplo da saída de dados de configuração de recurso de um arquivo LN, Shell32.dll, usando a opção-d com MUIRCT:


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



**Exemplo de saída de arquivo de recurso de Language-Specific usando a opção-d**

Aqui está um exemplo da saída de dados de configuração de recurso de um arquivo. mui, Shell32.dll. mui, usando a opção-d para MUIRCT:


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



## <a name="rc-compiler-utility"></a>Utilitário de compilador RC

O compilador RC (Rc.exe) é um utilitário de linha de comando para compilar um arquivo de script de definição de recurso (extensão. rc) em arquivos de recurso (extensão. res). O compilador RC está incluído no SDK do Windows. Este documento explica apenas o uso do compilador RC com recursos relacionados ao MUI do carregador de recursos. Para obter informações completas sobre o compilador, consulte [About Resource files](../menurc/about-resource-files.md).

O compilador RC permite que você crie, de um único conjunto de fontes, um arquivo LN e um arquivo de recursos específico de idioma separado. Para MUIRCT, os arquivos são associados pelos dados de configuração do recurso.

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a>Sintaxe do compilador RC como usada para recursos MUI

As opções do compilador RC são definidas em detalhes no [uso do RC](../menurc/using-rc-the-rc-command-line-.md). Esta seção define apenas as opções usadas para criar recursos do MUI. Lembre-se de que cada opção não diferencia maiúsculas de minúsculas. Os tipos de recursos são considerados neutros à língua, a menos que indicado em contrário.


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



**Opções e argumentos**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>-h |-?</td>
<td>Mostra a tela de ajuda.</td>
</tr>
<tr class="even">
<td>-FM</td>
<td>Usa o arquivo de recurso especificado para recursos específicos do idioma. Normalmente, o compilador de recurso cria um arquivo de recurso específico do idioma. No entanto, ele não cria o arquivo se alguma das seguintes condições existir:<br/>
<ul>
<li>Não há recursos localizáveis no arquivo. rc.</li>
<li>O único idioma de recurso encontrado no arquivo. rc é o idioma neutro.</li>
<li>O arquivo. RC tem recursos para mais de um idioma, não contando a linguagem neutra. Se o arquivo. rc contiver recursos para dois idiomas, e um deles for o idioma neutro, o compilador considerará o arquivo como multilíngue. Se houver recursos localizáveis, o compilador criará um arquivo de recursos específico do idioma.</li>
</ul></td>
</tr>
<tr class="odd">
<td>-Q</td>
<td>Usa o arquivo de configuração de recurso especificado para obter os tipos de recurso a serem colocados no arquivo de recurso específico do idioma e no arquivo LN. Para obter mais informações, consulte <a href="preparing-a-resource-configuration-file.md">preparando um arquivo de configuração de recurso</a>. Como alternativa a essa opção, você pode usar as opções-j e-k, mas é preferível usar um arquivo de configuração de recurso. <br/> Usando a opção-q com um arquivo de configuração de recurso, você pode implementar uma divisão baseada em item e fornecer atributos que acabarão com a configuração de recursos binários no LN e no arquivo de recurso específico do idioma. Essa divisão não é possível usando as opções-j e-k.
<blockquote>
[!Note]<br />
O processo de divisão do compilador RC não funcionará corretamente se você armazenar recursos e informações de versão em arquivos de configuração de recurso diferentes. Nesse caso, o compilador RC não divide as informações de versão. Portanto, um erro de vinculador ocorre durante a vinculação do arquivo de recursos específico do idioma porque o arquivo não tem recursos de versão.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-g</td>
<td>Especifica o identificador de <a href="language-identifiers.md">idioma de fallback</a> final em hexadecimal.<br/></td>
</tr>
<tr class="odd">
<td>-G1</td>
<td>Cria um arquivo MUI. res mesmo que o recurso de versão seja o único conteúdo localizável. Por padrão, o compilador RC não produzirá um arquivo. res se a versão for o único recurso localizável.<br/></td>
</tr>
<tr class="even">
<td>-g2</td>
<td>Especifica o número de versão personalizado a ser usado ao calcular a soma de verificação.<br/></td>
</tr>
<tr class="odd">
<td>mui_res_name</td>
<td>Arquivo de recurso para recursos específicos do idioma.<br/></td>
</tr>
<tr class="even">
<td>rc_config_file_name</td>
<td>Arquivo de configuração de recurso.<br/></td>
</tr>
<tr class="odd">
<td>langid</td>
<td>Identificador de idioma.<br/></td>
</tr>
<tr class="even">
<td>version</td>
<td>Número de versão personalizado, em um formato como &quot; 6.2.0.0 &quot; .<br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a>Exemplo de uso do compilador RC para criar recursos MUI

Para ilustrar a operação do compilador RC com recursos do MUI, vamos examinar a seguinte linha de comando para o arquivo de recurso MyFile. rc:


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



Essa linha de comando faz com que o compilador RC faça o seguinte:

-   Crie o arquivo de recurso específico do idioma MyFile \_ res. res e um arquivo de recurso neutro de idioma que assume o padrão de MyFile. res, com base no nome do arquivo. rc.
-   Adicione os dois (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 meus \_ tipos de recursos de tipo ao arquivo. res específico ao idioma se eles estiverem no arquivo. rc.
-   Adicione o tipo de recurso 16, juntamente com quaisquer outros tipos de recursos descritos no arquivo de recurso ao arquivo. res de idioma neutro e ao arquivo. res específico do idioma. Observe que, neste exemplo, o tipo de recurso 16 está sendo adicionado em dois lugares.
-   Escolha o valor do atributo "UltimateFallbackLanguage" para inserir nos dados de configuração de recurso do arquivo LN com base nos critérios a seguir, ordenados da prioridade mais alta para a mais baixa:
    -   O atributo "UltimateFallbackLanguage" no arquivo de configuração de recurso se um for passado como entrada.
    -   O valor do atributo de idioma a ser inserido nos dados de configuração de recurso com base na ordem de linguagem do compilador RC (linguagem de arquivo de recurso de linguagem neutra e específica de idioma). As considerações incluem o idioma no arquivo. rc, o valor de idioma da opção-GL e o identificador 0x0409 para inglês (Estados Unidos).

## <a name="remarks"></a>Comentários

Se você incluir qualquer ícone (3), caixa de diálogo (5), Cadeia de caracteres (6) ou tipo de recurso de versão (16) no elemento neutralResources, terá que duplicar essa entrada no elemento localizedResources no arquivo de configuração de recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de interface do usuário multilíngue](multilingual-user-interface-reference.md)
</dt> <dt>

[Gerenciamento de recursos do MUI](mui-resource-management.md)
</dt> <dt>

[Localizando recursos e compilando o aplicativo](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
