---
description: O Mt.exe é uma ferramenta que gera arquivos e catálogos assinados. Ele está disponível no SDK (Software Development Kit) do Microsoft Windows. Mt.exe requer que o arquivo referenciado no manifesto estar presente no mesmo diretório que o manifesto.
ms.assetid: 37f010ee-2658-4547-9871-c913201042de
title: Mt.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f18f3d60a7ad20298473ab1d65b2e1d07720bf54130dd66cb361fa5d220c357
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884996"
---
# <a name="mtexe"></a>Mt.exe

O Mt.exe é uma ferramenta que gera arquivos e catálogos assinados. Ele está disponível no SDK (Software Development Kit) do Microsoft Windows. Mt.exe requer que o arquivo referenciado no manifesto estar presente no mesmo diretório que o manifesto.

Mt.exe gera hashes usando a implementação de CryptoAPI do SHA-1 (Secure Hash Algorithm). Para obter mais informações sobre algoritmos de hash, consulte [Algoritmos de hash e assinatura.](/windows/desktop/SecCrypto/hash-and-signature-algorithms) Os hashes são inseridos como uma cadeia de caracteres hexadecimal nas marcas **de** arquivo no manifesto. Atualmente, a ferramenta gera apenas hashes SHA-1, embora os arquivos nos manifestos possam usar outros esquemas de hash.

Mt.exe usa Makecat.exe para gerar arquivos de catálogo (.cat) de arquivos de definição de catálogo (.cdf). Essa ferramenta preenche um CDF de modelo padrão com o nome e o local do manifesto. Você pode usar isso com Makecat.exe para gerar o catálogo de assembly.

A versão do Mt.exe fornecida em versões recentes do SDK do Windows também pode ser usada para gerar manifestos para assemblies gerenciados e assemblies não gerenciados lado a lado.

## <a name="syntax"></a>Syntax

