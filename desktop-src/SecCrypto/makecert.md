---
description: Cria um certificado X. 509, assinado pela chave raiz de teste ou outra chave especificada, que associa seu nome à parte pública do par de chaves. O certificado é salvo em um arquivo, um repositório de certificados do sistema ou ambos.
ms.assetid: a28e77dd-72c9-42a3-a72d-1b3eaf59d9cf
title: MakeCert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff9fb79b5db5a6a71eee981166742b4e1680184
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471922"
---
# <a name="makecert"></a>MakeCert

> [!Note]  
> O MakeCert foi preterido. Para criar certificados autoassinados, use o cmdlet do PowerShell [New-SelfSignedCertificate](/powershell/module/pki/new-selfsignedcertificate).

 

A ferramenta MakeCert cria um certificado [*X. 509*](../secgloss/x-gly.md) , assinado pela chave raiz de teste ou outra chave especificada, que associa seu nome à parte pública do par de chaves. O certificado é salvo em um arquivo, um repositório de certificados do sistema ou ambos. a ferramenta é instalada na \\ pasta Bin do caminho de instalação do Software Development Kit (SDK) do Microsoft Windows.

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




| Opção básica | Descrição | 
|--------------|-------------|
| <strong>-a</strong> <strong></strong> <em>Algoritmo</em> do | Algoritmo de <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> . Deve ser definido como <strong>SHA-1</strong> ou <strong>MD5</strong> (padrão). Para obter informações sobre MD5, consulte <a href="/windows/desktop/SecGloss/m-gly"><em>MD5</em></a>. | 
| <strong>-b</strong> <strong></strong> <em>DateStart</em> | Data em que o certificado se torna válido pela primeira vez. O padrão é quando o certificado é criado. O formato de <em>DateStart</em> é mm/dd/aaaa. | 
| <strong>-CY</strong> <strong></strong> <em>CertificateTypes</em> | Tipo de certificado. <em>CertificateTypes</em> pode ser <strong>end</strong> para a entidade end ou <strong>autoridade</strong> para <a href="/windows/desktop/SecGloss/c-gly"><em>autoridade de certificação</em></a>. | 
| <strong>-e</strong> <strong></strong> <em>DateEnd</em> | Data em que o período de validade termina. O padrão é o ano 2039. | 
| <strong>-EKU</strong> <strong></strong> <em>OID1</em><strong>,</strong><em>OID2</em> ... | Insere uma lista de um ou mais OIDs (<a href="/windows/desktop/SecGloss/o-gly"><em>identificadores de objeto</em></a> ) de <a href="/windows/desktop/SecGloss/e-gly"><em>uso avançado de chave</em></a>separados por vírgula no certificado. Por exemplo, <strong>-EKU 1.3.6.1.5.5.7.3.2</strong> insere o OID de autenticação de cliente. Para obter definições de OIDs permitidos, consulte o arquivo Wincrypt. h em CryptoAPI 2.0. | 
| <strong>-h</strong> <strong></strong> <em>NumChildren</em> | Altura máxima da árvore abaixo deste certificado. | 
| <strong>-l</strong> <strong></strong> <em>PolicyLink</em> | Link para informações de política do SPC Agency (por exemplo, uma URL). | 
| <strong>-m</strong> <strong></strong> <em>nMonths</em> | Duração do período de validade. | 
| <strong>-n</strong><strong>"</strong><em>nome</em><strong>"</strong> | Nome do certificado do editor. Esse nome deve estar em conformidade com o padrão <a href="/windows/desktop/SecGloss/x-gly"><em>X. 500</em></a> . O método mais simples é usar o formato "CN =<em>myname</em>". Por exemplo: <strong>-n "CN = test"</strong>. | 
| <strong>-nscp</strong> | A extensão de autenticação de cliente do Netscape deve ser incluída. | 
| <strong>-PE</strong> | Marca a chave privada como exportável. | 
| <strong>-r</strong> | Cria um certificado autoassinado. | 
| <strong>-SC</strong> <strong></strong> <em>SubjectCertFile</em> | Nome do arquivo de certificado com a chave pública de entidade existente a ser usada. | 
| <strong>-SK</strong> <strong></strong> <em>SubjectKey</em> | Local do contêiner de chave da entidade que contém a <a href="/windows/desktop/SecGloss/p-gly"><em>chave privada</em></a>. Se um contêiner de chave não existir, um será criado. Se nem a opção <strong>-SK</strong> ou <strong>-SV</strong> for usada, um contêiner de chave padrão será criado e usado por padrão. | 
| <strong>-céu</strong> <strong></strong> <em>SubjectKeySpec</em> | Especificação da chave da entidade. <em>SubjectKeySpec</em> deve ser um dos três valores possíveis:<br /><ul><li><strong>Assinatura</strong> (AT_SIGNATURE especificação de chave)</li><li><strong>Exchange</strong> (AT_KEYEXCHANGE especificação de chave)</li><li>Um inteiro, como <strong>3</strong></li></ul>Para obter mais informações, consulte a observação que segue esta tabela.<br /> | 
| <strong>-SP</strong> <strong></strong> <em>SubjectProviderName</em> | Provedor de CryptoAPI para o assunto. O padrão é o provedor do usuário. Para obter informações sobre provedores de CryptoAPI, consulte a documentação do CryptoAPI 2.0. | 
| <strong>-Sr</strong> <strong></strong> <em>SubjectCertStoreLocation</em> | Local do registro do repositório de certificados da entidade. <em>SubjectCertStoreLocation</em> deve ser <strong>LocalMachine</strong> (chave do registro HKEY_LOCAL_MACHINE) ou <strong>CurrentUser</strong> (chave do registro HKEY_CURRENT_USER). <strong>CurrentUser</strong> é o padrão. | 
| <strong>-SS</strong> <strong></strong> <em>SubjectCertStoreName</em> | Nome do repositório de certificados da entidade em que o certificado gerado será armazenado. | 
| <strong>-VA</strong> <strong></strong> <em>SubjectKeyFile</em> | Nome do arquivo. pvk da entidade. Se nem a opção <strong>-SK</strong> ou <strong>-SV</strong> for usada, um contêiner de chave padrão será criado e usado por padrão. | 
| <strong>-Sy</strong> <strong></strong> <em>nSubjectProviderType</em> | Tipo de provedor de CryptoAPI para o assunto. O padrão é <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Para obter informações sobre tipos de provedor de CryptoAPI, consulte a documentação do CryptoAPI 2.0. | 
| <strong>-#</strong><strong></strong><em>SerialNumber</em> | Número de série do certificado. O valor máximo é 2 ^ 31. O padrão é um valor gerado pela ferramenta que tem a garantia de ser exclusivo. | 
| <strong>-$</strong><strong></strong><em>CertificateAuthority</em> | Tipo de <a href="/windows/desktop/SecGloss/c-gly"><em>autoridade de certificação</em></a>. O <em>CertificateAuthority</em> deve ser definido como <strong>comercial</strong> (para certificados a serem usados por editores de software comercial) ou <strong>individual</strong> (para certificados a serem usados por editores de software individuais). | 
| <strong>-?</strong> | Exibe as opções básicas. | 
| <strong>-!</strong> | Exibe as opções estendidas. | 




 

