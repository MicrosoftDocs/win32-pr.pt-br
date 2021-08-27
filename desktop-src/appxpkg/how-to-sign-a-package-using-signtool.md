---
title: Como assinar um pacote do aplicativo usando a SignTool
description: saiba como usar o SignTool para assinar seus pacotes de aplicativo Windows para que eles possam ser implantados.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4e4c0941cbcced30053b8fd31e44100adc9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474882"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Como assinar um pacote do aplicativo usando a SignTool

> [!Note]  
> para assinar um pacote de aplicativo Windows, consulte [assinar um pacote de aplicativo usando SignTool](/windows/msix/package/sign-app-package-using-signtool).

 

saiba como usar o [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar seus pacotes de aplicativo Windows para que eles possam ser implantados. o [**SignTool**](/windows-hardware/drivers/devtest/signtool) faz parte do SDK (Software Development Kit) do Windows.

todos os pacotes de aplicativos Windows devem ser assinados digitalmente antes que possam ser implantados. embora Microsoft Visual Studio 2012 e posterior possam assinar um pacote de aplicativo durante sua criação, os pacotes que você cria usando a ferramenta [MakeAppx.exe (app packager)](make-appx-package--makeappx-exe-.md) do SDK do Windows não são assinados.

> [!Note]  
> você só pode usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar seus pacotes de aplicativos Windows no Windows 8 e posterior ou Windows Server 2012 e posterior. você não pode usar **SignTool** para assinar pacotes de aplicativos em sistemas operacionais de nível inferior, como Windows 7 ou Windows Server 2008 R2.

 

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Ferramentas para assinar arquivos e verificar assinaturas](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Pré-requisitos

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), que faz parte do SDK do Windows
-   um certificado de assinatura de código válido, por exemplo, um arquivo de informações pessoais Exchange (. pfx) criado com as ferramentas [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)

    Para obter informações sobre como criar um certificado de assinatura de código válido, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).

-   um aplicativo de Windows empacotado, por exemplo, um arquivo. appx criado usando a ferramenta do [app packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)

**Considerações adicionais**

O certificado que você usa para assinar o pacote de aplicativo deve atender a estes critérios:

-   o nome da entidade do certificado deve corresponder ao atributo **Publisher** que está contido no elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) do arquivo AppxManifest.xml armazenado no pacote. o nome do editor faz parte da identidade de um aplicativo Windows empacotado, portanto, você precisa fazer com que o nome da entidade do certificado corresponda ao nome do editor do aplicativo. Isso permite que a identidade de pacotes assinados seja verificada em relação à assinatura digital. Para obter informações sobre erros de assinatura que podem surgir na assinatura de um pacote de aplicativo usando [**SignTool**](/windows-hardware/drivers/devtest/signtool), consulte a seção comentários de [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).
-   O certificado deve ser válido para assinatura de código. Isso significa que ambos os itens devem ser verdadeiros:

    -   O campo EKU (uso estendido de chave) do certificado deve ser desdefinido ou conter o valor de EKU para assinatura de código (1.3.6.1.5.5.7.3.3).
    -   O campo uso de chave (KU) do certificado deve ser desdefinido ou conter o bit de uso para a assinatura digital (0x80).

-   O certificado contém uma chave privada.
-   O certificado é válido. Ele está ativo, não expirou e não foi revogado.

## <a name="instructions"></a>Instruções

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Etapa 1: determinar o algoritmo de hash a ser usado

Ao assinar o pacote do aplicativo, você deve usar o mesmo algoritmo de hash que usou quando criou o pacote do aplicativo. Se você usou as configurações padrão para criar o pacote do aplicativo, o algoritmo de hash usado é SHA256.

Se você usou o app Packager com um algoritmo de hash específico para criar o pacote do aplicativo, use o mesmo algoritmo para assinar o pacote. Para determinar o algoritmo de hash a ser usado para assinar um pacote, você pode extrair o conteúdo do pacote e inspecionar o arquivo de AppxBlockMap.xml. O atributo **HashMethod** do elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica o algoritmo de hash que foi usado ao criar o pacote do aplicativo. Por exemplo:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

O elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) anterior indica que o algoritmo SHA256 foi usado. Esta tabela lista o mapeamento dos algoritmos disponíveis no momento:

| Valor de **HashMethod**                            | *hashAlgorithm* para usar |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (padrão. AppX) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Etapa 2: executar SignTool.exe para assinar o pacote

**Para assinar o pacote com um certificado de autenticação de um arquivo. pfx**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) padroniza o parâmetro/FD *hashAlgorithm* para SHA1 se não for especificado, e SHA1 não é válido para assinar pacotes de aplicativos. Portanto, você deve especificar esse parâmetro ao assinar um pacote de aplicativo. Para assinar um pacote de aplicativo que foi criado com o hash SHA256 padrão, você especifica o parâmetro/FD *hashAlgorithm* como SHA256:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

