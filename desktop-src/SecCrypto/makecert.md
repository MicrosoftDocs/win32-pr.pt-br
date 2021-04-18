---
description: Cria um certificado X. 509, assinado pela chave raiz de teste ou outra chave especificada, que associa seu nome à parte pública do par de chaves. O certificado é salvo em um arquivo, um repositório de certificados do sistema ou ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980ba379688f2dc61c44b06d66ed5255e5b2e988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811054"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> O MakeCert foi preterido. Para criar certificados autoassinados, use o cmdlet do PowerShell [New-SelfSignedCertificate](/powershell/module/pkiclient/new-selfsignedcertificate).

 

A ferramenta MakeCert cria um certificado [*X. 509*](../secgloss/x-gly.md) , assinado pela chave raiz de teste ou outra chave especificada, que associa seu nome à parte pública do par de chaves. O certificado é salvo em um arquivo, um repositório de certificados do sistema ou ambos. A ferramenta é instalada na \\ pasta bin do caminho de instalação do SDK (Software Development Kit) do Microsoft Windows.

A ferramenta MakeCert usa a seguinte sintaxe de comando:

**MakeCert** \[ *Basicoptions* \| *Extended* \] *Arquivo_de_saída*

*Arquivo_de_saída* é o nome do arquivo no qual o certificado será gravado. Você pode omitir o *arquivo_de_saída* se o certificado não for gravado em um arquivo.

## <a name="options"></a>Opções

O MakeCert inclui opções básicas e estendidas. As opções básicas são as mais comuns para criar um certificado. As opções estendidas dão mais flexibilidade.

As opções para MakeCert também são divididas em três grupos funcionais:

-   Opções básicas específicas somente para a tecnologia de repositório de certificados.
-   Opções estendidas específicas somente para o SPC-File e a tecnologia de chave privada.
-   Opções estendidas aplicáveis à tecnologia de arquivo SPC, chave privada e repositório de certificados.