> [!Note]  
> Se a opção de especificação de chave **-céu** for usada no Internet Explorer versão 4,0 ou posterior, a especificação deverá corresponder à especificação de chave indicada pelo arquivo de [*chave privada*](../secgloss/p-gly.md) ou pelo [*contêiner de chave*](../secgloss/k-gly.md)privada. Se a opção de especificação de chave não for usada, a especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de chave privada será usada. Se houver mais de uma especificação de chave no contêiner de chave, MakeCert primeiro tentará usar a especificação da chave AT \_ SIGNATURE. Se isso falhar, o MakeCert tentará usar AT \_ KEYEXCHANGE. Como a maioria dos usuários tem uma chave AT SIGNATURE ou uma \_ chave AT KEYEXCHANGE, essa opção não precisa ser \_ usada na maioria dos casos.

 

As opções a seguir são apenas para arquivos SPC (Certificado Publisher [*software)*](../secgloss/s-gly.md) e tecnologia de chave privada.




| Opção SPC e chave privada | Descrição | 
|----------------------------|-------------|
| <strong>-ic</strong> <strong></strong> <em>IssuerCertFile</em> | Local do certificado do emissor. | 
| <strong>-ik</strong> <strong></strong> <em>IssuerKey</em> | Local do contêiner de chave do emissor. O padrão é a chave raiz de teste. | 
| <strong>-iky</strong> <strong></strong> <em>IssuerKeySpec</em> | Especificação de chave do emissor, que deve ser um dos três valores possíveis:<br /><ul><li><strong>Assinatura</strong> (especificação AT_SIGNATURE chave)</li><li><strong>Exchange</strong> (AT_KEYEXCHANGE de chave)</li><li>Um inteiro, como <strong>3</strong></li></ul>Para obter mais informações, consulte a Observação que segue esta tabela.<br /> | 
| <strong>-ip</strong> <strong></strong> <em>IssuerProviderName</em> | Provedor CryptoAPI para emissor. O padrão é o provedor do usuário. Para obter informações sobre provedores cryptoAPI, consulte a documentação CryptoAPI 2.0 criptografia. | 
| <strong>-iv</strong> <strong></strong> <em>IssuerKeyFile</em> | O arquivo de chave privada do emissor. O padrão é a raiz do teste. | 
| <strong>-iy</strong> <strong></strong> <em>nIssuerProviderType</em> | Tipo de provedor CryptoAPI para o emissor. O padrão é <a href="/windows/desktop/SecGloss/p-gly"><em>PROV_RSA_FULL</em></a>. Para obter informações sobre tipos de provedor CryptoAPI, consulte a documentação CryptoAPI 2.0 dados. | 




 

