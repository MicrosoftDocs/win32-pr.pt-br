---
description: Opções de linha de comando para msiexec.exe para Windows Instalador 3.0 e anterior. Fornece uma tabela mostrando opções, parâmetros e descrições. Exemplos que mostram como instalar produtos e outras tarefas.
ms.assetid: a70d8cc8-af47-4472-aabc-97481d97080d
title: Opções de Linha de Comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a45d59922a6c2c1d6cd0b5f8cd61b393944e23
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880626"
---
# <a name="command-line-options"></a>Opções de Linha de Comando

O programa executável que interpreta pacotes e instala produtos é Msiexec.exe. Observe que o Msiexec também define um nível de erro no retorno que corresponde aos códigos [de erro do sistema.](/windows/desktop/Debug/system-error-codes) As opções de linha de comando não são sensíveis a maiúsculas e minúsculas.

As opções de linha de comando na tabela a seguir estão disponíveis com o Windows Installer 3.0 e versões anteriores. As [opções de Command-Line standard também](standard-installer-command-line-options.md) estão disponíveis a partir do Windows Installer 3.0.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td><em>Pacote| Productcode</em></td>
<td>Instala ou configura um produto.<br/></td>
</tr>
<tr class="even">
<td><strong>/f</strong></td>
<td>[p|o|e|d|c|a|u|m|s|v] <em>Pacote</em> | <em>ProductCode</em></td>
<td>Repara um produto. Essa opção ignora os valores de propriedade inseridos na linha de comando. A lista de argumentos padrão para essa opção é 'omus'. Essa opção compartilha a mesma lista de argumentos que a <a href="reinstallmode.md"><strong>propriedade REINSTALLMODE.</strong></a><br/> p – reinstala somente se o arquivo estiver ausente.<br/> o – reinstala se o arquivo estiver ausente ou se uma versão mais antiga estiver instalada.<br/> e – reinstala se o arquivo estiver ausente ou se uma versão igual ou mais antiga estiver instalada.<br/> d – reinstala se o arquivo estiver ausente ou se uma versão diferente estiver instalada.<br/> c – reinstala se o arquivo estiver ausente ou se a verificação armazenada não corresponder ao valor calculado. Só repara arquivos que têm <strong>msidbFileAttributesChecksum</strong> na coluna Atributos da <a href="file-table.md">tabela</a> Arquivo.<br/> a – força todos os arquivos a serem reinstalados.<br/> u – reescreve todas as entradas de Registro específicas do usuário necessárias.<br/> m – reescreve todas as entradas de Registro específicas do computador necessárias.<br/> s – substitui todos os atalhos existentes.<br/> v – executa da origem e armazena em cache o pacote local. Não use a opção de reinstalação <strong>v</strong> para a primeira instalação de um aplicativo ou recurso.<br/></td>
</tr>
<tr class="odd">
<td><strong>/a</strong></td>
<td><em>Pacote</em></td>
<td><a href="administrative-installation.md">Opção de instalação</a> administrativa. Instala um produto na rede.<br/></td>
</tr>
<tr class="even">
<td><strong>/x</strong></td>
<td><em>Pacote| Productcode</em></td>
<td>Desinstala um produto.</td>
</tr>
<tr class="odd">
<td><strong>/j</strong></td>
<td>[u|m] <em>Empacotador</em><br/> [u|m] <em>Lista de</em><strong>transformação /t</strong><em>do pacote</em><br/> <em>or</em><br/> [u|m] <em>Pacote</em><strong>/g</strong><em>LanguageID</em><br/></td>
<td>Anuncia um produto. Essa opção ignora os valores de propriedade inseridos na linha de comando.<br/> u – anuncia para o usuário atual.<br/> m – anuncia a todos os usuários do computador.<br/> g – Identificador de idioma.<br/> t – Aplica a transformação ao pacote anunciado.<br/></td>
</tr>
<tr class="even">
<td><strong>/L</strong></td>
<td>[i|w|e|a|r|u|c|m|o|p|v|x|+|!| *] <em>Logfile</em></td>
<td>Grava informações de log em um arquivo de log no caminho existente especificado. O caminho para o local do logfile já deve existir. O instalador não cria a estrutura de diretório para o logfile. Sinalizadores indicam quais informações registrar. Se nenhum sinalizador for especificado, o padrão será 'i operação'.<br/> i - Mensagens de status.<br/> w - Avisos nãofatais.<br/> e - Todas as mensagens de erro.<br/> a - Iniciar de ações.<br/> r – registros específicos da ação.<br/> u - Solicitações de usuário.<br/> c – parâmetros de interface do usuário iniciais.<br/> m – informações de saída fatais ou sem memória.<br/> o – mensagens de espaço fora do disco.<br/> p - Propriedades do terminal.<br/> v – saída detalhada.<br/> x – informações adicionais de depuração. <strong>Windows Instalador 2.0:</strong> Sem suporte. A opção x está disponível com Windows Installer versão 3.0.3790.2180 e posterior.<br/> <br/> + - Anexar ao arquivo existente.<br/> ! - Liberar cada linha para o log.<br/> &quot;*&quot; - Curinga, registre todas as informações, exceto as opções v e x. Para incluir as opções v e x, &quot; especifique /l* vx &quot; .<br/>
<blockquote>
[!Note]<br />
Para obter mais informações sobre todos os métodos disponíveis para definir o modo de registro em log, consulte Registro em log <a href="normal-logging.md">normal</a> na seção registro em log do Windows <a href="windows-installer-logging.md">Instalador</a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>/m</strong></td>
<td><em>Filename</em>
<blockquote>
[!Note]<br />
O comprimento do <em>nome do arquivo</em> não deve ter mais de oito caracteres.
</blockquote>
<br/></td>
<td>Gera um arquivo .mif de status SMS. Deve ser usado com as opções install (-i), remove (-x), administrative installation (-a) ou reinstall (-f). O ISMIF32.DLL é instalado como parte do SMS e deve estar no caminho.<br/> Os campos do arquivo mif de status são preenchidos com as seguintes informações:<br/> Fabricante – <a href="author-summary.md"> <strong>Autor</strong></a><br/> Produto – <a href="revision-number-summary.md"> <strong>Número de Revisão</strong></a><br/> Versão – <a href="subject-summary.md"> <strong>Assunto</strong></a><br/> Localidade – <a href="template-summary.md"> <strong>Modelo</strong></a><br/> Número de Série – não definido<br/> Instalação – definida por ISMIF32.DLL como &quot; DateTime&quot;<br/> InstallStatus – &quot; Êxito &quot; ou &quot; Falha&quot;<br/> Descrição – Mensagens de erro na seguinte ordem: 1) Mensagens de erro geradas pelo instalador. 2) Recurso do Msi.dll se a instalação não puder iniciar ou sair do usuário. 3) Arquivo de mensagem de erro do sistema. 4) Mensagem formatada: &quot; Erro do instalador %i, em que %i é o erro &quot; retornado do Msi.dll.<br/></td>
</tr>
<tr class="even">
<td><strong>/p</strong></td>
<td><em>PatchPackage[;p atchPackage2</em> ]</td>
<td>Aplica um patch. Para aplicar um patch a uma imagem administrativa instalada, você deve combinar as seguintes opções:<br/> /p <em> &lt; PatchPackage &gt; [;p atchPackage2 ]</em> /a<em><Package></em><br/></td>
</tr>
<tr class="odd">
<td><strong>/q</strong></td>
<td>n|b|r|f</td>
<td>Define <a href="user-interface-levels.md">o nível da interface do usuário</a>.<br/> q , qn – Sem interface do usuário<br/> qb – <a href="b-gly.md"><em>Interface do usuário básica.</em></a> Use qb! para ocultar o <strong>botão</strong> Cancelar.<br/> qr – <a href="r-gly.md"><em>interface do usuário reduzida</em></a> sem caixa de diálogo modal exibida no final da instalação.<br/> qf – <a href="f-gly.md"><em>interface do usuário completa</em></a> e todas as caixas de diálogo <a href="fatalerror-dialog.md">fatalError,</a> <a href="userexit-dialog.md">UserExit</a>ou <a href="exit-dialog.md">Exit</a> modal criadas no final.<br/> qn+ – nenhuma interface do usuário, exceto uma caixa de diálogo modal exibida no final.<br/> qb+ – <a href="b-gly.md"><em>interface do usuário básica</em></a> com uma caixa de diálogo modal exibida no final. A caixa modal não será exibida se o usuário cancelar a instalação. Use qb+! ou qb!+ para ocultar o <strong>botão</strong> Cancelar.<br/> qb- – <a href="b-gly.md"><em>Interface do usuário básica</em></a> sem caixas de diálogo modais. Observe que /qb+- não é um nível de interface do usuário com suporte. Usar qb-! ou qb!- para ocultar o <strong>botão</strong> Cancelar.<br/> Observe que o ! A opção está disponível com o Windows Installer 2.0 e funciona apenas com a interface do usuário básica. Ele não é válido com a interface do usuário completa.<br/></td>
</tr>
<tr class="even">
<td><strong>/?</strong> ou <strong>/h</strong></td>
<td> </td>
<td>Exibe informações de direitos autorais para Windows Instalador.<br/></td>
</tr>
<tr class="odd">
<td><strong>/y</strong></td>
<td><em>Módulo</em></td>
<td>Chama a função de <strong>sistema DllRegisterServer para</strong> os módulos de auto-registro passados na linha de comando. Especifique o caminho completo para a DLL. Por exemplo, para MY_FILE.DLL na pasta atual, você pode usar:<br/> <strong>msiexec /y .\MY_FILE.DLL</strong><br/> Essa opção só é usada para informações do Registro que não podem ser adicionadas usando as tabelas do Registro do .msi arquivo.<br/></td>
</tr>
<tr class="even">
<td><strong>/z</strong></td>
<td><em>Módulo</em></td>
<td>Chama a função de <strong>sistema DllUnRegisterServer</strong> para não registro de módulos passados na linha de comando. Especifique o caminho completo para a DLL. Por exemplo, para MY_FILE.DLL na pasta atual, você pode usar: <br/> <strong>msiexec /z .\MY_FILE.DLL</strong><br/> Essa opção só é usada para informações do Registro que não podem ser removidas usando as tabelas do Registro do .msi arquivo.<br/></td>
</tr>
<tr class="odd">
<td><strong>/c</strong></td>

