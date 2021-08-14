---
title: Protegendo arquivos com DRM versão 7 ou posterior
description: Protegendo arquivos com DRM versão 7 ou posterior
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows SDK do formato de mídia, criando arquivos protegidos
- Windows SDK do formato de mídia, arquivos protegidos
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
ms.openlocfilehash: fcec136539f9ea5d52fb5c92cf546a965202b35e25bd22010baaf98d8fde7720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846151"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a>Protegendo arquivos com DRM versão 7 ou posterior

para proteger arquivos com Windows Media DRM versão 7 ou posterior, use o método [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) do objeto writer para definir atributos DRM. Como o DRM versão 7 e versões posteriores habilitam licenças exclusivas para cada arquivo protegido ou conjunto de arquivos, a interface **IWMDRMWriter** também tem métodos para criar chaves. Esses métodos são fornecidos apenas para fins de conveniência.

Para proteger os arquivos ASF usando o DRM versão 7 ou posterior, execute as seguintes etapas:

1.  Link para WMStubDRM. lib e, se necessário, desvincular WMVCORE. lib.
2.  Chame a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para criar o gravador de DRM. O primeiro argumento é reservado e deve ser definido como **nulo**.
3.  Defina um perfil para o gravador a ser usado chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) ou [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Você deve definir um perfil no gravador antes de definir qualquer atributo DRM. o DRM só tem suporte para perfis que usam os codecs de vídeo de mídia de áudio Windows mídia ou Windows
4.  Obtenha a interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) do objeto gravador.
5.  Chame [**IWMDRMWriter:: SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) e defina [**usar \_ \_ DRM avançado**](use-advanced-drm.md) como **verdadeiro**.
6.  Se você precisar gerar uma nova semente de chave, chame [**IWMDRMWriter:: GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed). Na maioria dos casos, você usará uma semente de chave que foi gerada anteriormente. Esse valor deve permanecer secreto; Ele não é gravado no arquivo.
7.  Chame [**IWMDRMWriter:: GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) para criar uma ID de chave, que é o segundo valor usado para criar a chave real. Ao contrário da semente de chave, a ID de chave é pública e gravada no arquivo no cabeçalho DRM em Clear. Crie uma nova ID de chave para cada novo arquivo que você criar.
8.  Chame **IWMDRMWriter:: GenerateSigningKeyPair** , se necessário, para gerar uma chave pública e privada que será usada para assinar o objeto de cabeçalho ASF do DRM avançado. Para obter mais informações sobre essas chaves, consulte [**IWMDRMWriter:: GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).
9.  Se necessário, obtenha os valores para preencher o objeto de assinatura digital do cabeçalho DRM. se você não tiver uma versão de trabalho do Windows Media rights Manager instalada em seu sistema, deverá configurar o objeto de assinatura digital do cabeçalho do arquivo ASF especificando os quatro atributos a seguir, que todos devem ser obtidos da Microsoft:

    -   [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)
    -   [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)
    -   [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)
    -   [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)

    se você tiver Windows o gerenciador de direitos de mídia instalado, não será necessário definir esses atributos em seu aplicativo. O componente DRM irá recuperar esses atributos e usá-los para assinar o cabeçalho automaticamente. se você tiver uma versão ativada do Windows Media rights Manager em outro computador e desejar reutilizar esses valores de objeto de assinatura digital, poderá encontrá-los no registro. O certificado do servidor de licença é armazenado em HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ Certificates: cert1 e o certificado raiz é armazenado em hKey \_ local \_ Machine \\ software \\ Microsoft \\ WM Rights Manager \\ License Server \\ certs: cert2. Ao proteger arquivos com o DRM versão 7, você deve usar os valores dessas chaves do registro. para a **\_ propriedade LASignaturePrivKey do DRM**, use **GenerateSigningKeysEx** (por meio do SDK Windows media rights manager) ou, caso contrário, reutilize o valor instalado pelo Windows gerenciador de direitos de mídia em HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ WM rights manager \\ License Server: Info \_ Cert0. para a **propriedade \_ LASignatureCert do DRM** , use **GenerateSigningKeysEx** (por meio do SDK Windows media rights manager) ou, caso contrário, o valor instalado por Windows gerenciador de direitos de mídia em HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ WM rights manager \\ License Server \\ certs: cert0.

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
12. se necessário, crie uma licença para o arquivo usando Windows gerenciador de direitos de mídia. Essa tarefa também pode ser executada por um servidor de licença de terceiros. Para cenários de DRM ao vivo, os usuários finais precisarão obter uma licença antes do início do fluxo, ou no momento em que tentarem se conectar a ele pela primeira vez.

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

 

 




