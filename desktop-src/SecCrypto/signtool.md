---
title: SignTool
description: SignTool é uma ferramenta de linha de comando que assina digitalmente arquivos, verifica as assinaturas em arquivos e arquivos de data/hora.
ms.assetid: aa59cb35-5fba-4ce8-97ea-fc767c83f88e
ms.topic: article
ms.date: 10/12/2020
ms.openlocfilehash: f7105e81b958e463612a5065003ed04c24b913f87f52d8d72bb7a708917ebbed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897951"
---
# <a name="signtool"></a>SignTool

SignTool é uma ferramenta de linha de comando que assina digitalmente arquivos, verifica as assinaturas em arquivos e arquivos de data/hora. Para obter informações sobre por que assinar arquivos é importante, consulte [Introdução à assinatura de código.](cryptography-tools.md) A ferramenta é instalada na pasta Bin do caminho de instalação do \\ SDK (Software Development Kit) do Microsoft Windows (exemplo: C:\Arquivos de Programas (x86)\Windows Kits\10\bin\10.0.19041.0\x64\signtool.exe).

O SignTool está disponível como parte do SDK Windows, que você pode baixar do <https://developer.microsoft.com/windows/downloads/windows-10-sdk/> .

> [!Note]  
> O SDK do Windows 10, Windows 10 HLK, Windows 10 WDK e Windows 10 ADK **builds 20236** e superiores agora exigirão a especificação do algoritmo digest. O comando signTool requer que as opções /fd e /td sejam especificadas durante a assinatura e o `file digest algorithm` `timestamp digest algorithm` data/hora, respectivamente. Um aviso (código de erro 0, inicialmente) será lançado se /fd não for especificado durante a assinatura e se /td não for especificado durante o data/hora. Em versões posteriores do SignTool, o aviso se tornará um erro. O SHA256 é recomendado e considerado mais seguro do que SHA1 pelo setor.  


## <a name="syntax"></a>Sintaxe  
  
```console  
signtool [command] [options] [file_name | ...]  
```  

## <a name="parameters"></a>parâmetros  
  
|Argumento|Descrição|  
|----|----|  
|`command`|Um dos quatro comandos (`catdb`, `sign`, `Timestamp` ou `Verify`) que especifica uma operação a ser realizada em um arquivo. Para obter uma descrição de cada comando, consulte a próxima tabela.|  
|`options`|Uma opção que modifica um comando. Além das opções globais `/q` e `/v`, cada comando dá suporte a um conjunto exclusivo de opções.|  
|`file_name`|O caminho para um arquivo a ser assinado.| 


Os comandos a seguir são suportados pelo SignTool.

