---
title: Assinatura Authenticode para desenvolvedores de jogos
description: Este artigo discute como começar a autenticar seu jogo e como integrar a autenticação em um processo de compilação diário.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f304e6cc8e185264699709987f62dfdca17bf8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105754684"
---
# <a name="authenticode-signing-for-game-developers"></a>Assinatura Authenticode para desenvolvedores de jogos

A autenticação de dados é cada vez mais importante para desenvolvedores de jogos. O Windows Vista e o Windows 7 têm uma série de recursos, como controles dos pais, que exigem que os jogos sejam assinados corretamente para garantir que nenhum deles tenha adulterado os dados. O Microsoft Authenticode permite que os usuários finais e o sistema operacional verifiquem se o código do programa provém do proprietário e se ele não foi alterado ou acidentalmente corrompido. Este artigo discute como começar a autenticar seu jogo e como integrar a autenticação em um processo de compilação diário.

-   [Tela de fundo](#background)
-   [Introdução](#getting-started)
-   [Usando uma autoridade de certificação confiável](#using-a-trusted-certificate-authority)
-   [Exemplo usando um certificado de teste](#example-using-a-test-certificate)
-   [Integrando a assinatura de código no sistema de compilação diário](#integrating-code-signing-into-the-daily-build-system)
-   [Revogação](#revocation)
-   [Drivers de assinatura de código](#code-signing-drivers)
-   [Resumo](#summary)
-   [Mais informações](#more-information)

> [!Note]  
> A partir de 1º de janeiro de 2016, o Windows 7 e versões posteriores não confiam mais em nenhum certificado de assinatura de código SHA-1 com uma data de expiração de 1º de janeiro de 2016 ou posterior. Consulte [imposição do Windows de assinatura de código Authenticode e carimbo de data/hora](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) para obter mais informações.

 

## <a name="background"></a>Tela de fundo

Os certificados digitais são usados para estabelecer a identidade do autor. Os certificados digitais são emitidos por terceiros confiáveis conhecidos como uma autoridade de certificação (CA), como VeriSign ou Thawte. A autoridade de certificação é responsável por verificar se o proprietário não está reivindicando uma identidade falsa. Depois de aplicar a uma CA para um certificado, os desenvolvedores comerciais podem esperar uma resposta ao seu aplicativo em menos de duas semanas.

Depois que a AC decidir que você atende aos seus critérios de política, ele gera um certificado de assinatura de código que está em conformidade com X. 509, o formato de certificado padrão da indústria criado pela International Telecommunications Union, com extensões da versão 3. Esse certificado identifica você e contém sua chave pública. Ele é armazenado pela autoridade de certificação para referência e uma cópia é fornecida eletronicamente. Ao mesmo tempo, você também cria uma chave privada, que você deve manter segura e que você não deve compartilhar com ninguém, até mesmo a autoridade de certificação.

Depois de ter uma chave pública e privada, você pode começar a distribuir o software assinado. A Microsoft fornece ferramentas para fazer isso na SDK do Windows. As ferramentas utilizam um hash unidirecional, produzem um resumo de comprimento fixo e geram uma assinatura criptografada com uma chave privada. Em seguida, eles combinam essa assinatura criptografada com o certificado e as credenciais em uma estrutura conhecida como um bloco de assinatura e a inserimos no formato de arquivo do executável. Qualquer tipo de arquivo binário executável pode ser assinado, incluindo DLLs, arquivos executáveis e arquivos de gabinete.

A assinatura pode ser verificada de várias maneiras. Os programas podem chamar a função CertVerifyCertificateChainPolicy e SignTool (signtool.exe) podem ser usados para verificar uma assinatura do prompt de linha de comando. O Windows Explorer também tem uma guia assinaturas digitais em Propriedades de arquivo que exibe cada certificado de um arquivo binário assinado. (A guia assinaturas digitais só aparece em Propriedades de arquivo para arquivos assinados.) Além disso, um aplicativo pode ser autoverificado pelo uso de [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

A assinatura Authenticode não é útil apenas para a autenticação de dados pelos usuários finais, mas também é necessária para aplicar patches de contas de usuário limitadas e controles dos pais no Windows Vista e no Windows 7. Além disso, as tecnologias futuras em sistemas operacionais Windows também podem exigir que o código seja assinado, portanto, é altamente recomendável que todos os desenvolvedores profissionais e amadores adquiram um certificado de assinatura de código de uma CA. Mais informações sobre como isso é feito podem ser encontradas posteriormente neste artigo em [usando uma autoridade de certificação confiável](#using-a-trusted-certificate-authority).

O código de jogo, os patches e os instaladores podem aproveitar ainda mais a assinatura do Authenicode verificando se os arquivos são autênticos no código. Isso pode ser usado para a segurança de rede geral e antienganar. Um exemplo de código para verificar se um arquivo está assinado pode ser encontrado aqui: [exemplo C programa: verificando a assinatura de um arquivo PE e um](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)código de exemplo para verificar a propriedade de um certificado de assinatura em um arquivo assinado pode ser encontrado aqui: [como obter informações de executáveis com Authenticode assinados](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Introdução

Para começar, a Microsoft fornece ferramentas com o Visual Studio 2005 e o Visual Studio 2008, e na [SDK do Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx), para ajudar a executar e verificar o processo de assinatura de código. Depois de instalar o Visual Studio ou o SDK do Windows, as ferramentas descritas neste artigo técnico estão localizadas em um subdiretório da instalação, que pode incluir um ou mais dos seguintes:

-   % SystemDrive% \\ arquivos de programas \\ Microsoft Visual Studio o \\ compartimento 8 SDK \\ v 2.0 \\
-   % SystemDrive% \\ arquivos de programas \\ Microsoft Visual Studio \\ compartimento de 8 vc \\ PlatformSDK \\
-   % SystemDrive% \\ arquivos de programas \\ Microsoft Visual Studio 9,0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   % SystemDrive% \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 a \\ bin\\

As seguintes ferramentas são as mais úteis para o código de assinatura:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Ferramenta de criação de certificado (MakeCert.exe)
</dt> <dd>

Gera um certificado X. 509 de teste, como um arquivo. cer, que contém sua chave pública e uma chave privada, como um arquivo. pvk. Esse certificado é apenas para fins de teste interno e não pode ser usado publicamente.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Cria um arquivo de troca de informações pessoais (. pfx) a partir de um par de arquivos. cer e. pvk. O arquivo. pfx contém sua chave pública e privada.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Assina o arquivo usando o arquivo. pfx. O SignTool dá suporte à assinatura de arquivos DLL, arquivos executáveis, arquivos Windows Installer (. msi) e arquivos de gabinete (. cab).

</dd> </dl>

> [!Note]  
> Ao ler outras documentações, você pode encontrar referências ao SignCode (SignCode.exe), mas essa ferramenta foi preterida e não tem mais suporte. em vez disso, use SignTool.

 

## <a name="using-a-trusted-certificate-authority"></a>Usando uma autoridade de certificação confiável

Para obter um certificado confiável, você deve aplicar a uma AC (autoridade de certificação), como VeriSign ou Thawte. A Microsoft não recomenda nenhuma AC sobre outra, mas se você quiser integrar-se ao serviço Relatório de Erros do Windows (WER), considere usar a VeriSign para emitir o certificado, pois o acesso ao banco de dados WER requer uma conta WinQual que exija uma ID da VeriSign. Para obter uma lista completa de autoridades de certificação de terceiros confiáveis, consulte [membros do programa de certificado raiz da Microsoft](/previous-versions/ms995347(v=msdn.10)). Para obter mais informações sobre como registrar com o WER, consulte "[introdução ao relatório de erros do Windows](https://msdn.microsoft.com/)" na [zona do ISV](https://msdn.microsoft.com/).

Depois de receber o certificado da autoridade de certificação, você pode assinar seu programa usando SignTool e liberar seu programa para o público. No entanto, você deve ter cuidado para proteger sua chave privada, que está contida em seus arquivos. pfx e. pvk. Lembre-se de manter esses arquivos em um local seguro.

## <a name="example-using-a-test-certificate"></a>Exemplo usando um certificado de teste

As etapas a seguir demonstram a criação de um certificado de assinatura de código para fins de teste, seguidos pela assinatura de um programa de exemplo de Direct3D (chamado BasicHLSL.exe) com esse certificado de teste. Este procedimento cria arquivos. cer e. pvk — suas chaves pública e privada, respectivamente, que não podem ser usadas para certificação pública.

Neste exemplo, um carimbo de data/hora também é adicionado à assinatura. Um carimbo de data/hora impede que a assinatura se torne inválida quando o certificado expira. O código assinado, mas falta um carimbo de data/hora, não será validado depois que o certificado expirar. Portanto, todo o código lançado publicamente deve ter um carimbo de data/hora.

**Para criar um certificado e assinar um programa**

1.  Crie um certificado de teste e uma chave privada usando a ferramenta de criação de certificado (MakeCert.exe).

    O exemplo de linha de comando a seguir especifica MyPrivateKey como o nome de arquivo para o arquivo de chave privada (. pvk), mypublickey como o nome de arquivo para o arquivo de certificado (. cer) e MySoftwareCompany como o nome do certificado. Ele também torna o certificado autoassinado, para que ele não tenha uma autoridade raiz não confiável.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Crie um arquivo de troca de informações pessoais (. pfx) do arquivo de chave privada (. pvk) e do arquivo de certificado (. cer) usando pvk2pfx.exe.

    O arquivo. pfx combina suas chaves pública e privada em um único arquivo. O exemplo de linha de comando a seguir usa os arquivos. pvk e. cer da etapa anterior para criar o arquivo. pfx chamado MyPFX com a senha sua \_ senha:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Assine seu programa com seu arquivo de troca de informações pessoais (. pfx) usando SignTool.

    Você pode especificar várias opções na linha de comando. O exemplo de linha de comando a seguir usa o arquivo. pfx da etapa anterior, fornece sua \_ senha como a senha, especifica BasicHLSL como o arquivo a ser assinado e recupera um carimbo de data/hora de um servidor especificado:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > A URL para o serviço de carimbo de data/hora é fornecida pela autoridade de certificação e é opcional para teste. É importante que a assinatura de produção inclua uma autoridade de carimbo de data/hora válida, ou a assinatura não será validada quando o certificado expirar.

     

4.  Verifique se o programa está assinado usando SignTool.

    O exemplo de linha de comando a seguir especifica que o SignTool deve tentar verificar a assinatura em BasicHLSL.exe usando todos os métodos disponíveis enquanto fornece a saída detalhada:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    Neste exemplo, SignTool deve indicar que o certificado está anexado, enquanto também está informando que não é confiável, pois não é emitido por uma autoridade de certificação.

5.  Confie no certificado de teste.

    Para certificados de teste, você precisa confiar no certificado. Essa etapa deve ser ignorada para certificados fornecidos por uma CA, uma vez que eles serão confiáveis por padrão.

    Somente nos computadores em que você deseja confiar no certificado de teste, execute o seguinte:

    ```
    certmgr.msc
    ```

    

    Em seguida, clique com o botão direito do mouse em autoridades de certificação raiz confiáveis e escolha todas as tarefas \| importar. Em seguida, navegue até o arquivo. pfx que você criou e siga as etapas do assistente, colocando o certificado nas autoridades de certificação raiz confiáveis.

    Quando o assistente for concluído, você poderá iniciar o teste com o certificado confiável nesse computador.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrando a assinatura de código no sistema de compilação diário

Para integrar o código de assinatura a um projeto do, você pode criar um arquivo em lotes ou script para executar as ferramentas de linha de comando. Depois que o projeto for criado, execute SignTool com as configurações apropriadas (conforme mostrado na etapa 3 do nosso exemplo).

Seja especialmente cauteloso em seu processo de compilação para garantir que o acesso aos arquivos. pfx e. pvk seja restrito ao mínimo de computadores e usuários possível. Como prática recomendada, os desenvolvedores só devem assinar o código usando o certificado de teste até que estejam prontos para serem entregues. Novamente, a chave privada (. pvk) deve ser mantida em um local seguro, como um espaço seguro ou bloqueado, e idealmente em um dispositivo criptográfico, como um cartão inteligente.

Outra camada de proteção é fornecida usando o Microsoft Authenticode para assinar o pacote de Windows Installer (MSI) em si. Isso ajuda a proteger o pacote MSI contra violações e danos acidentais. Consulte a documentação da ferramenta de criação do MSI para obter mais informações sobre como assinar pacotes com Authenticode.

## <a name="revocation"></a>Revogação

Caso a segurança da chave privada seja comprometida ou algum evento relacionado à segurança renderize um Code-Signing certificado inválido, o desenvolvedor deve revogar o certificado. Não fazer isso enfraqueceria a integridade do desenvolvedor e a eficácia do código de assinatura. Uma CA também pode emitir uma revogação com um horário específico; o código assinado com um carimbo de data/hora antes do tempo de revogação ainda será considerado válido, mas o código com um carimbo de data/hora subsequente será inválido. A revogação de certificado afeta o código em todos os aplicativos assinados com o certificado revogado.

## <a name="code-signing-drivers"></a>Drivers de Code-Signing

Os drivers podem e devem ser assinados por Authenticode. Os drivers do modo kernel têm requisitos adicionais: as edições de 64 bits do Windows Vista e do Windows 7 impedirão a instalação de todos os drivers do modo kernel não assinados, e todas as versões do Windows apresentarão um prompt de aviso quando um usuário tentar instalar um driver não assinado. Além disso, os administradores podem definir Política de Grupo para impedir que drivers não assinados sejam instalados no Microsoft Windows Server 2003, no Windows XP Professional x64 Edition e nas edições de 32 bits do Windows Vista e do Windows 7.

Muitos tipos de drivers podem ser assinados com uma assinatura confiável da Microsoft — como parte do programa de certificação do Windows do WHQL ( [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) ) ou do [programa de assinatura não classificada](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (anteriormente denominado assinatura de confiabilidade do driver) — que permite que o sistema confie totalmente nesses drivers e instale-os mesmo sem credenciais administrativas.

No mínimo, os drivers devem ser assinados por Authenticode, pois os drivers que não são assinados ou auto-assinados (ou seja, assinados com um certificado de teste) não serão instalados em muitas plataformas baseadas no Windows. Para obter mais informações sobre drivers de assinatura e código e recursos relacionados, consulte [requisitos de assinatura de driver para Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) no [Windows hardware Developer Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Resumo

Usar o Microsoft Authenticode é um processo simples. Depois de obter uma CER e criar uma chave privada, é uma simples questão de usar as ferramentas fornecidas pela Microsoft. Você pode habilitar recursos importantes no Windows Vista e no Windows 7, como controles dos pais, e informar aos clientes que seu produto vem diretamente do seu proprietário.

## <a name="more-information"></a>Mais informações

Para obter mais informações sobre ferramentas e processos relacionados ao código de assinatura, consulte os links a seguir:

-   [Ferramentas de criptografia](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referência de ferramentas de API de criptografia](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Visão geral e turtorials Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificados digitais](/windows/desktop/SecCrypto/digital-certificates)
-   [Implantando Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Como criar certificados temporários para uso durante o desenvolvimento](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 