As opções fornecidas nas tabelas a seguir podem ser usadas somente com o Internet Explorer 4,0 ou posterior.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção básica</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-a</strong> <strong></strong> <em>Algoritmo</em> do</td>
<td>Algoritmo de <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> . Deve ser definido como <strong>SHA-1</strong> ou <strong>MD5</strong> (padrão). Para obter informações sobre MD5, consulte <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-b</strong> <strong></strong> <em>DateStart</em></td>
<td>Data em que o certificado se torna válido pela primeira vez. O padrão é quando o certificado é criado. O formato de <em>DateStart</em> é mm/dd/aaaa.</td>
</tr>
<tr class="odd">
<td><strong>-CY</strong> <strong></strong> <em>CertificateTypes</em></td>
<td>Tipo de certificado. <em>CertificateTypes</em> pode ser <strong>end</strong> para a entidade end ou <strong>autoridade</strong> para <a href="/windows/desktop/SecGloss/c-gly"><em>autoridade de certificação</em></a>.</td>
</tr>
<tr class="even">
<td><strong>-e</strong> <strong></strong> <em>DateEnd</em></td>
<td>Data em que o período de validade termina. O padrão é o ano 2039.</td>
</tr>
<tr class="odd">
<td><strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong> <em>OID2</em> ...</td>
<td>Insere uma lista de um ou mais OIDs ( <a href="/windows/desktop/SecGloss/o-gly"><em>identificadores de objeto</em></a> ) de <a href="/windows/desktop/SecGloss/e-gly"><em>uso avançado de chave</em></a> separados por vírgula no certificado. Por exemplo, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> insere o OID de autenticação de cliente. Para obter definições de OIDs permitidos, consulte o arquivo Wincrypt. h em CryptoAPI 2.0.</td>
</tr>
<tr class="even">
<td><strong>-h</strong> <strong></strong> <em>NumChildren</em></td>
<td>Altura máxima da árvore abaixo deste certificado.</td>
</tr>
<tr class="odd">
<td><strong>-l</strong> <strong></strong> <em>PolicyLink</em></td>
<td>Link para informações de política do SPC Agency (por exemplo, uma URL).</td>
</tr>
<tr class="even">
<td><strong>-m</strong> <strong></strong> <em>nMonths</em></td>
<td>Duração do período de validade.</td>
</tr>
<tr class="odd">
<td><strong>-n</strong> <strong>&quot;</strong> <em>Nome</em> do<strong>&quot;</strong></td>
<td>Nome do certificado do editor. Esse nome deve estar em conformidade com o padrão <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> . O método mais simples é usar o &quot; formato CN =<em>myname</em> &quot; . Por exemplo: <strong>-n &quot; CN = test &quot; </strong>.</td>
</tr>
<tr class="even">
<td><strong>-nscp</strong></td>
<td>A extensão de autenticação de cliente do Netscape deve ser incluída.</td>
</tr>
<tr class="odd">
<td><strong>-PE</strong></td>
<td>Marca a chave privada como exportável.</td>
</tr>
<tr class="even">
<td><strong>-r</strong></td>
<td>Cria um certificado autoassinado.</td>
</tr>
<tr class="odd">
<td><strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em></td>
<td>Nome do arquivo de certificado com a chave pública de entidade existente a ser usada.</td>
</tr>
<tr class="even">
<td><strong>-SK</strong> <strong></strong> <em>SubjectKey</em></td>
<td>Local do contêiner de chave da entidade que contém a <a href="/windows/desktop/SecGloss/p-gly"><em>chave privada</em></a>. Se um contêiner de chave não existir, um será criado. Se nem a opção <strong>-SK</strong> ou <strong>-SV</strong> for usada, um contêiner de chave padrão será criado e usado por padrão.</td>
</tr>
<tr class="odd">
<td><strong>-céu</strong> <strong></strong> <em>SubjectKeySpec</em></td>
<td>Especificação da chave da entidade. <em>SubjectKeySpec</em> deve ser um dos três valores possíveis:<br/>
<ul>
<li><strong>Assinatura</strong> (AT_SIGNATURE especificação de chave)</li>
<li><strong>Troca</strong> (AT_KEYEXCHANGE especificação de chave)</li>
<li>Um inteiro, como <strong>3</strong></li>
</ul>
Para obter mais informações, consulte a observação que segue esta tabela.<br/></td>
</tr>
<tr class="even">
<td><strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em></td>
<td>Provedor de CryptoAPI para o assunto. O padrão é o provedor do usuário. Para obter informações sobre provedores de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em></td>
<td>Local do registro do repositório de certificados da entidade. <em>SubjectCertStoreLocation</em> deve ser <strong>LocalMachine</strong> (chave do registro HKEY_LOCAL_MACHINE) ou <strong>CurrentUser</strong> (chave do registro HKEY_CURRENT_USER). <strong>CurrentUser</strong> é o padrão.</td>
</tr>
<tr class="even">
<td><strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em></td>
<td>Nome do repositório de certificados da entidade em que o certificado gerado será armazenado.</td>
</tr>
<tr class="odd">
<td><strong>-VA</strong> <strong></strong> <em>SubjectKeyFile</em></td>
<td>Nome do arquivo. pvk da entidade. Se nem a opção <strong>-SK</strong> ou <strong>-SV</strong> for usada, um contêiner de chave padrão será criado e usado por padrão.</td>
</tr>
<tr class="even">
<td><strong>-Sy</strong> <strong></strong> <em>nSubjectProviderType</em></td>
<td>Tipo de provedor de CryptoAPI para o assunto. O padrão é <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Para obter informações sobre tipos de provedor de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-#</strong><strong></strong> <em>SerialNumber</em></td>
<td>Número de série do certificado. O valor máximo é 2 ^ 31. O padrão é um valor gerado pela ferramenta que tem a garantia de ser exclusivo.</td>
</tr>
<tr class="even">
<td><strong>-$</strong><strong></strong> <em>CertificateAuthority</em></td>
<td>Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>autoridade de certificação</em></a>. O <em>CertificateAuthority</em> deve ser definido como <strong>comercial</strong> (para certificados a serem usados por editores de software comercial) ou <strong>individual</strong> (para certificados a serem usados por editores de software individuais).</td>
</tr>
<tr class="odd">
<td><strong>-?</strong></td>
<td>Exibe as opções básicas.</td>
</tr>
<tr class="even">
<td><strong>-!</strong></td>
<td>Exibe as opções estendidas.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se a opção de especificação de chave **-céu** for usada no Internet Explorer versão 4,0 ou posterior, a especificação deverá corresponder à especificação de chave indicada pelo arquivo de [*chave privada*](../secgloss/p-gly.md) ou pelo [*contêiner de chave*](../secgloss/k-gly.md)privada. Se a opção de especificação de chave não for usada, a especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de chave privada será usada. Se houver mais de uma especificação de chave no contêiner de chave, o MakeCert tentará primeiro usar a \_ especificação de chave de assinatura at. Se isso falhar, o MakeCert tentará usar AT \_ Exchange. Como a maioria dos usuários tem uma \_ chave de assinatura at ou uma \_ chave de troca de chaves, essa opção não precisa ser usada na maioria dos casos.

 

