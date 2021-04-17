---
title: Protegendo arquivos com DRM versão 7 ou posterior
description: Protegendo arquivos com DRM versão 7 ou posterior
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- SDK do Windows Media Format, criando arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), criando arquivos protegidos
- ASF (formato de sistemas avançados), criando arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, criando arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105773062"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protegendo arquivos com DRM versão 7 ou posterior

Para proteger arquivos com o Windows Media DRM versão 7 ou posterior, use o método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) do objeto Writer para definir atributos DRM. Como o DRM versão 7 e versões posteriores habilitam licenças exclusivas para cada arquivo protegido ou conjunto de arquivos, a interface **IWMDRMWriter** também tem métodos para criar chaves. Esses métodos são fornecidos apenas para fins de conveniência.

Para proteger os arquivos ASF usando o DRM versão 7 ou posterior, execute as seguintes etapas:

1.  Link para WMStubDRM. lib e, se necessário, desvincular WMVCORE. lib.
2.  Chame a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para criar o gravador de DRM. O primeiro argumento é reservado e deve ser definido como **nulo**.
3.  Defina um perfil para o gravador a ser usado chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Você deve definir um perfil no gravador antes de definir qualquer atributo DRM. Somente há suporte para DRM para perfis que usam os codecs de vídeo do Windows Media Audio ou Windows Media
4.  Obtenha a interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) do objeto gravador.
5.  Chame [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e defina [**usar \_ \_ DRM avançado**](use-advanced-drm.md) como **verdadeiro**.
6.  Se você precisar gerar uma nova semente de chave, chame [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). Na maioria dos casos, você usará uma semente de chave que foi gerada anteriormente. Esse valor deve permanecer secreto; Ele não é gravado no arquivo.
7.  Chame [**IWMDRMWriter:: GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) para criar uma ID de chave, que é o segundo valor usado para criar a chave real. Ao contrário da semente de chave, a ID de chave é pública e gravada no arquivo no cabeçalho DRM em Clear. Crie uma nova ID de chave para cada novo arquivo que você criar.
8.  Chame **IWMDRMWriter:: GenerateSigningKeyPair** , se necessário, para gerar uma chave pública e privada que será usada para assinar o objeto de cabeçalho ASF do DRM avançado. Para obter mais informações sobre essas chaves, consulte [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Se necessário, obtenha os valores para preencher o objeto de assinatura digital do cabeçalho DRM. Se você não tiver uma versão de trabalho do Windows Media Rights Manager instalada em seu sistema, deverá configurar o objeto de assinatura digital do cabeçalho do arquivo ASF especificando os quatro atributos a seguir, que todos devem ser obtidos da Microsoft:

    -   [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)
    -   [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)
    -   [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)
    -   [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)

    Se você tiver o Windows Media Rights Manager instalado, não será necessário definir esses atributos em seu aplicativo. O componente DRM irá recuperar esses atributos e usá-los para assinar o cabeçalho automaticamente. Se você tiver uma versão ativada do Windows Media Rights Manager em outro computador e desejar reutilizar esses valores de objeto de assinatura digital, poderá encontrá-los no registro. O certificado do servidor de licença é armazenado em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ Certificates: cert1 e o certificado raiz é armazenado em hKey \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert2. Ao proteger arquivos com o DRM versão 7, você deve usar os valores dessas chaves do registro. Para a **\_ Propriedade LASignaturePrivKey do DRM**, use **GenerateSigningKeysEx** (por meio do SDK do Windows Media Rights Manager) ou, caso contrário, reutilize o valor instalado pelo Windows Media Rights Manager em hKey \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server: info \_ Cert0. Para a **propriedade \_ LASignatureCert do DRM** , use o **GenerateSigningKeysEx** (por meio do SDK do Windows Media Rights Manager) ou o valor instalado pelo Windows Media Rights Manager em hKey \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert0.

10. Chame [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) quantas vezes forem necessárias para configurar o objeto Writer, que definirá os atributos de cabeçalho DRM necessários, conforme necessário. Essas propriedades persistem durante o tempo de vida do objeto do gravador ou até que sejam redefinidas com um novo valor. Eles não precisam ser redefinidos para cada novo arquivo que você criar.

    As propriedades a seguir são exigidas pelo objeto do gravador:

    -   [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)
    -   [**Keysemente DRM \_**](drm-keyseed.md)
    -   [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)
    -   [**\_Keyid DRM**](drm-keyid.md)
    -   [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)

    As propriedades a seguir são opcionais:

    -   [**\_ContentId DRM**](drm-contentid.md)
    -   [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)

    Além disso, você pode especificar atributos de arquivo DRM definidos pelo usuário diretamente usando o atributo base [**\_ DRMHeader do DRM**](drm-drmheader.md) . Você pode adicionar qualquer atributo adicional que desejar, como "DRMHeader. RequireSAP", por exemplo, como uma maneira de comunicar informações adicionais que serão usadas pelo servidor de licença na criação da licença. O servidor de licença deve estar ciente antecipado de quaisquer propriedades adicionais que você adicionar. Não é possível descobrir propriedades desconhecidas de forma programática.

11. Grave o arquivo usando os métodos de interface [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) conforme descrito em outro lugar nesta documentação. Para criar um fluxo do DRM ao vivo, basta gravar em um coletor de rede. Você também pode gravar em um coletor de push.
12. Se necessário, crie uma licença para o arquivo usando o Windows Media Rights Manager. Essa tarefa também pode ser executada por um servidor de licença de terceiros. Para cenários de DRM ao vivo, os usuários finais precisarão obter uma licença antes do início do fluxo, ou no momento em que tentarem se conectar a ele pela primeira vez.

**Observação** O DRM não é compatível com a versão baseada em x64 deste SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Atributos**](attributes.md)
</dt> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> <dt>

[**Interface IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Lendo arquivos protegidos**](reading-protected-files.md)
</dt> <dt>

[**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