**mt.exe \[ -manifest** _<component1.manifest><component2.manifest>_ *_\] \[ -identity:_* *<identity string> * **\] \[ -rgs:**<_file1.rgs>_* _\] \[ -tlb:_<*_file2.tlb>_* _\] \[ -dll:_ *_<file3.dll>_* _\] \[ -replacements:_ *_<XML filename>_* _\] \[ -managedassemblyname:_ *_<managed assembly>_* _\] \[ -nodependency \] \[ -category \] \[ -out:_ *_<output manifest name>_* _\] \[ -inputresource:_ *_<file4>_* _; \[ \# \]_ *_><0 \_ id do recurso><1_* _\] \[ -outputresource:_ *_<file5>_* _; \[ \# \]_ *_><2 \_ id do recurso><3_* _\] \[ -updateresource:_ *_<file6>_* _; \[ \# \]_ *_><4 \_ id_* de recurso><5 _\] \[ -hashupdate: \[_ *_<path to files>_* _\] \] \[ -makecdfs \] \[ -validate \_ manifest \] \[ -validate \_ file \_ hashes:_ *_<path to files>_* _\] \[ -canonicalize \] \[ -check \_ for \_ duplicates \] \[ -nologo \] \[ -verbose \]_*

## <a name="command-line-options"></a>Opções de linha de comando

Mt.exe usa as seguintes opções de linha de comando sem valor de maiúsculas e minúsculas.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-manifest</td>
<td>Especifica o nome do arquivo de manifesto. Para modificar um único manifesto, especifique um nome de arquivo de manifesto. Por exemplo, component.manifest.<br/> Para mesclar vários manifestos, especifique os nomes dos manifestos de origem aqui. Especifique o nome do manifesto atualizado com as opções <strong>-out</strong>, <strong>-outputresource</strong>ou <strong>-updateresource.</strong> Por exemplo, a linha de comando a seguir solicita uma operação que mescla dois manifestos, man1.manifest e man2.manifest, em um novo manifesto, man3.manifest.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -out:man3.manifest</strong><br/>
<blockquote>
[!Note]<br />
Nenhum dois-pontos (:) é necessário com a <strong>opção -manifest.</strong>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>-identity</td>
<td>Fornece os valores de atributos do <strong>elemento assemblyIdentity</strong> do manifesto. O argumento da opção <strong>-identity</strong> é um valor de cadeia de caracteres que contém os valores de atributo em campos separados por vírgulas. Forneça o valor do <strong>atributo name</strong> no primeiro campo, sem incluir uma &quot; &quot; substring name=. Todos os campos restantes especificam os atributos e seus valores usando o formulário : <em> <attribute name> </em> = <em> <attribute_value> </em> .<br/> Por exemplo, para atualizar o <strong>elemento assemblyIdentity</strong> do manifesto com as seguintes informações:<br/> <assemblyIdentity type=&quot;win32&quot; name=&quot;Microsoft.Windows.SampleAssembly&quot; version=&quot;6.0.0.0&quot; processorArchitecture=&quot;x86&quot; publicKeyToken=&quot;a5aaf5ba15723d5&quot;/> <br/> inclua a seguinte <strong>opção -identity</strong> na linha de comando:<br/> <strong>-identity:</strong> &quot; Microsoft. Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5&quot;<br/></td>
</tr>
<tr class="odd">
<td>-rgs</td>
<td>Especifica o nome do arquivo de script de registro (.rgs). A <strong>opção -dll</strong> é necessária para usar a <strong>opção -rgs.</strong><br/></td>
</tr>
<tr class="even">
<td>-tlb</td>
<td>Especifica o nome do arquivo de biblioteca de tipos (.tlb). A <strong>opção -dll</strong> é necessária para usar a <strong>opção -tlb.</strong><br/></td>
</tr>
<tr class="odd">
<td>-dll</td>
<td>Especifica o nome do arquivo DLL (biblioteca de vínculo dinâmico). A <strong>opção -dll</strong> é necessária para <strong>mt.exe</strong> se as <strong>opções -rgs</strong> ou <strong>-tlb</strong> são usadas. Especifique o nome da DLL que você pretende eventualmente criar com base nos arquivos .rgs ou .tlb.<br/> Por exemplo, o comando a seguir solicita uma operação que gera um manifesto de arquivos .rgs e .tlb.<br/> <strong>mt.exe -rgs:testreg1.rgs -tlb:testlib1.tlb -dll:test.dll -replacements:rep.manifest -identity: &quot; Microsoft.Windows. SampleAssembly, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=a5aaf5ba15723d5 &quot; -out:rgstlb.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-replacements</td>
<td>Especifica o arquivo que contém valores para a cadeia de caracteres substituível no arquivo .rgs.<br/></td>
</tr>
<tr class="odd">
<td>-managedassemblyname</td>
<td>Gera um manifesto do assembly gerenciado especificado. Use com a <strong>opção -nodependency</strong> para gerar um manifesto sem elementos de dependência. Use com a <strong>opção -category</strong> para gerar um manifesto com marcas de categoria. Por exemplo, se managed.dll for um assembly gerenciado, a linha de comando a seguir gerará o out.manifest de managed.dll.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest</strong> <br/></td>
</tr>
<tr class="even">
<td>-nodependency</td>
<td>Especifica uma operação que gera um manifesto sem elementos de dependência. A <strong>opção -nodependency</strong> requer a <strong>opção -managedassemblyname.</strong> Por exemplo, se managed.dll for um assembly gerenciado, a linha de comando a seguir gerará o out.manifest de managed.dll sem informações de dependência.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -nodependency</strong><br/></td>
</tr>
<tr class="odd">
<td>-category</td>
<td>Especifica uma operação que gera um manifesto com marcas de categoria. A <strong>opção -category</strong> requer a <strong>opção -managedassemblyname.</strong> Por exemplo, se managed.dll é um assembly gerenciado, a linha de comando a seguir gera o out.manifest de managed.dll com marcas de categoria.<br/> <strong>mt.exe -managedassemblyname:managed.dll -out:out.manifest -category</strong><br/></td>
</tr>
<tr class="even">
<td>-nologo</td>
<td>Especifica uma operação que é executado sem exibir dados de direitos autorais padrão da Microsoft. Se <strong>mt.exe</strong> é executado como parte de um processo de build, essa opção pode ser usada para impedir a escrita de informações indesejadas nos arquivos de log. <br/></td>
</tr>
<tr class="odd">
<td>-out</td>
<td>Especifica o nome do manifesto atualizado. Se essa for uma operação de manifesto único e a <strong>opção -out</strong> for omitida, o manifesto original será modificado. <br/></td>
</tr>
<tr class="even">
<td>-inputresource</td>
<td>Especifica uma operação executada em um manifesto obtido de um recurso do tipo RT_MANIFEST. Se a <strong>opção -inputresource</strong> for usada sem especificar o identificador de recurso, , a operação usará o <em> <resource_id> </em> valor CREATEPROCESS_MANIFEST_RESOURCE. <br/> Por exemplo, o comando a seguir solicita uma operação que mescla um manifesto de uma DLL, dll_with_manifest.dll e um arquivo de manifesto, man2.manifest. Os manifestos mesclados são recebidos por um manifesto no arquivo de recurso de outra DLL, dll_with_merged_manifests. <br/> <strong>mt.exe -inputresource:dll_with_manifest.dll;#1 -manifest man2.manifest -outputresource:dll_with_merged_manifest.dll;#3</strong><br/> Para extrair o manifesto de uma DLL, especifique o nome do arquivo DLL. Por exemplo, o comando a seguir extrai o manifesto de lib1.dll e man3.manifest recebe o manifesto extraído.<br/> <strong>mt.exe -inputresource:lib.dll;#1 -out:man3.manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-outputresource</td>
<td>Especifica uma operação que gera um manifesto a ser recebido por um recurso do tipo RT_MANIFEST. Se a <strong>opção -outputresource</strong> for usada sem especificar o identificador de recurso, , a operação <em> <resource_id> </em> usará o valor CREATEPROCESS_MANIFEST_RESOURCE. <br/></td>
</tr>
<tr class="even">
<td>-updateresource</td>
<td>Especifica uma operação equivalente a usar as opções <strong>-inputresource</strong> e <strong>-outputresource</strong> com argumentos idênticos. Por exemplo, o comando a seguir solicita uma operação que calcula um hash dos arquivos no caminho especificado e atualiza o manifesto de um recurso de pe (executável portátil).<br/> <strong>mt.exe -updateresource:dll_with_manifest.dll;#1 -hashupdate:f:\files</strong>.<br/></td>
</tr>
<tr class="odd">
<td>-hashupdate</td>
<td>Calcula o valor de hash dos arquivos nos caminhos especificados e atualiza o valor do <strong>atributo hash</strong> do elemento <strong>File</strong> com esse valor. <br/> Por exemplo, o comando a seguir solicita uma operação que mescla dois arquivos de manifesto, man1.manifest e man2.manifest, e atualiza o valor do atributo <strong>hash</strong> do elemento <strong>File</strong> no manifesto que recebe as informações mescladas, merged.manifest.<br/> <strong>mt.exe -manifest man1.manifest man2.manifest -hashupdate:d:\filerepository -out:merged.manifest</strong><br/> Se os caminhos para os arquivos não são especificados, a operação pesquisa o local do manifesto especificado para receber a atualização. Por exemplo, o comando a seguir solicita uma operação que calcula o valor de hash atualizado usando arquivos encontrados pesquisando o local de updated.manifest.<br/> <strong>mt.exe -manifest yourComponent.manifest -hashupdate -out:updated.manifest</strong><br/></td>
</tr>
<tr class="even">
<td>-validate_manifest</td>
<td>Especifica uma operação que executa uma verificação de sintaxe da conformidade do manifesto com o esquema de manifesto. Por exemplo, o comando a seguir solicita uma verificação para validar a conformidade do man1. manifest com seu esquema. <br/> <strong>mt.exe-manifest man1. manifest-validate_manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-validate_file_hashes</td>
<td>Especifica uma operação que valida os valores de hash dos elementos de <strong>arquivo</strong> do manifesto. Por exemplo, o comando a seguir solicita uma operação que valida os valores de hash de todos os elementos de <strong>arquivo</strong> do man1. manifest.<br/> <strong>mt.exe-manifest man1. manifest-validate_file_hashes: &quot; c; \files&quot;</strong><br/></td>
</tr>
<tr class="even">
<td>-canonize</td>
<td>Especifica uma operação para atualizar o manifesto para o formulário canônico. Por exemplo, o comando a seguir atualiza man1. manifest para o formato canônico.<br/> <strong> Manifesto demt.exe man1. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-check_for_duplicates</td>
<td>Especifica uma operação que verifica o manifesto em busca de elementos duplicados. Por exemplo, o comando a seguir verifica man1. manifest em busca de elementos duplicados.<br/> <strong>mt.exe-man1. manifest-check_for_duplicates</strong><br/></td>
</tr>
<tr class="even">
<td>-makecdfs</td>
<td>Gera arquivos. CDF para criar catálogos. Por exemplo, para o comando a seguir, você solicita uma operação que atualiza o valor de hash e gera um arquivo. CDF.<br/> <strong>mt.exe-manifest comp1. manifest-hashupdate-makecdfs-out: atualizado. manifest</strong><br/></td>
</tr>
<tr class="odd">
<td>-verbose</td>
<td>Exibe informações detalhadas de depuração.</td>
</tr>
<tr class="even">
<td>-?</td>
<td>Quando executado com-?, ou sem opções e argumentos, Mt.exe exibe o texto de ajuda.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento lado a lado do assembly](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

