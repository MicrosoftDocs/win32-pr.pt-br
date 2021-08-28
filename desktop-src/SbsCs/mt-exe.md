---
description: O arquivo de Mt.exe é uma ferramenta que gera catálogos e arquivos assinados. ele está disponível no SDK (Software Development Kit) do Microsoft Windows. Mt.exe requer que o arquivo referenciado no manifesto esteja presente no mesmo diretório que o manifesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7f963c5131606da3f7be80185fef84a750e4de
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882066"
---
# <a name="mtexe"></a>Mt.exe

O arquivo de Mt.exe é uma ferramenta que gera catálogos e arquivos assinados. ele está disponível no SDK (Software Development Kit) do Microsoft Windows. Mt.exe requer que o arquivo referenciado no manifesto esteja presente no mesmo diretório que o manifesto.

Mt.exe gera hashes usando a implementação de CryptoAPI do algoritmo de hash seguro (SHA-1). Para obter mais informações sobre algoritmos de hash, consulte [hash e algoritmos de assinatura](/windows/desktop/SecCrypto/hash-and-signature-algorithms). Os hashes são inseridos como uma cadeia de caracteres hexadecimal nas marcas de **arquivo** no manifesto. Atualmente, a ferramenta gera somente hashes SHA-1, embora arquivos em manifestos possam usar outros esquemas de hash.

Mt.exe usa Makecat.exe para gerar arquivos de catálogo (. cat) a partir de arquivos de definição de catálogo (. CDF). Essa ferramenta preenche um CDF de modelo padrão com o nome e o local do seu manifesto. Você pode usar isso com Makecat.exe para gerar o catálogo do assembly.

a versão do Mt.exe fornecida em versões recentes do SDK do Windows também pode ser usada para gerar manifestos para assemblies gerenciados e assemblies lado a lado não gerenciados.

## <a name="syntax"></a>Syntax

