---
title: Autenticação authenticode para desenvolvedores de jogos
description: Este artigo discute como começar a autenticar seu jogo e como integrar a autenticação em um processo de build diário.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256b1cec0693787e76cfa479940524fca28d508e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436451"
---
# <a name="authenticode-signing-for-game-developers"></a>Autenticação authenticode para desenvolvedores de jogos

A autenticação de dados é cada vez mais importante para desenvolvedores de jogos. Windows O Vista e Windows 7 têm vários recursos, como controles dos pais, que exigem que os jogos sejam assinados corretamente para garantir que ninguém tenha adulterado os dados. O Microsoft Authenticode permite que os usuários finais e o sistema operacional verifiquem se o código do programa vem do proprietário correto e se ele não foi alterado ou corrompido acidentalmente. Este artigo discute como começar a autenticar seu jogo e como integrar a autenticação em um processo de build diário.

-   [Tela de fundo](#background)
-   [Introdução](#getting-started)
-   [Usando uma autoridade de certificação confiável](#using-a-trusted-certificate-authority)
-   [Exemplo usando um certificado de teste](#example-using-a-test-certificate)
-   [Integrando a entrada de código no sistema de build diário](#integrating-code-signing-into-the-daily-build-system)
-   [Revogação](#revocation)
-   [Drivers de assinatura de código](#code-signing-drivers)
-   [Resumo](#summary)
-   [Mais informações](#more-information)

> [!Note]  
> A partir de 1º de janeiro de 2016, o Windows 7 e posterior não confiam mais em nenhum certificado de assinatura de código SHA-1 com uma data de validade de 1º de janeiro de 2016 ou posterior. Confira [Windows imposição da assinatura de código Authenticode e o data/hora para](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) obter mais informações.

 

## <a name="background"></a>Tela de fundo

Certificados digitais são usados para estabelecer a identidade do autor. Certificados digitais são emitidos por um terceiro confiável conhecido como UMA (Autoridade de Certificação), como VeriSign ou Thawte. A AC é responsável por verificar se o proprietário não está reivindicando uma identificação falsa. Depois de aplicar a uma AC para um certificado, os desenvolvedores comerciais podem esperar uma resposta para seu aplicativo em menos de duas semanas.

Depois que a AC decide que você atende aos seus critérios de política, ela gera um certificado de assinatura de código que está em conformidade com x.509, o formato de certificado padrão do setor criado pela União Internacional de Telecomunicações, com extensões da Versão 3. Esse certificado identifica você e contém sua chave pública. Ele é armazenado pela AC para referência e uma cópia é dada a você eletronicamente. Ao mesmo tempo, você também cria uma chave privada, que deve ser segura e que você não deve compartilhar com ninguém, nem mesmo com a AC.

Depois de ter uma chave pública e privada, você pode começar a distribuir software assinado. A Microsoft fornece ferramentas para fazer isso no SDK do Windows. As ferramentas utilizam um hash único, produzem um resumo de comprimento fixo e geram uma assinatura criptografada com uma chave privada. Em seguida, eles combinam essa assinatura criptografada com seu certificado e suas credenciais em uma estrutura conhecida como um bloco de assinatura e a inscriem no formato de arquivo do executável. Qualquer tipo de arquivo binário executável pode ser assinado, incluindo DLLs, arquivos executáveis e arquivos de gabinete.

A assinatura pode ser verificada de várias maneiras. Os programas podem chamar a função CertVerifyCertificateChainPolicy e SignTool (signtool.exe) podem ser usados para verificar uma assinatura no prompt de linha de comando. Windows O Explorer também tem uma guia Assinaturas Digitais em Propriedades do Arquivo que exibe cada certificado de um arquivo binário assinado. (A guia Assinaturas Digitais só aparece em Propriedades do Arquivo para arquivos assinados.) Além disso, um aplicativo pode ser auto-verificar com o [**uso de CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

A assinatura authenticode não só é útil para autenticação de dados por usuários finais, mas também é necessária para a adoção de patch de Contas de Usuário Limitadas e por controles dos pais no Windows Vista e Windows 7. Além disso, as tecnologias futuras Windows sistemas operacionais também podem exigir que o código seja assinado, portanto, é fortemente aconselhável que todos os desenvolvedores profissionais e desenvolvedores de desenvolvedores adquiram um certificado de assinatura de código de uma AC. Mais informações sobre como isso é feito podem ser encontradas posteriormente neste artigo em [Usando uma autoridade de certificação confiável.](#using-a-trusted-certificate-authority)

O código do jogo, os patchers e os instaladores podem aproveitar ainda mais a assinatura do Authenticode verificando se os arquivos são autenticados no código. Isso pode ser usado para proteção contra fraudes e segurança de rede geral. O código de exemplo para verificar se um arquivo está assinado pode ser encontrado aqui: Programa C de [exemplo:](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)verificando a assinatura de um arquivo PE e o código de exemplo para verificar a propriedade de um certificado de autenticação em um arquivo assinado pode ser encontrado aqui: [How To Get Information from Authenticode Signed Executables](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Introdução

Para começar, a Microsoft fornece ferramentas com o Visual Studio 2005 e o Visual Studio 2008 e no [SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)do Windows para ajudar a executar e verificar o processo de assinatura de código. Depois de instalar o Visual Studio ou o SDK do Windows, as ferramentas descritas neste artigo técnico estão localizadas em um subdiretório da instalação, que pode incluir um ou mais dos seguintes:

-   %SystemDrive% \\ Program Files Microsoft Visual Studio \\ 8 \\ SDK \\ v2.0 \\ Bin
-   %SystemDrive% \\ Program Files Microsoft Visual Studio \\ 8 VC \\ \\ PlatformSDK \\ Bin
-   %SystemDrive% \\ Program Files Microsoft Visual Studio \\ \\ SDK do SDK do SmartDevices 9.0Tools \\ \\\\
-   %SystemDrive% \\ Program Files Microsoft \\ SDKs \\ Windows \\ v6.0A \\ bin\\

As ferramentas a seguir são as mais úteis para assinar código:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Ferramenta de Criação de Certificado (MakeCert.exe)
</dt> <dd>

Gera um certificado X.509 de teste, como um arquivo .cer, que contém sua chave pública e uma chave privada, como um arquivo .pvk. Esse certificado é apenas para fins de teste interno e não pode ser usado publicamente.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Cria um arquivo de Exchange (.pfx) de um par de arquivos .cer e .pvk. O arquivo .pfx contém sua chave pública e privada.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Assina o arquivo usando o arquivo .pfx. O SignTool dá suporte à assinatura de arquivos DLL, arquivos executáveis, arquivos .msi (instalador Windows) e arquivos de gabinete (.cab).

</dd> </dl>

> [!Note]  
> Durante a leitura de outra documentação, você pode encontrar referências ao SignCode (SignCode.exe), mas essa ferramenta foi preterida e não tem mais suporte– use SignTool em vez disso.

 

## <a name="using-a-trusted-certificate-authority"></a>Usando uma autoridade de certificação confiável

Para obter um certificado confiável, você deve aplicar a uma AC (Autoridade de Certificação), como VeriSign ou Thawte. A Microsoft não recomenda nenhuma AC em vez de outra, mas se você quiser integrar-se ao serviço wer (Relatório de Erros do Windows), considere usar o VeriSign para emitir o certificado, pois acessar o banco de dados WER requer uma conta WinQual que requer uma ID do VeriSign. Para ver uma lista completa de autoridades de certificação de terceiros confiáveis, consulte Membros do [Programa de Certificado Raiz da Microsoft](/previous-versions/ms995347(v=msdn.10)). Para obter mais informações sobre como registrar-se com o WER, consulte "[Introducing Relatório de Erros do Windows](https://msdn.microsoft.com/)" in [ISV Zone](https://msdn.microsoft.com/).

Depois de receber seu certificado da AC, você pode assinar seu programa usando SignTool e liberar seu programa para o público. No entanto, você deve ter cuidado para proteger sua chave privada, que está contida nos arquivos .pfx e .pvk. Certifique-se de manter esses arquivos em um local seguro.

## <a name="example-using-a-test-certificate"></a>Exemplo usando um certificado de teste

As etapas a seguir demonstram a criação de um certificado de assinatura de código para fins de teste, seguido pela assinatura de um programa de exemplo direct3D (chamado BasicHLSL.exe) com esse certificado de teste. Este procedimento cria arquivos .cer e .pvk — suas chaves públicas e privadas, respectivamente — que não podem ser usados para certificação pública.

Neste exemplo, um carimbo de data/hora também é adicionado à assinatura. Um carimbo de data/hora impede que a assinatura se torne inválida quando o certificado expirar. O código assinado, mas sem um carimbo de data/hora, não será validado depois que o certificado expirar. Portanto, todo o código lançado publicamente deve ter um carimbo de data/hora.

**Para criar um certificado e assinar um programa**

1.  Crie um certificado de teste e uma chave privada usando a Ferramenta de Criação de Certificado (MakeCert.exe).

    O exemplo de linha de comando a seguir especifica MyPrivateKey como o nome do arquivo de chave privada (.pvk), MyPublicKey como o nome do arquivo de certificado (.cer) e MySoftwareCompany como o nome do certificado. Ele também faz com que o certificado seja auto-assinado, de modo que ele não tenha uma autoridade raiz não confiança.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Crie um arquivo de Exchange (.pfx) de sua chave privada (.pvk) arquivo e arquivo de certificado (.cer) usando pvk2pfx.exe.

    O arquivo .pfx combina suas chaves públicas e privadas em um único arquivo. O exemplo de linha de comando a seguir usa os arquivos .pvk e .cer da etapa anterior para criar o arquivo .pfx chamado MyPFX com a senha sua \_ senha:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Assine seu programa com seu arquivo de Exchange (.pfx) usando SignTool.

    Você pode especificar várias opções na linha de comando. O exemplo de linha de comando a seguir usa o arquivo .pfx da etapa anterior, fornece sua senha como a senha, especifica BasicHLSL como o arquivo a ser assinado e recupera um carimbo de data/hora de um \_ servidor especificado:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > A URL para o serviço de carimbo de data/hora é fornecida pela AC e é opcional para teste. É importante que a assinatura de produção inclua uma autoridade de carimbo de data/hora válida ou a assinatura não será validada quando o certificado expirar.

     

4.  Verifique se o programa está assinado usando SignTool.

    O exemplo de linha de comando a seguir especifica que o SignTool deve tentar verificar a assinatura no BasicHLSL.exe usando todos os métodos disponíveis ao fornecer uma saída detalhada:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    Neste exemplo, SignTool deve indicar que o certificado está anexado, embora também indique que ele não é confiável, pois ele não é emitido por uma AC.

5.  Confie no certificado de teste.

    Para certificados de teste, você precisa confiar no certificado. Essa etapa deve ser ignorada para certificados fornecidos por uma AC, pois eles serão confiáveis por padrão.

    Somente nos computadores em que você deseja confiar no certificado de teste, execute o seguinte:

    ```
    certmgr.msc
    ```

    

    Em seguida, clique com o botão direito do mouse em Autoridades de Certificação Raiz Confiáveis e escolha Importação de Todas as \| Tarefas. Em seguida, navegue até o arquivo .pfx que você criou e siga as etapas do assistente, colocando o certificado nas Autoridades de Certificação Raiz Confiáveis.

    Quando o assistente for concluído, você poderá começar a testar com o certificado confiável nesse computador.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integrando a entrada de código no sistema de build diário

Para integrar a entrada de código em um projeto, você pode criar um arquivo ou script em lotes para executar as ferramentas de linha de comando. Depois que o projeto for criado, execute SignTool com as configurações apropriadas (conforme mostrado na etapa 3 de nosso exemplo).

Tenha especialmente cuidado em seu processo de build para garantir que o acesso aos arquivos .pfx e .pvk seja restrito ao menos computadores e usuários possível. Como melhor prática, os desenvolvedores só devem assinar código usando o certificado de teste até que eles estão prontos para enviar. Novamente, a chave privada (.pvk) deve ser mantida em um local seguro, como uma sala segura ou bloqueada e, idealmente, em um dispositivo criptográfico, como um cartão inteligente.

Outra camada de proteção é fornecida usando o Microsoft Authenticode para assinar o pacote Windows (MSI) em si. Isso ajuda a proteger o pacote MSI contra adulterações e danos acidentais. Consulte a documentação da ferramenta de criação do MSI para obter mais informações sobre como assinar pacotes com o Authenticode.

## <a name="revocation"></a>Revogação

Se a segurança da chave privada estiver comprometida ou algum evento relacionado à segurança renderizar um certificado Code-Signing inválido, o desenvolvedor deverá revogar o certificado. Não fazer isso diminuiria a integridade do desenvolvedor e a eficácia da assinatura de código. Uma AC também pode emitir uma revogação com hora específica; O código assinado com um carimbo de data/hora antes da hora da revogação ainda será considerado válido, mas o código com um carimbo de data/hora subsequente será inválido. A revogação de certificado afeta o código em todos os aplicativos assinados com o certificado revogado.

## <a name="code-signing-drivers"></a>drivers Code-Signing de Code-Signing

Os drivers podem e devem ser assinados por Authenticode. Os drivers de modo kernel têm requisitos adicionais: as edições de 64 bits do Windows Vista e do Windows 7 impedirão a instalação de todos os drivers de modo kernel não assinados e todas as versões do Windows apresentarão um prompt de aviso quando um usuário tentar instalar um driver sem sinal. Além disso, os administradores podem definir Política de Grupo para impedir que drivers não assinados são instalados no Microsoft Windows Server 2003, no Windows XP Professional x64 Edition e nas edições de 32 bits do Windows Vista e Windows 7.

Muitos tipos de drivers podem ser assinados com uma assinatura confiável da Microsoft – como parte do Programa de Certificação do Windows do Windows WHQL [(Hardware Quality Labs)](https://www.microsoft.com/whdc/whql/) ou do Programa de Assinatura Não Classificado [(anteriormente](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) chamado de Assinatura de Confiabilidade do Driver), que permite que o sistema confie totalmente nesses drivers e instale-os mesmo sem credenciais administrativas.

No mínimo, os drivers devem ser assinados por Authenticode, porque os drivers não assinados ou auto-assinados (ou seja, assinados com um certificado de teste) não serão instalados em muitas plataformas baseadas em Windows. Para obter mais informações sobre como assinar drivers e código e recursos relacionados, consulte [Requisitos](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) de assinatura de driver para Windows no [Windows Hardware Developer Central](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Resumo

Usar o Microsoft Authenticode é um processo simples. Depois de obter uma CER e criar uma chave privada, é uma simples questão de usar as ferramentas fornecidas pela Microsoft. Em seguida, você pode habilitar recursos importantes no Windows Vista e Windows 7, como controles dos pais, e permitir que os clientes saibam que seu produto vem diretamente de seu proprietário legítimo.

## <a name="more-information"></a>Mais informações

Para obter mais informações sobre ferramentas e processos relacionados à assinatura de código, consulte os links a seguir:

-   [Ferramentas de criptografia](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referência das Ferramentas de API de Criptografia](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Visão geral e tutorial do Authenticode](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificados Digitais](/windows/desktop/SecCrypto/digital-certificates)
-   [Implantando o Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Como criar certificados temporários para uso durante o desenvolvimento](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
