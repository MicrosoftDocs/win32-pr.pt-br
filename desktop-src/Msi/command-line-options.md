---
description: Opções de linha de comando para msiexec.exe para Windows Installer 3,0 e anteriores. Fornece uma tabela mostrando opções, parâmetros e descrições. Exemplos que mostram como instalar produtos e outras tarefas.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Opções de Linha de Comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fe56026c21e4120963c86b4de08decc85b2a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752052"
---
# <a name="command-line-options"></a>Opções de Linha de Comando

O programa executável que interpreta pacotes e instala produtos é Msiexec.exe. Observe que o msiexec também define um nível de erro no retorno que corresponde aos [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes). As opções de linha de comando não diferenciam maiúsculas de minúsculas.

As opções de linha de comando na tabela a seguir estão disponíveis com Windows Installer 3,0 e versões anteriores. As [Opções de Command-Line do instalador padrão](standard-installer-command-line-options.md) também estão disponíveis a partir do Windows Installer 3,0.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Parâmetros</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/I</strong></td>
<td><em>Pacote | ProductCode</em></td>
<td>Instala ou configura um produto.<br/></td>
</tr>
<tr class="even">
<td><strong>f</strong></td>
<td>[p | o | e | d | c | a | u | m | s | v] <em>Pacote</em> | do <em>ProductCode</em></td>
<td>Repara um produto. Essa opção ignora todos os valores de propriedade inseridos na linha de comando. A lista de argumentos padrão para esta opção é ' omus '. Essa opção compartilha a mesma lista de argumentos que a propriedade <a href="reinstallmode.md"><strong>REinstallmode</strong></a> .<br/> p – reinstala somente se o arquivo estiver ausente.<br/> o-reinstala se o arquivo está ausente ou se uma versão mais antiga está instalada.<br/> e-reinstala se o arquivo está ausente ou se uma versão igual ou anterior está instalada.<br/> d – reinstala se o arquivo está ausente ou se uma versão diferente está instalada.<br/> c – reinstala se o arquivo está ausente ou a soma de verificação armazenada não corresponde ao valor calculado. Repara somente os arquivos que têm <strong>msidbFileAttributesChecksum</strong> na coluna atributos da tabela de <a href="file-table.md">arquivos</a> .<br/> a-força todos os arquivos a serem reinstalados.<br/> u-reescreve todas as entradas de Registro necessárias específicas do usuário.<br/> m-reescreve todas as entradas de Registro necessárias específicas do computador.<br/> s-substitui todos os atalhos existentes.<br/> v-executa da origem e armazena novamente em cache o pacote local. Não use a opção <strong>v</strong> REINSTALL para a primeira instalação de um aplicativo ou recurso.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Pacote</em></td>
<td>Opção de <a href="administrative-installation.md">instalação administrativa</a> . Instala um produto na rede.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Pacote | ProductCode</em></td>
<td>Desinstala um produto.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u | m] <em>Empacotador</em><br/> [u | m] <em>Pacote</em><strong>/t</strong>de<em>lista de transformação</em><br/> <em>or</em><br/> [u | m] <em>Pacote</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Anuncia um produto. Essa opção ignora todos os valores de propriedade inseridos na linha de comando.<br/> u-anuncia para o usuário atual.<br/> m-anuncia para todos os usuários do computador.<br/> identificador de linguagem g.<br/> t-aplica a transformação ao pacote anunciado.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i | w | e | a | r | u | c | m | o | p | v | x | + |! | *] Arquivo de <em>log</em></td>
<td>Grava informações de log em um arquivo de log no caminho existente especificado. O caminho para o local do arquivo de log já deve existir. O instalador não cria a estrutura de diretório para o arquivo de log. Sinalizadores indicam quais informações registrar em log. Se nenhum sinalizador for especificado, o padrão será ' iwearmo '.<br/> i-mensagens de status.<br/> w-avisos não fatais.<br/> e-todas as mensagens de erro.<br/> a-inicialização de ações.<br/> r-registros específicos da ação.<br/> solicitações de u-User.<br/> c-parâmetros iniciais da interface do usuário.<br/> m-informações de saída fatal ou de memória insuficiente.<br/> o-mensagens de espaço em disco insuficientes.<br/> p-Propriedades do terminal.<br/> v-saída detalhada.<br/> x-informações adicionais de depuração. <strong>Windows Installer 2,0:</strong> Sem suporte. A opção x está disponível com Windows Installer versão 3.0.3790.2180 e posterior.<br/> <br/> + - Anexar ao arquivo existente.<br/> ! -Libere cada linha para o log.<br/> &quot;*&quot; -Curinga, registra todas as informações, exceto as opções v e x. Para incluir as opções v e x, especifique &quot; /l* VX &quot; .<br/>
<blockquote>
[!Note]<br />
Para obter mais informações sobre todos os métodos que estão disponíveis para definir o modo de log, consulte <a href="normal-logging.md">log normal</a> na seção <a href="windows-installer-logging.md">log de Windows Installer</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>opção</strong></td>
<td><em>nome do arquivo</em>
<blockquote>
[!Note]<br />
O comprimento do <em>nome do arquivo</em> não deve ter mais de oito caracteres.
</blockquote>
<br/></td>
<td>Gera um arquivo de status do SMS. mif. Deve ser usado com as opções Install (-i), Remove (-x), instalação administrativa (-a) ou reinstalar (-f). O ISMIF32.DLL é instalado como parte do SMS e deve estar no caminho.<br/> Os campos do arquivo de status MIF são preenchidos com as seguintes informações:<br/> Fabricante- <a href="author-summary.md"> <strong>autor</strong></a><br/> Número de <a href="revision-number-summary.md"> <strong>revisão</strong> do produto</a><br/> Versão- <a href="subject-summary.md"> <strong>assunto</strong></a><br/> <a href="template-summary.md"> <strong>Modelo</strong> de localidade</a><br/> Número de série-não definido<br/> Instalação-definida por ISMIF32.DLL como &quot; DateTime&quot;<br/> InstallStatus- &quot; êxito &quot; ou &quot; falha&quot;<br/> Descrição – mensagens de erro na seguinte ordem: 1) mensagens de erro geradas pelo instalador. 2) recurso de Msi.dll se a instalação não pôde ser iniciada ou encerrada pelo usuário. 3) arquivo de mensagem de erro do sistema. 4) mensagem formatada: &quot; erro do instalador% i &quot; , em que% i é um erro retornado de Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage [;P atchpackage2</em> ]</td>
<td>Aplica um patch. Para aplicar um patch a uma imagem administrativa instalada, você deve combinar as seguintes opções:<br/> /p <em> <PatchPackage> [;p atchpackage2] </em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n | b | r | f</td>
<td>Define o <a href="user-interface-levels.md">nível da interface do usuário</a>.<br/> q, qn-sem interface do usuário<br/> QB- <a href="b-gly.md"><em>interface do usuário básica</em></a>. Use QB! para ocultar o botão <strong>Cancelar</strong> .<br/> QR- <a href="r-gly.md"><em>interface do usuário reduzida</em></a> sem caixa de diálogo modal exibida no final da instalação.<br/> QF- <a href="f-gly.md"><em>interface do usuário completa</em></a> e todas as caixas de diálogo modais <a href="fatalerror-dialog.md">FatalError</a>, <a href="userexit-dialog.md">UserExit</a>ou <a href="exit-dialog.md">Exit</a> no final.<br/> qn +-nenhuma interface do usuário, exceto uma caixa de diálogo modal exibida no final.<br/> QB +- <a href="b-gly.md"><em>interface do usuário básica</em></a> com uma caixa de diálogo modal exibida no final. A caixa modal não será exibida se o usuário cancelar a instalação. Use QB +! ou QB! + para ocultar o botão <strong>Cancelar</strong> .<br/> QB-- <a href="b-gly.md"><em>interface do usuário básica</em></a> sem caixas de diálogo modais. Observe que/QB +-não é um nível de interface do usuário com suporte. Use QB-! ou QB!-para ocultar o botão <strong>Cancelar</strong> .<br/> Observe que o! a opção está disponível com o Windows Installer 2,0 e funciona somente com a interface do usuário básica. Ele não é válido com a interface do usuário completa.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> ou <strong>/h</strong></td>
<td> </td>
<td>Exibe informações de direitos autorais para Windows Installer.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>modulo</em></td>
<td>Chama a função do sistema <strong>DllRegisterServer</strong> para registrar automaticamente os módulos passados na linha de comando. Especifique o caminho completo para a DLL. Por exemplo, para MY_FILE.DLL na pasta atual, você pode usar:<br/> <strong>msiexec/y .\MY_FILE.DLL</strong><br/> Essa opção só é usada para informações de registro que não podem ser adicionadas usando as tabelas de registro do arquivo. msi.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>modulo</em></td>
<td>Chama a função de sistema <strong>DllUnregisterServer</strong> para cancelar o registro de módulos passados na linha de comando. Especifique o caminho completo para a DLL. Por exemplo, para MY_FILE.DLL na pasta atual, você pode usar: <br/> <strong>msiexec/z .\MY_FILE.DLL</strong><br/> Essa opção só é usada para informações de registro que não podem ser removidas usando as tabelas de registro do arquivo. msi.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Anuncia uma nova instância do produto. Deve ser usado em conjunto com/t. Disponível a partir da versão Windows Installer que é fornecida com o Windows Server 2003 e o Windows XP com Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>opção</strong></td>
<td><em>ProductCode</em></td>
<td>Especifica uma instância específica do produto. Usado para identificar uma instância instalada usando o suporte a várias instâncias por meio de transformações de código do produto. Disponível a partir da versão Windows Installer fornecida com o Windows Server 2003 e o Windows XP com SP1. <br/></td>
</tr>
</tbody>
</table>



 

