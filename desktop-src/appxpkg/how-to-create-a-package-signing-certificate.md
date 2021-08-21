---
title: Como criar um certificado de assinatura de pacote de aplicativos
description: Saiba como usar MakeCert.exe e Pvk2Pfx.exe para criar um certificado de assinatura de código de teste, para que você possa assinar seus Windows de aplicativo.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc495c27e63dc4ee3a42db1b2763f4f59f7647a3a98d20193d8049dcfad965c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049064"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>Como criar um certificado de assinatura de pacote de aplicativos

> [!IMPORTANT]
> MakeCert.exe foi preterido. Para obter diretrizes atuais sobre como criar um certificado, consulte [Criar um certificado para assinatura de pacote.](/windows/msix/package/create-certificate-package-signing)

 

Saiba como usar [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) para criar um certificado de assinatura de código de teste, para que você possa assinar seus Windows de aplicativo.

Você deve assinar digitalmente seus aplicativos Windows empacotados antes de implantá-los. Se você não usar o Microsoft Visual Studio 2012 para criar e assinar seus pacotes de aplicativos, precisará criar e gerenciar seus próprios certificados de assinatura de código. Você pode criar certificados [**usando**](/windows-hardware/drivers/devtest/makecert)MakeCert.exee [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) do WDK (Kit de Driver Windows) do Windows. Em seguida, você pode usar os certificados para assinar os pacotes de aplicativos para que eles possam ser implantados localmente para teste.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Pacotes de aplicativos e implantação](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Ferramentas para drivers de assinatura](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Pré-requisitos

-   [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) e [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) ferramentas do WDK

## <a name="instructions"></a>Instruções

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Etapa 1: Determinar o nome do editor do pacote

Para tornar o certificado de assinatura que você cria para uso com o pacote de aplicativos que deseja assinar, o nome da assunto do certificado de assinatura deve corresponder ao atributo **Publisher** do elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no AppxManifest.xml para esse aplicativo. Por exemplo, suponha que o AppxManifest.xml contém:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Para o *parâmetro publisherName* especificado com o utilitário [**MakeCert**](/windows-hardware/drivers/devtest/makecert) na próxima etapa, use "CN=Contoso Software, O=Contoso Corporation, C=US".

> [!Note]  
> Essa cadeia de caracteres de parâmetro é especificada entre aspas e é sensível a minúsculas e espaços em branco.

 

A **Publisher** de atributo definida para o elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) no AppxManifest.xml deve ser idêntica à cadeia de caracteres especificada com o parâmetro [**MakeCert**](/windows-hardware/drivers/devtest/makecert) /n para o nome da assunto do certificado. Copie e copie a cadeia de caracteres sempre que possível.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Etapa 2: Criar uma chave privada usando MakeCert.exe

Use o [**utilitário MakeCert**](/windows-hardware/drivers/devtest/makecert) para criar um certificado de teste auto-assinado e uma chave privada:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Esse comando solicita que você forneça uma senha para o arquivo .pvk. Recomendamos que você escolha uma [senha forte e](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) mantenha sua chave privada em um local seguro.

Recomendamos que você use os parâmetros sugeridos no exemplo anterior por estes motivos:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Cria um certificado raiz auto-assinado. Isso simplifica o gerenciamento do certificado de teste.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Marca a restrição básica para o certificado como uma entidade final. Isso impede que o certificado seja usado como uma AC (Autoridade de Certificação) que pode emitir outros certificados.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Define os valores de EKU (Uso Aprimorado de Chave) para o certificado.

> [!Note]  
> Não coloque um espaço entre os dois valores delimitados por vírgula.

 

-   1.3.6.1.5.5.7.3.3 indica que o certificado é válido para assinatura de código. Sempre especifique esse valor para limitar o uso pretendido para o certificado.
-   1.3.6.1.4.1.311.10.3.13 indica que o certificado respeita a assinatura de tempo de vida. Normalmente, se uma assinatura tiver um carimbo de data/hora, desde que o certificado seja válido no ponto em que foi marcado, a assinatura permanecerá válida mesmo se o certificado expirar. Essa EKU força a assinatura a expirar, independentemente de a assinatura ser marcada com carimbo de data/hora.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Define a data de validade do certificado. Forneça um valor para *o parâmetro expirationDate* no formato mm/dd/aaaa. Recomendamos que você escolha uma data de validade apenas o tempo necessário para suas finalidades de teste, normalmente menos de um ano. Essa data de validade em conjunto com a EKU de assinatura de tempo de vida pode ajudar a limitar a janela na qual o certificado pode ser comprometido e usado indevidamente.

</dd> </dl>

Para obter mais informações sobre outras opções, consulte [**MakeCert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Etapa 3: Criar um arquivo de Exchange (.pfx) usando Pvk2Pfx.exe

Use o [**utilitário Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para converter os arquivos .pvk e .cer criados pelo [**MakeCert**](/windows-hardware/drivers/devtest/makecert) em um arquivo .pfx que você pode usar com [SignTool](/windows/desktop/SecCrypto/signtool) para assinar um pacote de aplicativos:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Os *arquivos MyKey.pvk* e *MyKey.cer* [**são**](/windows-hardware/drivers/devtest/makecert) os mesmosMakeCert.execriados na etapa anterior. Usando o parâmetro /po opcional, você pode especificar uma senha diferente para o .pfx resultante; caso contrário, o .pfx tem a mesma senha *que MyKey.pvk*.

Para obter mais informações sobre outras opções, consulte [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Comentários

Depois de criar o arquivo .pfx, você pode usar o arquivo com [SignTool](/windows/desktop/SecCrypto/signtool) para assinar um pacote de aplicativos. Para obter mais informações, [consulte Como assinar um pacote de aplicativos usando o SignTool.](how-to-sign-a-package-using-signtool.md) Mas o certificado ainda não é confiável pelo computador local para implantação de pacotes de aplicativos até que você o instale no armazenamento de certificados confiáveis do computador local. Você pode usar [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), que vem com Windows.

**Para instalar certificados com WindowsCertutil.exe**

1.  Execute **Cmd.exe** como administrador.
2.  Execute este comando:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Recomendamos que você remova os certificados se eles não estão mais em uso. No mesmo prompt de comando do administrador, execute este comando:

``` syntax
Certutil -delStore TrustedPeople certID
```

O **certID** é o número de série do certificado. Execute este comando para determinar o número de série do certificado:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Considerações de segurança

Ao adicionar um certificado em [repositórios de certificados do computador local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), você afetará a confiança do certificado de todos os usuários no computador. Recomendamos que você instale todos os certificados de assinatura de código que você deseja para testar pacotes de aplicativos no armazenamento de certificados pessoas confiáveis. Remova imediatamente esses certificados quando eles não são mais necessários, para impedir que eles sejam usados para comprometer a confiança do sistema.

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

[Como assinar um pacote de aplicativos usando o SignTool](how-to-sign-a-package-using-signtool.md)
</dt> <dt>

[Assinar um pacote do aplicativo](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 