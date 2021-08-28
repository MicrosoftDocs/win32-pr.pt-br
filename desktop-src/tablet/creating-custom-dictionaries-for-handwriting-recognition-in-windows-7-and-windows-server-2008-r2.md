---
description: Esta seção explica como criar um dicionário personalizado para reconhecimento de manuscrito.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Criando dicionários personalizados para reconhecimento de manuscrito no Windows 7 e Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe391125b21bfe35a9e1a69be6258e1643b424e
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883885"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Criando dicionários personalizados para reconhecimento de manuscrito no Windows 7 e Windows Server 2008 R2

Esta seção explica como criar um dicionário personalizado para reconhecimento de manuscrito.

No sistema operacional Windows 7 e no sistema operacional Windows Server 2008 R2, a precisão do reconhecimento de manuscrito pode ser significativamente aprimorada por meio do uso de dicionários personalizados. Esses dicionários complementam ou substituem dicionários do sistema usados para manuscrito. O suporte para reconhecimento de manuscrito é fornecido por meio do Serviços de Reconhecimento de Manuscrito que precisa ser habilitado por meio de Gerenciador do Servidor.

> [!Note]  
> Dicionários personalizados podem ser instalados para um idioma somente se o reconhecedor de manuscrito para esse idioma estiver instalado.

 

Há duas etapas básicas para configurar um dicionário personalizado para manuscrito:

-   Compile uma lista de palavras. A compilação cria um arquivo de dicionário personalizado compilado (.hwrdict).
-   Instale o dicionário personalizado compilado.

## <a name="compiling-a-word-list"></a>Compilando uma lista de palavras

A lista de palavras a ser compilada deve estar em formato de texto sem formatação e deve ser salva usando uma codificação Unicode. Outras codificações não funcionarão. Cada linha do arquivo de texto é tomada como uma única entrada no dicionário. Entradas de unidades de várias palavras que contêm um ou mais espaços são permitidas. Os espaços no início ou no final de uma linha são ignorados.

Um dicionário personalizado é compilado de uma linha de comando. Para compilar um dicionário, abra uma janela de comando, navegue até a pasta que contém a lista de palavras e, em seguida, execute HwrComp.exe com as opções de linha de comando que você deseja usar.

O exemplo a seguir mostra a sintaxe de uso para as opções de linha de comando.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Explicação das opções



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang &lt; localename&gt;</td>
<td>O nome de localidade especificado atribuído ao arquivo de dicionário personalizado compilado. O nome &lt; do argumento local tem o formato &gt; language-REGION. Um exemplo disso é en-US, que significa o idioma inglês na Estados Unidos região. Para exemplos desse formulário, consulte Constantes e cadeias de caracteres do [identificador de idioma.](/windows/desktop/Intl/language-identifier-constants-and-strings) Os seguintes idiomas têm suporte para o Windows 7 e o Windows Server 2008 R2 por este recurso: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-ES, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES e hr-HR.<br/></td>
</tr>
<tr class="even">
<td>-type &lt; type&gt;</td>
<td>O tipo de argumento option é uma concatenação de cadeia de caracteres única do uso do recurso como a lista de palavras principais (PRIMARY) ou como um suplemento para a lista de palavras principais (SECONDARY) seguida pelo nome real da lista de palavras à qual o recurso &lt; &gt; é aplicado (como DICTIONARY ou SURNAME). O valores possíveis são os seguintes:
<ul>
<li>PRIMARY-CITYNAME-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>PRIMARY-DICTIONARY</li>
<li>PRIMARY-GIVENNAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>PRIMARY-SURNAME-LIST</li>
<li>SECONDARY-CITYNAME-LIST</li>
<li>SECONDARY-COUNTRYNAME-LIST</li>
<li>SECONDARY-COUNTRYSHORTNAME-LIST</li>
<li>SECONDARY-DICTIONARY</li>
<li>SECONDARY-EMAILSMTP-LIST</li>
<li>SECONDARY-EMAILUSERNAME-LIST</li>
<li>SECONDARY-GIVENNAME-LIST</li>
<li>SECONDARY-STATEORPROVINCE-LIST</li>
<li>SECONDARY-STREETNAME-LIST</li>
<li>SECONDARY-SURNAME-LIST</li>
<li>SECONDARY-URL-LIST</li>
</ul>
Se um valor de tipo começar com o prefixo PRIMARY, o dicionário compilado, depois de instalado, substituirá o dicionário do sistema para esse idioma. O valor PRIMARY-DICTIONARY representa o dicionário do sistema principal para um idioma.
<blockquote>
[!Note]<br />
Substituir um dicionário do sistema não faz nada para o conteúdo original do dicionário do sistema, pois a substituição só está em vigor até que o dicionário personalizado tenha sido removido.
</blockquote>
<br/> Se um valor de tipo começar com o prefixo SECONDARY, o dicionário compilado complementará o dicionário do sistema sem substituí-lo.</td>
</tr>
<tr class="odd">
<td>-comment <comment></td>
<td>O comentário especificado é compilado no arquivo de dicionário. O comentário deve ser uma única cadeia de caracteres e não ter mais de 64 caracteres.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>A saída é escrita no nome de arquivo especificado por <dictfile.hwrdict> .<br/> Se essa opção estiver ausente, o nome do arquivo de saída será derivado do nome do arquivo de entrada original, com a extensão de arquivo de entrada substituída por .hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Padrões

Se nenhum parâmetro for especificado, os valores de opção padrão serão

-lang <current input language> -type SECONDARY-DICTIONARY

### <a name="examples"></a>Exemplos