<td>Anuncia uma nova instância do produto. Deve ser usado em conjunto com /t. Disponível a partir da versão do Windows Installer que é enviada com o Windows Server 2003 e o Windows XP com o Service Pack 1 (SP1).<br/></td>
</tr>
<tr class="even">
<td><strong>/n</strong></td>
<td><em>ProductCode</em></td>
<td>Especifica uma instância específica do produto. Usado para identificar uma instância instalada usando o suporte a várias instâncias por meio de uma transformação de alteração de código do produto. Disponível a partir da versão Windows Installer do Windows Server 2003 e Windows XP com SP1. <br/></td>
</tr>
</tbody>
</table>



 

As opções /i, /x, /f \[ p o e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a, /p, /y e /z não devem ser usadas juntas. A única exceção a essa regra é que a adoção de patch de uma [instalação administrativa](administrative-installation.md) requer o uso de /p e /a. As opções /t, /c e /g só devem ser usadas com /j. As opções /l e /q podem ser usadas com /i, /x, /f \[ p o e d c a u m s \| v \| , \| \| \| \| \| \| \| \] /j u m , \[ \| \] /a e /p. A opção /n pode ser usada com /i, /f, /x e /p.

Para instalar um produto de A: \\Example.msi, instale o produto da seguinte forma:

**msiexec /i A: \\Example.msi**

Somente [propriedades públicas](public-properties.md) podem ser modificadas usando a linha de comando. Todos os nomes de propriedade na linha de comando são interpretados como maiúsculas, mas o valor retém a sensibilidade a maiúsculas e minúsculas. Se você inserir **MyProperty** em uma linha de comando, o instalador substituirá o valor de MYPROPERTY e não o valor de **MyProperty** na tabela Property. Para obter mais informações, consulte [Sobre propriedades](about-properties.md).

Para instalar um produto com PROPERTY definido como VALUE, use a sintaxe a seguir na linha de comando. Você pode colocar a propriedade em qualquer lugar, exceto entre uma opção e seu argumento.

Sintaxe correta:

**msiexec /i A: \\Example.msi PROPERTY=VALUE**

Sintaxe incorreta:

**msiexec /i PROPERTY=VALUE A: \\Example.msi**

Os valores de propriedade que são cadeias de caracteres literais devem ser entre aspas. Inclua espaços em branco na cadeia de caracteres entre as marcas.

**msiexec /i A: \\Example.msi PROPERTY="Espaço em Branco Inserido"**

Para limpar uma propriedade pública usando a linha de comando, de definido seu valor como uma cadeia de caracteres vazia.

**msiexec /i A: \\Example.msi PROPERTY=""**

Para seções de texto separadas por aspas literais, coloque a seção com um segundo par de aspas.

**msiexec /i A: \\Example.msi PROPERTY="Embedded ""Quotes"" White Space"**

O exemplo a seguir mostra uma linha de comando complicada.

**msiexec /i testdb.msi INSTALLLEVEL=3 /l \* msi.log COMPANYNAME="Acme ""Widgets" e ""Gizmos."""**

O exemplo a seguir mostra as opções de anúncio. Observe que as opções não são sensíveis a minúsculas.

**msiexec /JM msisample.msi /T transform.mst /LIME logfile.txt**

O exemplo a seguir mostra como instalar uma nova instância de um produto a ser anunciado. Este produto é autor para dar suporte a várias transformações de instância.

**msiexec /JM msisample.msi /T :instance1.mst;customization.mst /c /LIME logfile.txt**

O exemplo a seguir mostra como corrigir uma instância de um produto que é instalado usando várias transformações de instância.

**msiexec /p msipatch.msp;msipatch2.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Quando você aplica patches a um produto específico, as opções /i e /p não podem ser especificadas juntas em uma linha de comando. Nesse caso, você pode aplicar patches a um produto da seguinte forma.

**msiexec /i A: \\Example.msi PATCH=msipatch.msp;msipatch2.msp /qb**

A [**propriedade PATCH**](patch.md) não pode ser definida em uma linha de comando, quando a opção /p é usada. Se a **propriedade PATCH** for definida quando a opção /p for usada, o valor da propriedade **PATCH** será ignorado e substituído.

 

