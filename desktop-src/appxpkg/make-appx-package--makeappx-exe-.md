---
title: Empacotador de aplicativo (MakeAppx.exe)
description: O app Packager (MakeAppx.exe) cria um pacote de aplicativo de arquivos em disco ou extrai os arquivos de um pacote de aplicativo para o disco.
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084457"
---
# <a name="app-packager-makeappxexe"></a>Empacotador de aplicativo (MakeAppx.exe)

> [!Note]  
> Para obter diretrizes de UWP sobre como usar essa ferramenta, consulte [criar um pacote de aplicativo com a ferramenta de MakeAppx.exe](/windows/msix/package/create-app-package-with-makeappx-tool).

 

O app Packager (MakeAppx.exe) cria um pacote de aplicativo de arquivos em disco ou extrai os arquivos de um pacote de aplicativo para o disco. A partir do Windows 8.1, o app Packager também cria um pacote de aplicativos de pacotes de aplicativos no disco ou extrai os pacotes de aplicativos de um pacote de pacotes de aplicativos para o disco. Ele está incluído no Microsoft Visual Studio e no SDK (Software Development Kit) do Windows para Windows 8 ou Windows Software Development Kit (SDK) para Windows 8.1. Visite [downloads para que os desenvolvedores os]( https://msdn.microsoft.com/windows/apps/br229516.aspx) obtenham.

A ferramenta de MakeAppx.exe normalmente é encontrada nestes locais:

-   Em x86: C: \\ Program Files (x86) \\ windows kits \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C: \\ Program files (x86) \\ Windows kits \\ 8,1 \\ bin \\ x86 \\makeappx.exe
-   Em x64 em dois locais:
    -   C: \\ arquivos de programas (x86) \\ kits do Windows \\ 8,0 \\ bin \\ x86 \\makeappx.exe ou C: \\ arquivos de programas (x86) \\ kits do Windows \\ 8,1 \\ compartimento \\ x86 \\makeappx.exe
    -   C: \\ arquivos de programas (x86) \\ windows kits \\ 8,0 \\ bin \\ x64 \\makeappx.exe ou C: \\ arquivos de programas (x86) kits do \\ Windows \\ 8,1 \\ bin \\ x64 \\makeappx.exe

Não há nenhuma versão ARM da ferramenta.

-   [Para criar um pacote usando uma estrutura de diretório](#to-create-a-package-using-a-directory-structure)
-   [Para criar um pacote usando um arquivo de mapeamento](#to-create-a-package-using-a-mapping-file)
-   [Para assinar o pacote usando SignTool](#to-sign-the-package-using-signtool)
-   [Para extrair arquivos de um pacote](#to-extract-files-from-a-package)
-   [Para criar um pacote de pacotes usando uma estrutura de diretório](#to-create-a-package-bundle-using-a-directory-structure)
-   [Para criar um pacote de pacotes usando um arquivo de mapeamento](#to-create-a-package-bundle-using-a-mapping-file)
-   [Para extrair pacotes de um pacote](#to-extract-packages-from-a-bundle)
-   [Para criptografar um pacote com um arquivo de chave](#to-encrypt-a-package-with-a-key-file)
-   [Para criptografar um pacote com uma chave de teste global](#to-encrypt-a-package-with-a-global-test-key)
-   [Para descriptografar um pacote com um arquivo de chave](#to-decrypt-a-package-with-a-key-file)
-   [Para descriptografar um pacote com uma chave de teste global](#to-decrypt-a-package-with-a-global-test-key)
-   [Usage](#usage)

## <a name="using-app-packager"></a>Usando o app Packager

> [!Note]  
> Caminhos relativos têm suporte em toda a ferramenta.

 

### <a name="to-create-a-package-using-a-directory-structure"></a>Para criar um pacote usando uma estrutura de diretório

Coloque o AppxManifest.xml na raiz de um diretório que contém todos os arquivos de carga para seu aplicativo. Uma estrutura de diretório idêntica é criada para o pacote do aplicativo e estará disponível quando o pacote for extraído no momento da implantação.

1.  Coloque todos os arquivos em uma única estrutura de diretório, criando subdiretórios conforme desejado.

2.  Crie um manifesto de pacote válido, AppxManifest.xml e coloque-o no diretório raiz.

3.  Execute este comando:

    **MakeAppx Pack/d** *entrada \_ DirectoryPath* **/p** _FilePath_**. Appx**

### <a name="to-create-a-package-using-a-mapping-file"></a>Para criar um pacote usando um arquivo de mapeamento

1.  Crie um manifesto de pacote válido, AppxManifest.xml.

2.  Crie um arquivo de mapeamento. A primeira linha contém os **\[ arquivos \]** de cadeia de caracteres e as linhas a seguir especificam os caminhos de origem (disco) e destino (pacote) em cadeias de caracteres entre aspas.

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  Execute este comando:

    **MakeAppx Pack/f** *mapeando \_ FilePath* **/p** _FilePath_**. Appx**

### <a name="to-sign-the-package-using-signtool"></a>Para assinar o pacote usando SignTool

1.  Crie o certificado. O Publicador listado no manifesto deve corresponder às informações do assunto do Publicador do certificado de autenticação. Para obter mais informações sobre como criar um certificado de autenticação, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).

2.  Execute SignTool.exe para assinar o pacote:

    **Signtool sinal/a/v/FD** *hashAlgorithm* **/f** *certFileName* _FilePath_**. Appx**

    O *hashAlgorithm* deve corresponder ao algoritmo de hash usado para criar o blockmap quando o aplicativo foi empacotado. Com o utilitário de empacotamento MakeAppx, o algoritmo de hash Appx blockmap padrão é **SHA256**. Execute SignTool.exe especificando **SHA256** como o algoritmo de síntese de arquivo (/FD):

    **Signtool sinal/a/v/FD SHA256/F** *certFileName* _FilePath_**. Appx**

    Para obter mais informações sobre como assinar pacotes, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md).

### <a name="to-extract-files-from-a-package"></a>Para extrair arquivos de um pacote

1.  Execute este comando:

    **MakeAppx Unpack/p** _File_**. Appx/d** *\_ diretório de saída*

2.  O pacote desempacotado tem a mesma estrutura que o pacote instalado.

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a>Para criar um pacote de pacotes usando uma estrutura de diretório

Usamos o comando **Bundle** para criar um pacote de aplicativo em <output bundle name> Adicionando todos os pacotes de <content directory> (incluindo subpastas). Se <content directory> contiver um manifesto de pacote, AppxBundleManifest.xml, ele será ignorado.

1.  Coloque todos os pacotes em uma única estrutura de diretório, criando subdiretórios conforme desejado.

2.  Execute este comando:

    **MakeAppx Bundle/d** *entrada \_ DirectoryPath* **/p** _FilePath_**. appxbundle**

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a>Para criar um pacote de pacotes usando um arquivo de mapeamento

Usamos o comando **Bundle** para criar um pacote de aplicativo em <output bundle name> Adicionando todos os pacotes de uma lista de pacotes no <mapping file> . Se <mapping file> contiver um manifesto de pacote, AppxBundleManifest.xml, ele será ignorado.

1.  Criará um <mapping file>. A primeira linha contém os **\[ arquivos \]** de cadeia de caracteres e as linhas a seguir especificam os pacotes a serem adicionados ao pacote. Cada pacote é descrito por um par de caminhos entre aspas, separados por espaços ou tabulações. O par de caminhos representa a origem do pacote (no disco) e o destino (em grupo). Todos os nomes de pacote de destino devem ter a extensão. Appx.

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  Execute este comando:

    **Pacote MakeAppx/f** *mapeando \_ FilePath* **/p** _FilePath_**. appxbundle**

### <a name="to-extract-packages-from-a-bundle"></a>Para extrair pacotes de um pacote

1.  Execute este comando:

    **MakeAppx desagrupar/p** _\_ nome do pacote_**. appxbundle/d** *\_ diretório de saída*

2.  O pacote desempacotado tem a mesma estrutura que o pacote de pacotes instalado.

### <a name="to-encrypt-a-package-with-a-key-file"></a>Para criptografar um pacote com um arquivo de chave

1.  Crie um arquivo de chave. Os arquivos de chave devem começar com uma linha que contém a cadeia de caracteres " \[ Keys \] " seguida por linhas que descrevem as chaves com as quais criptografar o pacote. Cada chave é descrita por um par de cadeias de caracteres entre aspas, separadas por espaços ou tabulações. A primeira cadeia de caracteres representa a ID da chave e a segunda cadeia de caracteres representa a chave de criptografia em formato hexadecimal.

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  Execute este comando:

    **MakeAppx.exe criptografar/p** _\_ nome do pacote_**. Appx/EP** _Encrypted \_ Package \_ Name_**. eappx/KF** _keyfile \_ Name_**. txt**

3.  O pacote de entrada será criptografado no pacote criptografado especificado usando o arquivo de chave fornecido.

### <a name="to-encrypt-a-package-with-a-global-test-key"></a>Para criptografar um pacote com uma chave de teste global

1.  Execute este comando:

    **MakeAppx.exe criptografar/p** _\_ nome do pacote_**. Appx/EP** _\_ \_ nome do pacote criptografado_**. eappx/KT**

2.  O pacote de entrada será criptografado no pacote criptografado especificado usando a chave de teste global.

### <a name="to-decrypt-a-package-with-a-key-file"></a>Para descriptografar um pacote com um arquivo de chave

1.  Crie um arquivo de chave. Os arquivos de chave devem começar com uma linha que contém a cadeia de caracteres " \[ Keys \] " seguida por linhas que descrevem as chaves com as quais criptografar o pacote. Cada chave é descrita por um par de cadeias de caracteres entre aspas, separadas por espaços ou tabulações. A primeira cadeia de caracteres representa a ID de chave de 32 bytes codificada em Base64 e a segunda cadeia de caracteres representa a chave de criptografia de 32 bytes codificada em base64.

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  Execute este comando:

    **MakeAppx.exe descriptografar/p** _\_ nome do pacote_**. Appx/EP** _\_ \_ nome do pacote não criptografado_**. eappx/KF** _\_ nome do keyfile_**. txt**

3.  O pacote de entrada será descriptografado no pacote não criptografado especificado usando o arquivo de chave fornecido.

### <a name="to-decrypt-a-package-with-a-global-test-key"></a>Para descriptografar um pacote com uma chave de teste global

1.  Execute este comando:

    **MakeAppx.exe descriptografar/p** _\_ nome do pacote_**. Appx/EP** _\_ \_ nome do pacote não criptografado_**. eappx/KT**

2.  O pacote de entrada será descriptografado no pacote não criptografado especificado usando a chave de teste global.

## <a name="usage"></a>Uso

O argumento de linha de comando **/p** é sempre necessário, com **/d**, **/f** ou **/EP**. Observe que **/d**, **/f** e **/EP** são mutuamente exclusivos.

**\[ Opções \] do MakeAppx Pack** **/p** *\<output package name\>* **/d***\<content directory\>*

**\[ Opções \] do MakeAppx Pack** **/p** *\<output package name\>* **/f***\<mapping file\>*

**MakeAppx \[ opções \] de desempacotamento** **/p** *\<input package name\>* **/d***\<output directory\>*

**\[ Opções \] de pacote MakeAppx** **/p** *\<output bundle name\>* **/d***\<content directory\>*

**\[ Opções \] de pacote MakeAppx** **/p** *\<output bundle name\>* **/f***\<mapping file\>*

**MakeAppx \[ opções \] de desempacotamento** **/p** *\<input bundle name\>* **/d***\<output directory\>*

**MakeAppx \[ opções \] de criptografia** **/p** *\<input package name\>* **/EP***\<output package name\>*

**MakeAppx descriptografar \[ opções \]** **/p** *\<input package name\>* **/EP***\<output package name\>*

## <a name="command-line-syntax"></a>Sintaxe da linha de comando

Aqui está a sintaxe de uso comum de linha de comando para MakeAppx.

Pacote Unpack MakeAppx Pack do pacote desempacotar **\[ \| \| \| \| criptografar/ \| descriptografar \]** \[ **/h** **/KF** **/KT** **/l** **/o**  / **/NV** **/v** **/PFN** **/?**\]

**MakeAppx** packs ou descompactam os arquivos em um pacote, agrupa ou desagrupa os pacotes em um pacote, ou criptografa ou descriptografa o pacote do aplicativo ou o grupo no diretório de entrada ou no arquivo de mapeamento especificado. Aqui está a lista de parâmetros que se aplicam ao **MakeAppx Pack**, **MakeAppx Unpack**, **MakeAppx Bundle**, **MakeAppx desagrupar**, **MakeAppx Encrypt** ou **MakeAppx Decrypt**.

<dl> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Essa opção é usada para pacotes localizados. A validação padrão é bloqueada em pacotes localizados. Essa opção desabilita apenas essa validação específica, sem a necessidade de que todas as validações sejam desabilitadas.

</dd> <dt>

<span id="_o"></span><span id="_O"></span>**/o**
</dt> <dd>

Substituir o arquivo de saída se ele existir. Se você não especificar essa opção ou a opção **/** não, o usuário será perguntado se deseja substituir o arquivo.

Você não pode usar essa opção com **/**.

</dd> <dt>

<span id="_no"></span><span id="_NO"></span>**/**
</dt> <dd>

Impede uma substituição do arquivo de saída, se houver. Se você não especificar essa opção ou a opção **/o** , o usuário será perguntado se deseja substituir o arquivo.

Você não pode usar essa opção com **/o**.

</dd> <dt>

<span id="_nv"></span><span id="_NV"></span>**/nv**
</dt> <dd>

Ignore a validação semântica. Se você não especificar essa opção, a ferramenta executará uma validação completa do pacote.

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

Habilite a saída de log detalhado para o console.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Exibir texto de ajuda.

</dd> </dl>

**MakeAppx Pack** , **MakeAppx Unpack** , **pacote de MakeAppx**, **MakeAppx desagrupar**, **MakeAppx Encrypt** e **MakeAppx Decrypt** são comandos mutuamente exclusivos. Estes são os parâmetros de linha de comando que se aplicam especificamente a cada comando:

**Pacote MakeAppx** \[ **h**\]

Cria um pacote.

<dl> <dt>

<span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span> *algoritmo* /h
</dt> <dd>

Especifica o algoritmo de hash a ser usado ao criar o mapa de blocos. Aqui estão os valores válidos para o *algoritmo*:

<dl> <dd>SHA256 (padrão)</dd> <dd>SHA384</dd> <dd>SHA512</dd> </dl>

Você não pode usar essa opção com o comando **Unpack** .

</dd> </dl>

**Descompactar MakeAppx** \[ **PFN**\]

Extrai todos os arquivos do pacote especificado para o diretório de saída especificado. A saída tem a mesma estrutura de diretório que o pacote.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Especifica um diretório chamado com o nome completo do pacote. Esse diretório é criado no local de saída fornecido. Você não pode usar essa opção com o comando **Pack** .

</dd> </dl>

**Desagrupar MakeAppx** \[ **PFN**\]

Desempacota todos os pacotes em um subdiretório no caminho de saída especificado, nomeados após o nome completo do pacote. A saída tem a mesma estrutura de diretório que o pacote de pacotes instalado.

<dl> <dt>

<span id="_pfn"></span><span id="_PFN"></span>**/pfn**
</dt> <dd>

Especifica um diretório chamado com o nome completo do pacote de pacotes. Esse diretório é criado no local de saída fornecido. Você não pode usar essa opção com o comando **Bundle** .

</dd> </dl>

**MakeAppx criptografar** \[ **KF**, **KT**\]

Cria um pacote de aplicativo criptografado do pacote do aplicativo de entrada especificado no pacote de saída especificado.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Criptografa o pacote ou grupo usando a chave do arquivo de chave especificado. Você não pode usar essa opção com **KT**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Criptografa o pacote ou grupo usando a chave de teste global. Você não pode usar essa opção com **KF**.

</dd> </dl>

**Descriptografar MakeAppx** \[ **KF**, **KT**\]

Cria um pacote de aplicativo não criptografado do pacote do aplicativo de entrada especificado no pacote de saída especificado.

<dl> <dt>

<span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/KF***<key file>*
</dt> <dd>

Descriptografa o pacote ou grupo usando a chave do arquivo de chave especificado. Você não pode usar essa opção com **KT**.

</dd> <dt>

<span id="_kt"></span><span id="_KT"></span>**/kt**
</dt> <dd>

Descriptografa o pacote ou grupo usando a chave de teste global. Você não pode usar essa opção com **KF**.

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a>Validação semântica executada pelo MakeAppx

O MakeAppx executa uma validação semântica limitada que é projetada para detectar os erros de implantação mais comuns e ajudar a garantir que o pacote do aplicativo seja válido.

Essa validação garante que:

-   Todos os arquivos referenciados no manifesto do pacote sejam incluídos no pacote de aplicativo.
-   Um app não tenha duas chaves idênticas.
-   Um aplicativo não se registra para um protocolo proibido desta lista: SMB, arquivo, MS-WWA-WEB, MS-WWA.

Essa validação semântica não está completa e não há garantia de que os pacotes criados pelo MakeAppx sejam instaláveis.

 

 