**mt.exe \[ -manifest** _<Component1. manifest><component2. manifest>_ *_\] \[ -Identity:_* *<identity string> * **\] \[ -RGS:** _<arquivo1. rgs>_* _\] \[ -tlb:_ *_<arquivo2. tlb>_* _\] \[ -dll:_ *_<file3.dll_*>_\] \[ -Replacement:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -Category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_*_&lt; Arquivo4 &gt;_*_; \[ \# \]_ *_ID do recurso de><0 \_><1_* _\] \[ -outputresource:_*_&lt; arquivo5 &gt;_*_; \[ \# \]_ *_ID do recurso de><2 \_><3_* _\] \[ -UpdateResource:_*_&lt; file6 &gt;_*_; \[ \# \]_ *_ID do recurso de><4 \_><5_* _\] \[ -hashupdate \[ :_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -validar \_ manifesto \] \[ -validar \_ \_ hashes de arquivo:_ *_<path to files>_* _\] \[ -canonize \] \[ -Verifique se \_ há \_ duplicatas \] \[ – sem logotipo \] \[ -detalhado \]_*

## <a name="command-line-options"></a>Opções de linha de comando

Mt.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifesto</td>
<td>Especifica o nome do arquivo de manifesto. Para modificar um único manifesto, especifique um nome de arquivo de manifesto. Por exemplo, Component. manifest.<br/> Para mesclar vários manifestos, especifique os nomes dos manifestos de origem aqui. Especifique o nome do manifesto atualizado com as opções <strong>-out</strong>, <strong>-outputresource</strong>ou <strong>-UpdateResource</strong> . Por exemplo, a linha de comando a seguir solicita uma operação que mescla dois manifestos, man1. manifest e man2. manifest, em um novo manifesto, man3. manifest.<br/> <strong>mt.exe-manifest man1. manifest man2. manifest-out: man3. manifest</strong><br/>
<blockquote>
[!Note]<br />
Sem dois-pontos (:) é necessário com a opção <strong>-manifest</strong> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identidade</td>
<td>Fornece os valores de atributos do elemento <strong>AssemblyIdentity</strong> do manifesto. O argumento da opção <strong>-Identity</strong> é um valor de cadeia de caracteres que contém os valores de atributo em campos separados por vírgulas. Forneça o valor do atributo <strong>Name</strong> no primeiro campo, sem incluir um &quot; name = &quot; substring. Todos os campos restantes especificam os atributos e seus valores usando o formulário: <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Por exemplo, para atualizar o elemento <strong>AssemblyIdentity</strong> do manifesto com as seguintes informações:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> inclua a seguinte opção de <strong>identidade</strong> na linha de comando:<br/> <strong>-identidade:</strong> &quot; O. Windows. SampleAssembly, processorArchitecture = x86, versão = 6.0.0.0, tipo = Win32, publicKeyToken = a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-RGS</td>
<td>Especifica o nome do arquivo de script de registro (. rgs). A opção <strong>-dll</strong> é necessária para usar a opção <strong>-RGS</strong> .<br/></td>
</tr>
<tr class="even">
<td>-tlb</td>
<td>Especifica o nome do arquivo de biblioteca de tipos (.tlb). A opção <strong>-dll</strong> é necessária para usar a opção <strong>-tlb</strong> .<br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Especifica o nome do arquivo da biblioteca de vínculo dinâmico (DLL). A opção <strong>-dll</strong> é necessária por <strong>mt.exe</strong> se as opções <strong>-RGS</strong> ou <strong>-tlb</strong> forem usadas. Especifique o nome da DLL que você pretende compilar eventualmente por meio dos arquivos. rgs ou. tlb.<br/> Por exemplo, o comando a seguir solicita uma operação que gera um manifesto de arquivos. rgs e. tlb.<br/> <strong>mt.exe-RGS: testreg1. rgs-tlb: testlib1. tlb -dll:test.dll-substituições: Rep. manifest-Identity: &quot; Microsoft. Windows. SampleAssembly, processorArchitecture = x86, versão = 6.0.0.0, tipo = Win32, publicKeyToken = a5aaf5ba15723d5 &quot; -out: rgstlb. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-substituições</td>
<td>Especifica o arquivo que contém valores para a cadeia de caracteres substituível no arquivo. rgs.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Gera um manifesto do assembly gerenciado especificado. Use com a opção <strong>-nodependency</strong> para gerar um manifesto sem elementos de dependência. Use com a opção <strong>-Category</strong> para gerar um manifesto com marcas de categoria. Por exemplo, se managed.dll for um assembly gerenciado, a linha de comando a seguir gerará o out. manifest do managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll-out: out. manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Especifica uma operação que gera um manifesto sem elementos de dependência. A opção <strong>-nodependency</strong> requer a opção <strong>-managedassemblyname</strong> . Por exemplo, se managed.dll for um assembly gerenciado, a linha de comando a seguir gerará o out. manifest de managed.dll sem informações de dependência.<br/> <strong>mt.exe -managedassemblyname:managed.dll-out: out. manifest-nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-Categoria</td>
<td>Especifica uma operação que gera um manifesto com marcas de categoria. A opção <strong>-Category</strong> requer a opção <strong>-managedassemblyname</strong> . Por exemplo, se managed.dll for um assembly gerenciado, a linha de comando a seguir gerará o out. manifest de managed.dll com marcas de categoria.<br/> <strong>mt.exe -managedassemblyname:managed.dll-out: out. manifest – categoria</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Especifica uma operação que é executada sem exibir dados padrão de direitos autorais da Microsoft. Se <strong>mt.exe</strong> for executado como parte de um processo de compilação, essa opção poderá ser usada para evitar a gravação de informações indesejadas nos arquivos de log. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Especifica o nome do manifesto atualizado. Se essa for uma operação de manifesto único e a opção <strong>-out</strong> for omitida, o manifesto original será modificado. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Especifica uma operação executada em um manifesto obtido de um recurso do tipo RT_MANIFEST. Se a opção <strong>-inputresource</strong> for usada sem especificar o identificador de recurso, <em> <resource_id> </em> a operação usará o valor CREATEPROCESS_MANIFEST_RESOURCE. <br/> Por exemplo, o comando a seguir solicita uma operação que mescla um manifesto de uma DLL, dll_with_manifest.dll e um arquivo de manifesto, man2. manifest. Os manifestos mesclados são recebidos por um manifesto no arquivo de recurso de outra DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll; #1 do manifesto man2. manifest -outputresource:dll_with_merged_manifest.dll; #3</strong><br/> Para extrair o manifesto de uma DLL, especifique o nome do arquivo DLL. Por exemplo, o comando a seguir extrai o manifesto de lib1.dll e man3. manifest recebe o manifesto extraído.<br/> <strong>mt.exe -inputresource:lib.dll; #1-out: man3. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Especifica uma operação que gera um manifesto a ser recebido por um recurso do tipo RT_MANIFEST. Se a opção <strong>-outputresource</strong> for usada sem especificar o identificador de recurso, <em> <resource_id> </em> a operação usará o valor CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-UpdateResource</td>
<td>Especifica uma operação que é equivalente a usar as opções <strong>-inputresource</strong> e <strong>-outputresource</strong> com argumentos idênticos. Por exemplo, o comando a seguir solicita uma operação que computa um hash dos arquivos no caminho especificado e atualiza o manifesto de um recurso de um executável portátil (PE).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll; #1-hashupdate: f: \files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Computa o valor de hash dos arquivos nos caminhos especificados e atualiza o valor do atributo de <strong>hash</strong> do elemento <strong>File</strong> com esse valor. <br/> Por exemplo, o comando a seguir solicita uma operação que mescla dois arquivos de manifesto, man1. manifest e man2. manifest, e atualiza o valor do atributo de <strong>hash</strong> do elemento <strong>File</strong> no manifesto que recebe as informações mescladas, mergeted. manifest.<br/> <strong>mt.exe-manifest man1. manifest man2. manifest-hashupdate: d: \filerepository-out: mesclated. manifest</strong><br/> Se os caminhos para os arquivos não forem especificados, a operação pesquisará o local do manifesto especificado para receber a atualização. Por exemplo, o comando a seguir solicita uma operação que computa o valor de hash atualizado usando os arquivos encontrados pesquisando o local do arquivo. manifest atualizado.<br/> <strong>mt.exe-manifest yourComponent. manifest-hashupdate-out: atualizado. manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Especifica uma operação que executa uma verificação de sintaxe da conformidade do manifesto com o esquema de manifesto. Por exemplo, o comando a seguir solicita uma verificação para validar a conformidade de man1.manifest com seu esquema. <br/> <strong>mt.exe -manifest man1.manifest -validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Especifica uma operação que valida os valores de hash dos <strong>elementos File</strong> do manifesto. Por exemplo, o comando a seguir solicita uma operação que valida os valores de hash de todos os elementos <strong>File</strong> do man1.manifest.<br/> <strong>mt.exe -manifest man1.manifest -validate_file_hashes: &quot; c;\files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonicalize</td>
<td>Especifica uma operação para atualizar o manifesto para a forma canônica. Por exemplo, o comando a seguir atualiza man1.manifest para forma canônica.<br/> <strong>mt.exe -manifest man1.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Especifica uma operação que verifica o manifesto quanto a elementos duplicados. Por exemplo, o comando a seguir verifica man1.manifest para elementos duplicados.<br/> <strong>mt.exe -man1.manifest -check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Gera arquivos .cdf para criar catálogos. Por exemplo, para o comando a seguir solicita uma operação que atualiza o valor de hash e gera um arquivo .cdf.<br/> <strong>mt.exe -manifest comp1.manifest -hashupdate -makecdfs -out:updated.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Exibe informações detalhadas de depuração.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Quando executado com -?, ou sem opções e argumentos, Mt.exe exibe o texto da ajuda.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento de assembly lado a lado](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