As opções a seguir são apenas para arquivos SPC ( [*certificado do fornecedor de software*](../secgloss/s-gly.md) ) e tecnologia de chave privada.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção SPC e chave privada</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>-IC</strong> <strong></strong> <em>IssuerCertFile</em></td>
<td>Local do certificado do emissor.</td>
</tr>
<tr class="even">
<td><strong>-IK</strong> <strong></strong> <em>IssuerKey</em></td>
<td>Local do contêiner de chave do emissor. O padrão é a chave raiz de teste.</td>
</tr>
<tr class="odd">
<td><strong>-iKy</strong> <strong></strong> <em>IssuerKeySpec</em></td>
<td>A especificação de chave do emissor, que deve ser um dos três valores possíveis:<br/>
<ul>
<li><strong>Assinatura</strong> (AT_SIGNATURE especificação de chave)</li>
<li><strong>Troca</strong> (AT_KEYEXCHANGE especificação de chave)</li>
<li>Um inteiro, como <strong>3</strong></li>
</ul>
Para obter mais informações, consulte a observação que segue esta tabela.<br/></td>
</tr>
<tr class="even">
<td><strong>-IP</strong> <strong></strong> <em>IssuerProviderName</em></td>
<td>Provedor de CryptoAPI para emissor. O padrão é o provedor do usuário. Para obter informações sobre provedores de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</td>
</tr>
<tr class="odd">
<td><strong>-IV</strong> <strong></strong> <em>IssuerKeyFile</em></td>
<td>Arquivo de chave privada do emissor. O padrão é a raiz do teste.</td>
</tr>
<tr class="even">
<td><strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em></td>
<td>Tipo de provedor de CryptoAPI para emissor. O padrão é <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Para obter informações sobre tipos de provedor de CryptoAPI, consulte a documentação do CryptoAPI 2.0.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Se a opção de especificação de chave **-iKy** for usada no Internet Explorer 4,0 ou posterior, a especificação deverá corresponder à especificação de chave indicada pelo arquivo de [*chave privada*](../secgloss/p-gly.md) ou pelo [*contêiner de chave*](../secgloss/k-gly.md)privada. Se a opção de especificação de chave não for usada, a especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de chave privada será usada. Se houver mais de uma especificação de chave no contêiner de chave, o MakeCert tentará primeiro usar a \_ especificação de chave de assinatura at. Se isso falhar, o MakeCert tentará usar AT \_ Exchange. Como a maioria dos usuários tem uma \_ chave de assinatura at ou uma \_ chave de troca de chaves, essa opção não precisa ser usada na maioria dos casos.

 

As opções a seguir são apenas para a tecnologia de [*repositório de certificados*](../secgloss/c-gly.md) .



| Opção de repositório de certificados          | Description                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-IC** *IssuerCertFile*          | Arquivo que contém o certificado do emissor. O MakeCert pesquisará no repositório de certificados para um certificado com uma correspondência exata.                                                                                                                                                                                                        |
| **-em** *IssuerNameString*        | Nome comum do certificado do emissor. O MakeCert pesquisará no repositório de certificados para um certificado cujo nome comum inclua *IssuerNameString*.                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Local do registro do repositório de certificados do emissor. *IssuerCertStoreLocation* deve ser **LocalMachine** (chave do registro hKey \_ local \_ Machine) ou **CurrentUser** (chave do registro hKey \_ Current \_ User). **CurrentUser** é o padrão.                                                                                                |
| **-é** *IssuerCertStoreName*     | Repositório de certificados do emissor que inclui o certificado do emissor e suas informações de chave privada associadas. Se houver mais de um certificado no repositório, o usuário deverá identificá-lo exclusivamente usando a opção **-IC** ou **-in** . Se o certificado no repositório de certificados não for identificado de forma exclusiva, o MakeCert falhará. |



 

 

 
