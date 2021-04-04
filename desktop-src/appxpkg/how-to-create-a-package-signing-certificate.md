---
title: Como criar um certificado de assinatura de pacote de aplicativos
description: Saiba como usar MakeCert.exe e Pvk2Pfx.exe para criar um certificado de assinatura de código de teste, para que você possa assinar seus pacotes de aplicativos do Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007372"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>Como criar um certificado de assinatura de pacote de aplicativos

> [!IMPORTANT]
> MakeCert.exe é preterida. Para obter as diretrizes atuais sobre a criação de um certificado, consulte [criar um certificado para assinatura de pacote](/windows/msix/package/create-certificate-package-signing).

 

Saiba como usar [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) para criar um certificado de assinatura de código de teste, para que você possa assinar seus pacotes de aplicativos do Windows.

Você deve assinar digitalmente seus aplicativos do Windows empacotados antes de implantá-los. Se você não usar Microsoft Visual Studio 2012 para criar e assinar seus pacotes de aplicativos, você precisará criar e gerenciar seus próprios certificados de assinatura de código. Você pode criar certificados usando [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) do Windows Driver Kit (WDK). Em seguida, você pode usar os certificados para assinar os pacotes de aplicativos, para que eles possam ser implantados localmente para teste.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Ferramentas para assinar drivers](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Pré-requisitos

-   Ferramentas de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) do WDK

## <a name="instructions"></a>Instruções

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Etapa 1: determinar o nome do editor do pacote

Para tornar o certificado de autenticação que você cria utilizável com o pacote do aplicativo que você deseja assinar, o nome da entidade do certificado de autenticação deve corresponder ao atributo **Publisher** do elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no AppxManifest.xml para esse aplicativo. Por exemplo, suponha que o AppxManifest.xml contenha:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Para o parâmetro *PublisherName* que você especificar com o utilitário [**MakeCert**](/windows-hardware/drivers/devtest/makecert) na próxima etapa, use "CN = Contoso software, O = Contoso Corporation, C = US".

> [!Note]  
> Essa cadeia de caracteres de parâmetro é especificada entre aspas e diferencia maiúsculas de minúsculas e espaço em branco.

 

A cadeia de caracteres de atributo do **Publicador** definida para o elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no AppxManifest.xml deve ser idêntica à cadeia de caracteres que você especificar com o parâmetro [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n para o nome da entidade do certificado. Copie e cole a cadeia de caracteres sempre que possível.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Etapa 2: criar uma chave privada usando MakeCert.exe

Use o utilitário [**MakeCert**](/windows-hardware/drivers/devtest/makecert) para criar um certificado de teste autoassinado e uma chave privada:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Esse comando solicita que você forneça uma senha para o arquivo. pvk. Recomendamos que você escolha uma [senha forte](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) e mantenha sua chave privada em um local seguro.

É recomendável que você use os parâmetros sugeridos no exemplo anterior por estes motivos:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Cria um certificado raiz autoassinado. Isso simplifica o gerenciamento do seu certificado de teste.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Marca a restrição básica para o certificado como uma entidade final. Isso impede que o certificado seja usado como uma autoridade de certificação (CA) que pode emitir outros certificados.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Define os valores de EKU (uso avançado de chave) para o certificado.

> [!Note]  
> Não coloque um espaço entre os dois valores delimitados por vírgula.

 

-   1.3.6.1.5.5.7.3.3 indica que o certificado é válido para assinatura de código. Sempre Especifique esse valor para limitar o uso pretendido para o certificado.
-   1.3.6.1.4.1.311.10.3.13 indica que o certificado respeita o tempo de vida da assinatura. Normalmente, se uma assinatura tiver o carimbo de data/hora, desde que o certificado tenha sido válido no ponto em que estava carimbado, a assinatura permanecerá válida mesmo se o certificado expirar. Esse EKU força a assinatura a expirar, independentemente de a assinatura ser carimbada pelo tempo.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Define a data de validade do certificado. Forneça um valor para o parâmetro *expirationDate* no formato mm/dd/aaaa. Recomendamos que você escolha uma data de expiração somente se necessário para seus fins de teste, normalmente menos de um ano. Essa data de expiração em conjunto com o EKU de assinatura de tempo de vida pode ajudar a limitar a janela em que o certificado pode ser comprometido e usado indefinidamente.

</dd> </dl>

Para obter mais informações sobre outras opções, consulte [**MakeCert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Etapa 3: criar um arquivo de troca de informações pessoais (. pfx) usando Pvk2Pfx.exe

Use o utilitário [**pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para converter os arquivos. pvk e. cer que o [**MakeCert**](/windows-hardware/drivers/devtest/makecert) criou em um arquivo. pfx que você pode usar com [SignTool](/windows/desktop/SecCrypto/signtool) para assinar um pacote de aplicativo:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Os arquivos *myKey. pvk* e *myKey. cer* são os mesmos arquivos que [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) criados na etapa anterior. Usando o parâmetro opcional/Po, você pode especificar uma senha diferente para o. pfx resultante; caso contrário, o. pfx terá a mesma senha que *myKey. pvk*.

Para obter mais informações sobre outras opções, consulte [**pvk2pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Comentários

Depois de criar o arquivo. pfx, você pode usar o arquivo com [SignTool](/windows/desktop/SecCrypto/signtool) para assinar um pacote de aplicativo. Para obter mais informações, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md). Mas o certificado ainda não é confiável para o computador local para implantação de pacotes de aplicativos até que você o instale no repositório de certificados confiáveis do computador local. Você pode usar [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), que vem com o Windows.

**Para instalar certificados com WindowsCertutil.exe**

1.  Execute **Cmd.exe** como administrador.
2.  Execute este comando:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Recomendamos que você remova os certificados se eles não estiverem mais em uso. No mesmo prompt de comando do administrador, execute este comando:

``` syntax
Certutil -delStore TrustedPeople certID
```

**Certid** é o número de série do certificado. Execute este comando para determinar o número de série do certificado:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Considerações de segurança

Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador. Recomendamos que você instale todos os certificados de assinatura de código desejados para testar pacotes de aplicativos no repositório de certificados de pessoas confiáveis. Remova imediatamente esses certificados quando eles não forem mais necessários, para impedir que eles sejam usados para comprometer a confiança do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Amostras**
</dt> <dt>

[Criar exemplo de pacote de aplicativo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceitos**
</dt> <dt>

[Práticas recomendadas de assinatura de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Como assinar um pacote de aplicativos usando o SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Assinar um pacote do aplicativo](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 