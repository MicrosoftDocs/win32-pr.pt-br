---
description: Uma ferramenta CryptoAPI que cria um arquivo de catálogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827251"
---
# <a name="makecat"></a>MakeCat

A ferramenta MakeCat é uma ferramenta CryptoAPI que cria um arquivo de catálogo. O MakeCat está disponível como parte do SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0 e é instalado, por padrão, na \\ pasta bin do caminho de instalação do SDK.

A ferramenta MakeCat usa a seguinte sintaxe de comando:

**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nome do arquivo*

## <a name="parameters"></a>Parâmetros



| Parâmetro             | Descrição                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-n**<br/>     | Não pare em um erro recuperável.<br/>                                                                                                                           |
| **-r**<br/>     | Força MakeCat a terminar se encontrar erros recuperáveis. Especificamente, ele terminará ao processar as entradas na seção de arquivos de catálogo de um arquivo. CDF.<br/> |
| **-v**<br/>     | Extensa. Exibe todas as mensagens de progresso e de erro.<br/>                                                                                                            |
| *FileName*<br/> | Nome do arquivo. CDF a ser analisado. Para obter a estrutura e o conteúdo necessários, consulte comentários.<br/>                                                                         |



 

## <a name="remarks"></a>Comentários

O arquivo. CDF deve ser criado com as especificações a seguir.

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> A última entrada no arquivo. CDF sempre deve ter um caractere de nova linha explícito no final da linha.

 

A \[ \] seção CatalogHeader define informações sobre o arquivo de catálogo inteiro.



| Opção                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nome<br/>           | Nome do arquivo de catálogo, incluindo sua extensão.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ResultDir<br/>      | Diretório em que o arquivo. Cat criado será colocado. Se não for indicado, o diretório atual padrão será usado. Se o diretório não existir, ele será criado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PublicVersion<br/>  | Não há suporte para essa opção. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Versão do catálogo. Se for deixado em branco, o valor padrão, 1, será usado.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CatalogVersion<br/> | Versão do catálogo. Se a versão não estiver presente ou estiver definida como 1, "0x100" será passado para o parâmetro *dwPublicVersion* da função [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e um arquivo de catálogo da versão 1 será criado. A opção HashAlgorithms deve estar vazia ou conter SHA1.<br/> Se a versão for definida como 2, "0x200" será passado para o parâmetro *dwPublicVersion* da função [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e um arquivo de catálogo da versão 2 será criado. A opção HashAlgorithms deve conter SHA256.<br/> Se essa opção estiver presente, mas contiver qualquer valor diferente de 1 ou 2, a ferramenta MakeCat apresentará um erro.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para essa opção.<br/> <br/> |
| HashAlgorithm<br/> | Nome do algoritmo de hash usado. Para obter mais informações, consulte a opção CatalogVersion.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para essa opção.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PageHashes<br/>     | Especifica se os arquivos listados na opção devem ser incluídos em hash na <HASH> \[ \] seção CatalogFiles<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para essa opção.<br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| EncodingType<br/>   | Tipo de codificação de mensagem usado. Se deixado em branco, o EncodingType padrão será a codificação \_ \_ ASN X509 de codificação ASN PKCS 7 \_ \| \_ \_ , 0x00010001. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

A \[ \] seção CatalogFiles define cada membro do arquivo de catálogo com arquivos de vários tipos e atributos de vários tipos em grupos separados.



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
<td>marca de referência<br/></td>
<td>Referência de texto para o arquivo. Isso pode incluir qualquer caractere de texto ASCII, exceto o sinal de igual (=). O sistema deve ser capaz de reproduzir essa marca após a instalação. <br/> Use <HASH> como um prefixo do nome do arquivo. Isso faz com que a marca seja o hash do arquivo no formato de cadeia de caracteres ASCII. <br/></td>
</tr>
<tr class="even">
<td>caminho e nome do arquivo<br/></td>
<td>O nome do arquivo, incluindo a extensão a ser analisada e o caminho relativo para o arquivo. Qualquer tipo de arquivo que possa ser assinado com SignTool pode ser adicionado a um catálogo. Por exemplo, os nomes de arquivo com as seguintes extensões, entre outros, podem ser adicionados a um catálogo:. exe,. cab,. Cat,. ocx,. dll e. STL.<br/></td>
</tr>
<tr class="odd">
<td>ALTSIPID<br/></td>
<td>O GUID do SIP que deve ser usado para hash em vez do SIP padrão com base no tipo de arquivo. Essa entrada é opcional. Se essa entrada for omitida, o membro será transformado em hash usando o SIP padrão. Se nenhum SIP instalado padrão for encontrado, o SIP simples será usado.<br/></td>
</tr>
<tr class="even">
<td>guid<br/></td>
<td>Representação de texto de um GUID.<br/></td>
</tr>
<tr class="odd">
<td>ATTRx<br/></td>
<td>Opcional. Atributo ou instrução sobre o arquivo ou conteúdo. Pode haver qualquer número de atributos, incluindo nenhum.<br/></td>
</tr>
<tr class="even">
<td>tipo<br/></td>
<td>Define o tipo de atributo que está sendo adicionado no formato 0x00000000 (Text). Essa opção pode ser uma combinação de bit-a-<strong>ou</strong> de zero ou mais dos seguintes valores:<br/>
<ul>
<li>0x10000000 o atributo autenticado (assinado, incluído no hash).</li>
<li>0x20000000 atributo não autenticado (não assinado, não incluído no hash, não verificável).</li>
<li>o atributo 0x01000000 não será replicado para entradas SHA1 em um catálogo CatalogVersion 2.</li>
<li>o atributo 0x00010000 é representado em texto sem formatação. Nenhuma conversão será feita.</li>
<li>o atributo 0x00020000 é representado na codificação base-64. Isso é usado para representar dados binários.</li>
<li>o atributo 0x00000001 é um par de nome-valor. Use a opção OID para o nome. Este atributo é lento; Portanto, use essa opção com moderação.</li>
<li>o atributo 0x00000002 é referenciado por um OID ( <a href="/windows/desktop/SecGloss/o-gly"><em>identificador de objeto</em></a> ).</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>oid<br/></td>
<td>A representação de texto da chave de referência do atributo. É um OID na forma de uma cadeia de caracteres de texto em notação quádrupla pontilhada (por exemplo, a. b. c. d) ou um nome de texto.<br/></td>
</tr>
<tr class="even">
<td>value<br/></td>
<td>A representação de texto do valor do atributo. O tipo de representação de texto usado depende do valor da opção Type. Os caracteres de EOL determinam o comprimento.<br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td>Aplica hash ao arquivo especificado.<br/></td>
</tr>
</tbody>
</table>



 

O arquivo de catálogo gerado não está assinado. Se ele for assinado antes da transmissão, ele será assinado usando [SignTool](signtool.md).

 

 