|Comando|Descrição|  
|----|----|  
|`Catdb`|Adiciona ou remove um arquivo de catálogo de um banco de dados do catálogo. Os bancos de dados do catálogo são usados na pesquisa automática de arquivos de catálogo e são identificados por uma GUID. Para obter uma lista de opções com suporte pelo comando `catdb`, consulte [Opções do Comando catdb](/dotnet/framework/tools/signtool-exe#catdb-command-options).|  
|`Sign`|Assina arquivos digitalmente. As assinaturas digitais protegem os arquivos contra violação e permitem aos usuários verificar o signatário com base em um certificado de assinatura. Para obter uma lista de opções com suporte pelo comando `sign`, consulte [Opções do Comando sign](/dotnet/framework/tools/signtool-exe#sign-command-options).|  
|`Timestamp`|Arquivos de carimbo de data/hora. Para obter uma lista das opções com suporte pelo comando `TimeStamp`, consulte [Opções de Comando TimeStamp](/dotnet/framework/tools/signtool-exe#timestamp-command-options).|  
|`Verify`|Verifica a assinatura digital dos arquivos determinando se o certificado de assinatura foi emitido por uma autoridade confiável, se o certificado de assinatura foi revogado e, como opção, se o certificado de assinatura é válido para uma política específica. Para obter uma lista das opções com suporte pelo comando `Verify`, consulte [Opções do Comando Verify](/dotnet/framework/tools/signtool-exe#verify-command-options).|

 As seguintes opções aplicam-se a todos os comandos da Ferramenta de Assinatura.  
  
|Opção global|Descrição|  
|----|----|  
|**/q**|Não exibirá nenhuma saída se o comando for executado com êxito e exibirá saída mínima se o comando falhar.|  
|**/v**|Exibe saída detalhada, independentemente de o comando ser executado com êxito ou falhar, além de exibir mensagens de aviso.|  
|**/debug**|Exibe informações de depuração.|  

 
## <a name="catdb-command-options"></a>Opções de comando catdb  

 A tabela a seguir lista as opções que podem ser usadas com o comando `Catdb`.

| Opção Catdb | Descrição |
|----|----| 
| **/d** | Especifica que o banco de dados de catálogo padrão seja atualizado. Se a opção **/d** nem **/g** não for usada, o SignTool atualizará o componente do sistema e o banco de dados do driver. |
| **/g** *GUID* | Especifica que o banco de dados de catálogo identificado pelo GUID seja atualizado.|
| **/r** | Remove o catálogo especificado do banco de dados de catálogo. Se essa opção não for especificada, o SignTool adicionará o catálogo especificado ao banco de dados do catálogo.|
| **/u** | Especifica que um nome exclusivo seja gerado automaticamente para os arquivos de catálogo adicionados. Se necessário, os arquivos do catálogo são renomeados para evitar conflitos de nome com os arquivos de catálogo existentes. Se essa opção não for especificada, o SignTool substituirá qualquer catálogo existente que tenha o mesmo nome que o catálogo que está sendo adicionado.|

> [!Note]  
> Os bancos de dados de catálogo são usados para a busca automática de arquivos de catálogo.


## <a name="sign-command-options"></a>Opções do comando de entrada  

 A tabela a seguir lista as opções que podem ser usadas com o comando `sign`.  
  
|Opções do comando de entrada|Descrição|  
|----|----| 
|`/a`|Seleciona automaticamente o melhor certificado de assinatura. A Ferramenta de Assinatura encontrará todos os certificados válidos que atendem às condições especificadas e selecionará aquele válido durante um tempo mais longo. Se essa opção não estiver presente, a Ferramenta de Assinatura deverá localizar apenas um certificado de assinatura válido.|  
|`/ac`  *Arquivo*|Adiciona um certificado adicional de *file* ao bloco de assinatura.|  
|`/as`|Acrescenta esta assinatura. Se nenhuma assinatura primária estiver presente, essa assinatura será definida como a assinatura principal.|  
|`/c`  *CertTemplateName*|Especifica o Nome do Modelo de Certificado (uma extensão da Microsoft) para o certificado de assinatura.|  
|`/csp`  *CSPName*|Especifica o provedor de serviços de criptografia (CSP) que contém o contêiner de chave privada.|  
|`/d`  *Desc*|Especifica uma descrição do conteúdo assinado.|  
|`/dg`  *Caminho*|Gera o resumo a ser assinado e os arquivos PKCS7 não assinados. O resumo de saída e os arquivos PKCS7 serão: *Path\FileName.dig* e *Path\FileName.p7u.* Para saída de um arquivo XML adicional, <strong>consulte /dxml</strong>.|  
|`/di`  *Caminho*|Cria a assinatura ingerindo o resumo assinado para o arquivo PKCS7 não assinado. O resumo assinado de entrada e os arquivos PKCS7 não assinados devem ser: *Path\FileName.dig.signed* *e Path\FileName.p7u*.|  
|`/dlib`  *DLL*|Especifica a DLL que implementa a <code>AuthenticodeDigestSign</code> função com a que assinar o resumo. Essa opção é equivalente a usar <strong>SignTool</strong> separadamente com as opções <strong>/dg</strong>, <strong>/ds</strong>e <strong>/di,</strong> exceto que essa opção invoca todos os três como uma operação atômica.|  
|`/dmdf`  *Nome de arquivo*|Quando usado com a <strong>opção /dg,</strong> passa o conteúdo do arquivo para a <code>AuthenticodeDigestSign</code> função sem modificação.|  
|`/ds`  |Assina apenas o resumo. O arquivo de entrada deve ser o resumo gerado pela <strong>opção /dg.</strong> O arquivo de saída será: *File.signed.*|  
|`/du`  *URL*|Especifica uma URL (Uniform Resource Locator) para obter a descrição expandida do conteúdo assinado.|  
|`/dxml`  |Quando usado com a <strong>opção /dg,</strong> produz um arquivo XML. O arquivo de saída será: *Path\FileName.dig.xml*.|  
|`/f`  *SignCertFile*|Especifica o certificado de assinatura em um arquivo. Se o arquivo estiver no formato PFX (Personal Information Exchange) e protegido por senha, use a opção `/p` para especificar a senha. Se o arquivo não contiver chaves privadas, use as opções `/csp` e `/kc` para especificar o CSP e o nome do contêiner de chave privada.|  
|`/fd`*alg*|Especifica o algoritmo de resumo do arquivo a ser usado na criação de assinaturas de arquivo. </br> **Observação:** Um aviso será gerado se <strong>a opção /fd</strong> não for fornecida durante a assinatura. A alg padrão é SHA1, mas SHA256 é recomendado.|
|`/fd`  *certHash*|Especificar a cadeia de caracteres certHash será padrão para o algoritmo usado no certificado de assinatura. </br> **Observação:** Disponível somente no Windows 10 kit de builds 20236 e superior.|  
|`/i`  *IssuerName*|Especifica o nome do emissor de certificado de assinatura. Esse valor pode ser uma subcadeia de caracteres do nome do emissor inteiro.|  
|`/kc`  *PrivKeyContainerName*|Especifica o nome do contêiner de chave privada.|  
|`/n`  *SubjectName*|Especifica o nome do assunto do certificado de assinatura. Esse valor pode ser uma subcadeia de caracteres do nome da entidade inteiro.|  
|`/nph`|Se compatível, suprime hashes de página para arquivos executáveis. O padrão é determinado pela variável de ambiente SIGNTOOL_PAGE_HASHES e pela versão de wintrust.dll. Essa opção é ignorada para arquivos não PE.|  
|`/p`  *Senha*|Especifica a senha a ser usada durante a abertura de um arquivo PFX. (Use a opção `/f` para especificar um arquivo PFX).|  
|`/p7` *Caminho*|Especifica se um arquivo PKCS (Public Key Cryptography Standards) #7 é produzido para cada arquivo de conteúdo especificado. Os arquivos #7 PKCS são nomeados \\ *nome de arquivo de caminho*.p7.|  
|`/p7ce` *Valor*|Especifica opções para o conteúdo de PKCS #7 assinado. Defina *Value* como “Embedded” para inserir o conteúdo assinado no arquivo PKCS #7 ou como “DetachedSignedData” para produzir a parte de dados assinada de um arquivo PKCS #7 desanexado. Se a opção `/p7ce` não for usada, o conteúdo assinado será inserido por padrão.|  
|`/p7co` *\<OID>*|Especifica o OID (identificador de objeto) que identifica o conteúdo assinado de PKCS #7.|  
|`/ph`|Se compatível, gera hashes de página para arquivos executáveis.|  
|`/r`  *RootSubjectName*|Especifica o nome do assunto do certificado raiz em que o certificado de assinatura deve ser encadeado. Esse valor pode ser uma subcadeia de caracteres do nome de entidade inteiro do certificado raiz.|  
|`/s`  *Storename*|Especifica o armazenamento a ser aberto durante a pesquisa pelo certificado. Se essa opção não for especificada, o armazenamento `My` será aberto.|  
|`/sha1`  *Hash*|Especifica o hash SHA1 do certificado de assinatura. O hash SHA1 costuma ser especificado quando vários certificados atendem aos critérios especificados pelas opções restantes.|  
|`/sm`|Especifica se um armazenamento do computador, em vez de um armazenamento de usuário, é usado.|  
|`/t`  *URL*|Especifica a URL do servidor de carimbo de data/hora. Se essa opção (ou `/tr`) não estiver presente, o arquivo assinado não receberá carimbo de data/hora. Um aviso será gerado se o carimbo de data/hora falhar. Essa opção não pode ser usada com a opção `/tr`.|  
|`/td`  *Alg*|Usado com a opção `/tr` para solicitar um algoritmo de resumo usado pelo servidor do carimbo de data/hora RFC 3161. </br> **Observação:** Um aviso será gerado se <strong>a opção /td</strong> não for fornecida durante o data/hora. A alg padrão é SHA1, mas SHA256 é recomendado. <br/> A <strong>opção /td</strong> deve ser declarada após a opção <strong>/tr,</strong> não antes. Se a <strong>opção /td</strong> for declarada antes da opção <strong>/tr,</strong> o timestamp retornado será de um algoritmo SHA1 em vez do algoritmo SHA256 pretendido. |
|`/tr`  *URL*|Especifica a URL do servidor do carimbo de data/hora RFC 3161. Se essa opção (ou `/t`) não estiver presente, o arquivo assinado não receberá carimbo de data/hora. Um aviso será gerado se o carimbo de data/hora falhar. Essa opção não pode ser usada com a opção `/t`.|  
|`/u`  *Uso*|Especifica o EKU (uso avançado de chave) que deve estar presente no certificado de assinatura. O valor de uso pode ser especificado por OID ou por cadeia de caracteres. O uso padrão é "Assinatura de Código" (1.3.6.1.5.5.7.3.3).|  
|`/uw`|Especifica o uso da "Verificação do Componente do Sistema Windows" (1.3.6.1.4.1.311.10.3.6).|  
  
 Para obter exemplos de uso, consulte [Using SignTool to Sign a File](using-signtool-to-sign-a-file.md) (Usando a SignTool para assinar um arquivo).  
  

## <a name="timestamp-command-options"></a>Opções de comando TimeStamp  

 A tabela a seguir lista as opções que podem ser usadas com o comando `TimeStamp`.  
  
|Opção do carimbo de data/hora|Descrição|  
|----|----|  
|`/p7`|Arquivos PKCS #7 do carimbo de data/hora.|  
|`/t`  *URL*|Especifica a URL do servidor de carimbo de data/hora. O arquivo com carimbo de data/hora assinado anteriormente. A opção `/t` ou `/tr` é obrigatória.|  
|`/td`  *Alg*|Usado com a opção `/tr` para solicitar um algoritmo de resumo usado pelo servidor do carimbo de data/hora RFC 3161. </br> **Observação:** Um aviso será gerado se <strong>a opção /td</strong> não for fornecida durante o data/hora. A alg padrão é SHA1, mas SHA256 é recomendado. <br/> A <strong>opção /td</strong> deve ser declarada após a opção <strong>/tr,</strong> não antes. Se a <strong>opção /td</strong> for declarada antes da opção <strong>/tr,</strong> o timestamp retornado será de um algoritmo SHA1 em vez do algoritmo SHA256 pretendido. |
|`/tp`*índice*|Marca com o carimbo de data/hora a assinatura em *index*.|  
|`/tr`  *URL*|Especifica a URL do servidor do carimbo de data/hora RFC 3161. O arquivo com carimbo de data/hora assinado anteriormente. A opção `/tr` ou `/t` é obrigatória.|  


## <a name="verify-command-options"></a>Verificar opções de comando  

|Opção Verificar|Descrição|
|----|----|
| **/a** | Especifica que todos os métodos podem ser usados na verificação do arquivo. Primeiro, os bancos de dados do catálogo são pesquisados para determinar se o arquivo está assinado em um catálogo. Se o arquivo não estiver assinado em nenhum catálogo, o SignTool tentará verificar a assinatura inserida do arquivo. Essa opção é recomendada durante a verificação de arquivos que podem estar ou não assinados em um catálogo. Exemplos de arquivos que podem ou não ser assinados incluem arquivos Windows ou drivers. |
| **/ad** | Encontra o catálogo usando o banco de dados do catálogo padrão. |
| **/all** | Verifica todas as assinaturas em um arquivo com várias assinaturas. |
| **/as** | Encontra o catálogo usando o banco de dados do catálogo do componente de sistema (driver). |
| **/ag** *CatDBGUID* | Localiza o catálogo no banco de dados de catálogo identificado pelo **GUID**. |
| **/c** *CatFile* | Especifica o arquivo de catálogo por nome. |
| **/d** | Imprima a URL de descrição e descrição.<br/> **Windows Vista e anteriores:** Não há suporte para esse sinalizador.<br/> |
| **Índice /ds**  | Verifica a assinatura em uma determinada posição. |
| **/hash**{**SHA1** \| **SHA256**} | Especifica um algoritmo de hash opcional a ser usado durante a procura de um arquivo em um catálogo. |
| **/kp** | Executa a verificação usando a política de assinatura de driver no modo kernel x64. |
| **/ms** | Usa várias semânticas de verificação. Esse é o comportamento padrão de uma [**chamada WinVerifyTrust.**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) |
| **/o** *Versão* | Verifica o arquivo pela versão do sistema operacional. O parâmetro version é do formato:<br/> *PlatformID***:**_VerMajor._* *_VerMinor_*_._ * _BuildNumber_<br/> O uso da opção */o* é recomendado. Se */o* não for especificado, SignTool poderá retornar resultados inesperados. Por exemplo, se você não incluir a opção */o,* os catálogos do sistema validados corretamente em um sistema operacional mais antigo poderão não ser validados corretamente em um sistema operacional mais recente. |
| **/p7** | Verifique os arquivos PKCS \# 7. Nenhuma política existente é usada para validação do PKCS \# 7. A assinatura é verificada e uma cadeia é compilada para o certificado de assinatura. |
| **/pa** | Especifica que a Política de Verificação de Autenticação Padrão é usada. Se a **opção /pa** não for especificada, a SignTool usará a política Windows verificação de driver. Essa opção não pode ser usada com as **opções catdb.** |
| **/pg** *PolicyGUID* | Especifica uma política de verificação por **GUID.** O **GUID** corresponde à ActionID da política de verificação. Essa opção não pode ser usada com as **opções catdb.** |
| **/ph** | Imprima e verifique os valores de hash da página.<br/> **Windows Vista e anteriores:** Não há suporte para esse sinalizador.<br/>  |
| **/r** *RootSubjectName* | Especifica o nome do assunto do certificado raiz em que o certificado de assinatura deve ser encadeado. Esse valor pode ser uma subcadeia de caracteres do nome da entidade inteiro do certificado raiz. |
| **/tw** | Especifica que um aviso será gerado se a assinatura não tiver carimbo de data/hora.|


O comando signTool **verify** determina se o certificado de assinatura foi emitido por uma autoridade confiável, se o certificado de assinatura foi revogado e, opcionalmente, se o certificado de assinatura é válido para uma política específica.  

O comando SignTool **verify** vai dar o status de assinatura inserido, a menos que uma opção seja especificada para pesquisar um catálogo (/a, /ad, /as, /ag, /c). 


## <a name="return-value"></a>Valor retornado  

 A Ferramenta de Assinatura retorna um dos códigos de saída a seguir quando é encerrada.  
  
|Código de saída|Descrição|  
|----|----| 
|0|A execução foi bem-sucedida.|  
|1|A execução falhou.|  
|2|A execução foi concluída com avisos.|


## <a name="examples"></a>Exemplos  

 O comando a seguir adiciona o arquivo de catálogo MyCatalogFileName.cat aos bancos de dados do componente e de driver do sistema. A opção `/u` gera um nome exclusivo, se necessário, para evitar a substituição de um arquivo de catálogo existente chamado `MyCatalogFileName.cat`.  
  
```console  
signtool catdb /v /u MyCatalogFileName.cat  
```  
  
 O comando a seguir assina um arquivo automaticamente usando-se o melhor certificado.  
  
```console  
signtool sign /a /fd SHA256 MyFile.exe 
```  
  
 O comando a seguir assina digitalmente um arquivo usando um certificado armazenado em um arquivo PFX protegido por senha.  
  
```console  
signtool sign /f MyCert.pfx /p MyPassword /fd SHA256 MyFile.exe 
```  
  
 O comando a seguir assina digitalmente e coloca carimbos de data/hora em um arquivo. O certificado usado para assinar o arquivo é armazenado em um arquivo PFX.  
  
```console  
signtool sign /f MyCert.pfx /t http://timestamp.digicert.com /fd SHA256 MyFile.exe 
```  
  
 O comando a seguir assina um arquivo usando um certificado localizado no armazenamento `My` que tem um nome de entidade de `My Company Certificate`.  
  
```console  
signtool sign /n "My Company Certificate" /fd SHA256 MyFile.exe 
```  
  
 O comando a seguir assina um controle ActiveX e fornece informações exibidas pelo Internet Explorer quando o usuário deve instalar o controle.  
  
```console  
Signtool sign /f MyCert.pfx /d: "MyControl" /du http://www.example.com/MyControl/info.html /fd SHA256 MyControl.exe 
```  
  
 O comando a seguir marca um arquivo com carimbos de data/hora já assinado digitalmente.  
  
```console  
signtool timestamp /t http://timestamp.digicert.com MyFile.exe
```  

O comando a seguir marca o carimbo de data/hora de um arquivo usando um servidor de carimbo de data/hora RFC 3161.  
  
```console  
signtool timestamp /tr http://timestamp.digicert.com /td SHA256 MyFile.exe
```  
  
 O comando a seguir verifica se um arquivo foi assinado.  
  
```console  
signtool verify MyFile.exe  
```  
  
 O comando a seguir verifica um arquivo de sistema que pode ser assinado em um catálogo.  
  
```console  
signtool verify /a SystemFile.dll  
```  
  
 O comando a seguir verifica um arquivo de sistema assinado em um catálogo chamado `MyCatalog.cat`.  
  
```console  
signtool verify /c MyCatalog.cat SystemFile.dll  
```  