> [!Note]  
> Se a **opção -iky** key specification for usada no Internet Explorer 4.0 ou posterior, a [](../secgloss/p-gly.md) especificação deverá corresponder à especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de [*chave privada*](../secgloss/k-gly.md). Se a opção de especificação de chave não for usada, a especificação de chave indicada pelo arquivo de chave privada ou pelo contêiner de chave privada será usada. Se houver mais de uma especificação de chave no contêiner de chave, MakeCert primeiro tentará usar a especificação da chave AT \_ SIGNATURE. Se isso falhar, o MakeCert tentará usar AT \_ KEYEXCHANGE. Como a maioria dos usuários tem uma chave AT SIGNATURE ou uma \_ chave AT KEYEXCHANGE, essa opção não precisa ser \_ usada na maioria dos casos.

 

As opções a seguir são apenas para [*tecnologia de armazenamento*](../secgloss/c-gly.md) de certificados.



| Opção de armazenamento de certificados          | Descrição                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **-ic** *IssuerCertFile*          | Arquivo que contém o certificado do emissor. MakeCert pesquisa no armazenamento de certificados um certificado com uma combinação exata.                                                                                                                                                                                                        |
| **-in** *IssuerNameString*        | Nome comum do certificado do emissor. MakeCert pesquisa no armazenamento de certificados um certificado cujo nome comum inclui *IssuerNameString*.                                                                                                                                                                                  |
| **-ir** *IssuerCertStoreLocation* | Local do Registro do armazenamento de certificados do emissor. *IssuerCertStoreLocation* deve ser **LocalMachine** (chave do Registro HKEY LOCAL MACHINE) ou \_ \_ **CurrentUser** (chave do Registro HKEY \_ CURRENT \_ USER). **CurrentUser** é o padrão.                                                                                                |
| **-is** *IssuerCertStoreName*     | O armazenamento de certificados do emissor que inclui o certificado do emissor e suas informações de chave privada associadas. Se houver mais de um certificado no armazenamento, o usuário deverá identificá-lo exclusivamente usando a **opção -ic** **ou -in.** Se o certificado no armazenamento de certificados não for identificado exclusivamente, o MakeCert falhará. |



 

 

 
