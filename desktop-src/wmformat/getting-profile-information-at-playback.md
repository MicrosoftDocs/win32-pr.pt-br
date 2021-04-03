---
title: Obtendo informações de perfil na reprodução
description: Obtendo informações de perfil na reprodução
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- SDK do Windows Media Format, perfis
- ASF (Advanced Systems Format), perfis
- ASF (formato de sistemas avançados), perfis
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- ASF (Advanced Systems Format), compartilhamento de largura de banda
- ASF (formato de sistemas avançados), compartilhamento de largura de banda
- fluxos, obtendo informações de perfil na reprodução
- perfis, obtendo informações em reprodução
- exclusão mútua, obtendo informações de perfil na reprodução
- compartilhamento de largura de banda, obtendo informações de perfil em reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084362"
---
# <a name="getting-profile-information-at-playback"></a>Obtendo informações de perfil na reprodução

As informações do perfil usado para criar um arquivo são armazenadas na seção de cabeçalho do arquivo. Ambos os objetos de leitura podem acessar as informações de perfil do cabeçalho do arquivo. Há várias razões pelas quais você pode querer acessar dados de perfil do leitor. Normalmente, você precisará recuperar informações sobre fluxos, objetos de exclusão mútua e objetos de compartilhamento de largura de banda.

O objeto leitor assíncrono e o objeto leitor síncrono podem ser consultados para a interface [**IWMProfile**](iwmprofile.md) . Nenhuma alteração feita nas informações do perfil pode afetar o arquivo no leitor. Para obter mais informações sobre como acessar informações de perfil, consulte [trabalhando com perfis](working-with-profiles.md).

## <a name="stream-information"></a>Informações de fluxo

Às vezes, é importante saber como um fluxo é configurado. Ao recuperar propriedades de mídia de qualquer um dos objetos de leitor, você obtém as propriedades das saídas. As propriedades de saída descrevem como os dados descompactados de um fluxo serão entregues pelo leitor, e não como o fluxo é configurado no arquivo ASF.

Ao receber amostras de fluxo não compactado de um objeto de leitor, você deve usar as informações de perfil para identificar o formato dos dados compactados. Isso é particularmente importante se você pretende gravar o fluxo compactado em outro arquivo ASF.

Você também precisa acessar as informações de fluxo ao usar a recompactação inteligente para transcodificar um fluxo de áudio para uma taxa de bits inferior.

Talvez você queira determinar se um fluxo foi gravado usando a codificação de taxa de bits variável (VBR). Você não pode acessar nenhuma informação de VBR da interface **IWMProfile** de um objeto de leitor. Isso ocorre porque as informações de VBR não são armazenadas no arquivo após a codificação. Você pode determinar se um fluxo foi criado usando a codificação de VBR, obtendo um ponteiro para a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) do objeto leitor e chamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname). Você deve especificar o número do fluxo e passar g \_ wszIsVBR como o nome do atributo.

## <a name="mutual-exclusion-information"></a>Informações de exclusão mútua

Se você quiser criar um aplicativo de leitura que usa a exclusão mútua, você desejará acessar as informações sobre todos os objetos de exclusão mútua incluídos no perfil. Para todos os tipos de exclusão mútua, exceto a taxa de bits, o aplicativo de leitura é responsável por qualquer alternância de fluxo que seja necessária. Para alternar fluxos, você precisa saber quais fluxos são.

## <a name="bandwidth-sharing-information"></a>Informações de compartilhamento de largura de banda

Os objetos de compartilhamento de largura de banda que são incluídos em um perfil são incluídos apenas para fins informativos. Nem o objeto Writer nem qualquer um dos objetos de leitor executa nenhuma ação como resultado de dados de compartilhamento de largura de banda. Se você quiser usar o compartilhamento de largura de banda em seu aplicativo de leitura, deverá acessar as informações de compartilhamento de largura de banda dos dados de perfil.

> [!Note]  
> Nem todas as informações do perfil usado para criar um arquivo estão presentes no cabeçalho do arquivo. Como regra geral, os dados que são usados somente no momento da codificação não são persistidos no arquivo. Isso inclui configurações de entrada que foram definidas usando o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , bem como propriedades definidas usando o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