As opções/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a,/p,/y e/z não devem ser usadas juntas. A única exceção a essa regra é que a aplicação de patch de uma [instalação administrativa](administrative-installation.md) requer o uso de/p e/a. As opções/t,/c e/g só devem ser usadas com/j. As opções/l e/q podem ser usadas com/i,/x,/f \[ p \| o \| e \| d \| c \| a \| u \| m \| s \| v \] ,/j \[ u \| m \] ,/a e/p. A opção/n pode ser usada com/i,/f,/x e/p.

Para instalar um produto de um: \\Example.msi, instale o produto da seguinte maneira:

**msiexec/i A: \\Example.msi**

Somente [Propriedades públicas](public-properties.md) podem ser modificadas usando a linha de comando. Todos os nomes de propriedade na linha de comando são interpretados como maiúsculos, mas o valor retém a distinção entre maiúsculas e minúsculas. Se você inserir **MyProperty** em uma linha de comando, o instalador substituirá o valor de MyProperty e não o valor de **MyProperty** na tabela de propriedades. Para obter mais informações, consulte [sobre propriedades](about-properties.md).

Para instalar um produto com a propriedade definida como valor, use a sintaxe a seguir na linha de comando. Você pode colocar a propriedade em qualquer lugar, exceto entre uma opção e seu argumento.