O seguinte compila o arquivo de entrada mylist1.txt, aplica os valores de opção padrão e cria o arquivo de saída mylist1.hwrdict.

``` syntax
hwrcomp mylist1.txt
```

Por outro lado, o seguinte compila mylist1.txt em myrsrc1.hwrdict, mas atribui "Inglês (EUA)" (en-US) como o idioma e SECONDARY-DICTIONARY como o tipo.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Instalando um dicionário personalizado compilado

HwrComp.exe cria um arquivo .hwrdict, que está em um formato binário que pode ser usável por um reconhecedor de manuscrito. Esse arquivo pode ser instalado em qualquer computador que executa Windows 7 ou Windows Server 2008 R2 que dá suporte ao reconhecimento de manuscrito. Um dicionário é instalado apenas para o usuário atual ou para todos os usuários em um computador.

Um arquivo de dicionário personalizado compilado pode ser instalado na linha de comando usando a ferramenta HwrReg.exe. Essa ferramenta será útil se você quiser substituir alguns dos valores de configuração que são compilados no arquivo ou são os valores padrão. Há duas maneiras de executar HwrReg.exe: no modo de verificação/instalação e no modo de lista/remoção.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Executando HwrReg.exe no modo de verificação/instalação

Esse modo é para arquivos de dicionário personalizados que ainda não foram instalados. O exemplo a seguir mostra a sintaxe de uso para as opções de linha de comando.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Explicação das opções



| Parâmetro                | Descrição                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -check                   | O arquivo de dicionário é verificado sem ser instalado. A opção de verificação exibe o comentário do arquivo, além das informações de registro que seriam usadas para instalar o arquivo. Essa opção é útil para verificar as informações de registro antes que a instalação seja executada. <br/> Se essa opção estiver ausente, HwrReg.exe instalará o dicionário personalizado.<br/>  |
|  lang &lt; localename&gt; | O arquivo de dicionário é verificado sem ser instalado. A opção de verificação exibe o comentário do arquivo, além das informações de registro que seriam usadas para instalar o arquivo. Essa opção é útil para verificar as informações de registro antes que a instalação seja executada. <br/> Se essa opção estiver ausente, HwrReg.exe instalará o dicionário personalizado. <br/> |
|  scope {all \| me}         | O dicionário personalizado é instalado para todos os usuários (escopo todos) ou apenas para o usuário atual (escopo me). A instalação com escopo requer que o comando seja executado em um prompt de comando com elevação; caso contrário, um código de erro será retornado. <br/> Se essa opção estiver ausente, a instalação será no escopo apenas do usuário atual.<br/>                          |
|  Noprompt                | HwrReg.exe não solicita confirmação. Isso pode ser útil ao executar hwrReg.exe de um script. <br/>                                                                                                                                                                                                                                                                 |



 

O exemplo a seguir instala o dicionário personalizado myrsrc1.hwrdict para o idioma "Dinamarquês (Deçãoção)" (da DK), com o escopo padrão apenas do usuário atual.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Executando HwrReg.exe no modo de lista/remoção

Esse modo lista ou remove dicionários personalizados instalados. O exemplo a seguir mostra a sintaxe de uso para as opções de linha de comando.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Explicação das opções



| Parâmetro                | Descrição                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang &lt; localename&gt; | Os dicionários registrados apenas para esse nome de localidade são listados ou removidos. O nome &lt; do argumento local tem o formato idioma &gt; REGION. Para exemplos desse formulário, consulte Constantes e cadeias de caracteres do [identificador de idioma.](/windows/desktop/Intl/language-identifier-constants-and-strings) <br/> Se essa opção estiver ausente, os dicionários para todos os idiomas serão listados ou removidos.<br/> |
|  scope {all \| me}         | O dicionário personalizado é instalado para todos os usuários (escopo todos) ou apenas para o usuário atual (escopo me). A instalação com escopo requer que o comando seja executado em um prompt de comando com elevação; caso contrário, um código de erro será retornado. <br/> Se essa opção estiver ausente, a instalação será no escopo apenas do usuário atual.<br/>                      |
|  tipo &lt; de tipo&gt;       | Lista ou remove somente os dicionários registrados com o tipo especificado.<br/> Se essa opção estiver ausente, todos os tipos de dicionário serão listados ou removidos. Instalar ou remover um dicionário personalizado de outro tipo (como PRIMARY-COUNTRYNAME-LIST) pode afetar o reconhecimento de manuscrito em outros contextos. <br/>                                              |
|  list                    | Lista todos os dicionários instalados que corresponderem às outras opções.<br/> Se essa opção estiver ausente, a opção remove deverá ser especificada.<br/>                                                                                                                                                                                                                          |
|  remove                  | Solicita a remoção de qualquer dicionário que corresponde às outras opções.<br/> Se essa opção estiver ausente, a lista de opções deverá ser especificada.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Exemplos

O exemplo a seguir lista os dicionários que têm o idioma "Inglês (EUA)" (en US) e o tipo PRIMARY DICTIONARY e que são instalados apenas para o usuário atual.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Da mesma forma, o seguinte remove dicionários que corresponderem aos mesmos critérios.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Observações gerais sobre dicionários personalizados

-   Se você instalar dois dicionários personalizados que têm o mesmo tipo, idioma e escopo, a segunda instalação substituirá a primeira.
-   Se você instalar dois dicionários personalizados com o mesmo tipo e idioma, mas com escopos diferentes (um para todos os usuários e outro para o usuário atual), o dicionário instalado para o usuário atual tem precedência e o dicionário instalado para todos os usuários é ignorado.

 