Você pode omitir o parâmetro/p *password* se usar um arquivo. pfx que não seja protegido por senha. Você também pode usar outras opções de seleção de certificado com suporte de [**SignTool**](/windows-hardware/drivers/devtest/signtool) para assinar pacotes de aplicativos. Para obter mais informações sobre essas opções, consulte [SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> Não é possível usar a operação de carimbo de data/hora de [**SignTool**](/windows-hardware/drivers/devtest/signtool) em um pacote de aplicativo assinado; Não há suporte para a operação.

 

Se desejar marcar o data/hora do pacote do aplicativo, você deverá fazê-lo durante a operação de entrada. Por exemplo:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Torne o parâmetro/TR *timestampServerUrl* igual à URL de um servidor de carimbo de data/hora RFC 3161.

## <a name="remarks"></a>Comentários

Esta seção aborda a solução de problemas de erros de assinatura para pacotes de aplicativos.

### <a name="troubleshooting-app-package-signing-errors"></a>Solucionando problemas de erros de assinatura de pacote de aplicativo

Além dos erros de assinatura que o [**SignTool**](/windows-hardware/drivers/devtest/signtool) pode retornar, o **SignTool** também pode retornar erros que são específicos para a assinatura de pacotes de aplicativos. Esses erros geralmente aparecem como erros internos:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Se o código de erro começar com 0x8008, como o 0x80080206 APPX \_ E o \_ conteúdo corrompido \_ ), isso indicará que o pacote que está sendo assinado é inválido. Nesse caso, antes de poder assinar o pacote, você deve recompilar o pacote. Para obter a lista completa de \* erros de 0x8008, consulte [**códigos de erro com (segurança e configuração)**](/windows/desktop/com/com-error-codes-4).

Mais comumente, o erro é 0x8007000B ( \_ formato inadequado do erro \_ ). Nesse caso, você pode encontrar informações de erro mais específicas no log de eventos:

**Para pesquisar o log de eventos**

1.  Execute eventvwr. msc.
2.  abra o log de eventos: Visualizador de Eventos (Local) > Logs de aplicativos e serviços > microsoft > Windows > AppxPackagingOM > microsoft-Windows-AppxPackaging/operational
3.  Procure o evento de erro mais recente.

O erro interno geralmente corresponde a um destes:


| ID do evento | Cadeia de caracteres de evento de exemplo | Sugestão | 
|----------|----------------------|------------|
| 150 | Erro 0x8007000B: O nome do editor de manifesto de aplicativo (CN = Contoso) deve coincidir com o nome do requerente do certificado de autenticação (CN = Contoso, C = US). | O nome do editor de manifesto de aplicativo deve corresponder exatamente ao nome do assunto após a assinatura.<blockquote>[!Note]<br />Esses nomes são especificados entre aspas e são diferenciais de maiúsculas e minúsculas e de espaço em branco.</blockquote><br /> você pode atualizar a cadeia de caracteres do atributo <strong>Publisher</strong> que é definida para o elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> no arquivo AppxManifest.xml para corresponder ao nome da entidade do certificado de autenticação pretendido. Ou então, selecione um certificado de autenticação diferente com um nome de entidade que corresponda ao nome do editor do manifesto do aplicativo. O nome do editor do manifesto e o nome da entidade do certificado estão listados na mensagem do evento. | 
| 151 | Erro 0x8007000B: O método de hash de assinatura especificado (SHA512) deve coincidir com o método de hash usado no mapa de blocos do pacote de aplicativos (SHA256). | O hashAlgorithm especificado no parâmetro/FD está incorreto (consulte a etapa 1: determinar o algoritmo de hash a ser usado). Execute o <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> novamente com o hashAlgorithm que corresponde ao mapa do bloco do pacote do aplicativo. | 
| 152 | Erro 0x8007000B: O conteúdo do pacote de aplicativos deve ser validado em relação ao mapa de blocos. | O pacote de aplicativos está corrompido e precisa ser recompilado para gerar um novo mapa de blocos. para obter mais informações sobre como criar um pacote de aplicativo, consulte criando um pacote de aplicativo com o <a href="make-appx-package--makeappx-exe-.md">app packager</a> ou <a href="/previous-versions/hh975357(v=vs.110)">criando um pacote de aplicativo com o Visual Studio 2012</a>. | 




 

## <a name="security-considerations"></a>Considerações de segurança

Depois que o pacote é assinado, o certificado que você usou para assinar o pacote ainda deve ser confiável pelo computador no qual o pacote será implantado. Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador. Recomendamos que você instale os certificados de assinatura de código que deseja para testar pacotes de aplicativos no repositório de certificados de pessoas confiáveis e remova esses certificados imediatamente quando não forem mais necessários. Se você criar seus próprios certificados de teste para assinar pacotes de aplicativos, também recomendamos que você restrinja os privilégios associados ao certificado de teste. Para obter mais informações sobre como criar certificados de teste para assinar pacotes de aplicativos, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Amostras**
</dt> <dt>

[Criar exemplo de pacote de aplicativos](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceitos**
</dt> <dt>

[Práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Assinando um pacote no Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[Empacotador de aplicativos (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[Como criar um certificado de assinatura de pacote de aplicativos](how-to-create-a-package-signing-certificate.md)
</dt> </dl>