Sintaxe correta:

**msiexec/i A: \\Example.msi propriedade = valor**

Sintaxe incorreta:

**msiexec/i PROPERTY = valor A: \\Example.msi**

Os valores de propriedade que são cadeias de caracteres literais devem ser colocados entre aspas. Inclua quaisquer espaços em branco na cadeia de caracteres entre as marcas.

**msiexec/i A: \\Example.msi Propriedade = "espaço em branco inserido"**

Para limpar uma propriedade pública usando a linha de comando, defina seu valor como uma cadeia de caracteres vazia.

**msiexec/i A: \\Example.msi Propriedade = ""**

Para seções de texto separadas por aspas literais, coloque a seção com um segundo par de aspas.

**msiexec/i A: \\Example.msi Propriedade = "Embedded" "aspas" "espaço em branco"**

O exemplo a seguir mostra uma linha de comando complicada.

**msiexec/i testdb.msi INSTALLLEVEL = 3/l \* MSI. log CompanyName = "Acme" "widgets" "e" "utensílios." ""**

O exemplo a seguir mostra as opções de anúncio. Observe que as opções não diferenciam maiúsculas de minúsculas.

**msiexec/JM msisample.msi/T Transform. MST/LIME logfile.txt**

O exemplo a seguir mostra como instalar uma nova instância de um produto a ser anunciado. Este produto é criado para dar suporte a transformações de várias instâncias.

**msiexec/JM msisample.msi/T: instance1. MST; customization. MST/c/LIME logfile.txt**

O exemplo a seguir mostra como aplicar patch em uma instância de um produto que é instalado usando transformações de várias instâncias.

**msiexec/p msipatch. msp; msipatch2. msp/n {00000001-0002-0000-0000-624474736554} /QB**

Quando você aplica patches a um produto específico, as opções/i e/p não podem ser especificadas juntas em uma linha de comando. Nesse caso, você pode aplicar patches a um produto da seguinte maneira.

**msiexec/i A: \\Example.msi patch = msipatch. msp; msipatch2. msp/QB**

A propriedade [**patch**](patch.md) não pode ser definida em uma linha de comando, quando a opção/p é usada. Se a propriedade **patch** for definida quando a opção/p for usada, o valor da propriedade **patch** será ignorado e substituído.

 

