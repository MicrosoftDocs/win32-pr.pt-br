---
title: Objeto de configuração de fluxo
description: Objeto de configuração de fluxo
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- SDK do Windows Media Format, objetos de configuração de fluxo
- ASF (Advanced Systems Format), objetos de configuração de fluxo
- ASF (formato de sistemas avançados), objetos de configuração de fluxo
- objetos, objetos de configuração de fluxo
- objetos de configuração de fluxo
- fluxos, objetos de configuração de fluxo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084397"
---
# <a name="stream-configuration-object"></a>Objeto de configuração de fluxo

Um objeto de configuração de fluxo é usado para especificar as propriedades de um fluxo de mídia em um arquivo ASF. Os objetos de configuração de fluxo podem ser criados para fluxos existentes em um perfil ou podem ser criados em branco, prontos para receber novos dados. Os objetos de configuração de fluxo não podem existir independentemente de um objeto de perfil. Para salvar o conteúdo de um objeto de configuração de fluxo, você deve chamar [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) para adicionar um novo fluxo ou [**IWMProfile:: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) para salvar as alterações feitas em um fluxo existente.

Para criar um objeto de configuração de fluxo, use um dos métodos a seguir.



| Método                                                                | Descrição                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Cria um objeto de configuração de fluxo sem nenhum dado.                                                                          |
| [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Cria um objeto de configuração de fluxo populado com dados de um perfil. Usa o índice de fluxo para identificar o fluxo desejado.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Cria um objeto de configuração de fluxo populado com dados de um perfil. Usa o número de fluxo para identificar o fluxo desejado. |



 

Todos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMStreamConfig** . As outras interfaces do objeto de configuração de fluxo podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte do objeto de configuração de fluxo.



| Interface                                        | Descrição                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Define e recupera a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Define e recupera propriedades que não são necessárias para todos os fluxos, como configurações de taxa de bits variável (VBR).                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Define e recupera todas as informações básicas sobre um fluxo.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Configura os tipos de extensões de unidade de dados associadas ao fluxo. Herda todos os métodos de **IWMStreamConfig**. |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Define e recupera o idioma para o fluxo. Herda todos os métodos de **IWMStreamConfig** e **IWMStreamConfig2**. |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gerencia as propriedades de um fluxo de vídeo. Essa é uma interface opcional e está disponível apenas para fluxos de vídeo.            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> </dl>

 

 




