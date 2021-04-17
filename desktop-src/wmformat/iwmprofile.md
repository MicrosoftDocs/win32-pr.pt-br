---
title: Interface IWMProfile
description: A interface IWMProfile é a interface primária para um objeto de perfil.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Formato de mídia do Windows da interface IWMProfile
- Formato de mídia do Windows da interface IWMProfile, descrito
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "105811895"
---
# <a name="iwmprofile-interface"></a>Interface IWMProfile

A interface **IWMProfile** é a interface primária para um objeto de [*perfil*](wmformat-glossary.md) . Um objeto de perfil é usado para configurar perfis personalizados. Você pode usar **IWMProfile** para criar, excluir ou modificar objetos de configuração de fluxo e objetos de exclusão mútua. Você também pode definir e recuperar informações gerais sobre o perfil. Para acessar todos os recursos do objeto de perfil, você deve usar [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3), que herda de **IWMProfile** e [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2).

O **IWMProfile** também é acessível por meio do objeto leitor, onde você pode usá-lo para obter informações sobre os fluxos de um arquivo que é carregado no leitor. Ao acessar o **IWMProfile** do leitor, você pode fazer alterações no perfil, mas nenhuma das alterações pode ser salva no arquivo. Geralmente, é útil usar o perfil de um arquivo existente como a base de um novo perfil. O leitor síncrono dá suporte a **IWMProfile** da mesma maneira que o leitor.

As informações de perfil obtidas por meio do leitor ou leitor síncrono não são provenientes de um arquivo. prx. O leitor usa as informações no arquivo ASF para montar as configurações de fluxo. Assim, determinadas informações de perfil, como o nome e a descrição, não estão disponíveis por meio do leitor.

Há várias maneiras de obter um ponteiro para uma interface **IWMProfile** . O Gerenciador de perfis tem métodos para criar um novo perfil e acessar perfis existentes. Todos esses métodos definem um ponteiro **IWMProfile** . Ao ler um arquivo, um ponteiro para **IWMProfile** pode ser obtido chamando o método **QueryInterface** de qualquer interface de leitor. Da mesma forma, qualquer interface do objeto leitor síncrono pode obter um ponteiro com uma chamada para **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3).

## <a name="members"></a>Membros

A interface **IWMProfile** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMProfile** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWMProfile** tem esses métodos.



| Método                                                                  | Descrição                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Adiciona um objeto de exclusão mútua ao perfil.<br/>                                   |
| [**AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Adiciona um fluxo ao perfil.<br/>                                                    |
| [**CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Cria um objeto de exclusão mútua para o perfil.<br/>                               |
| [**CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Cria um objeto de configuração de fluxo para o perfil.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Recupera a descrição do perfil.<br/>                                        |
| [**GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Recupera um objeto de exclusão mútua do perfil.<br/>                            |
| [**GetMutualExclusionCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Recupera o número de objetos de exclusão mútua no perfil.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Recupera o nome do perfil.<br/>                                               |
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Recupera um fluxo, usando um número de índice, do perfil.<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Recupera um fluxo, usando o número do fluxo, do perfil.<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Recupera o número de fluxos no perfil.<br/>                                  |
| [**Obter versão**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Recupera o número de versão do Microsoft Windows Media Services no perfil.<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Permite que as alterações feitas em uma configuração de fluxo sejam incluídas no perfil.<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Remove um objeto de exclusão mútua do perfil.<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Remove um fluxo do perfil.<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Remove um fluxo do perfil.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Especifica a descrição do perfil.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Especifica o nome do perfil.<br/>                                               |



 

Para obter informações sobre quais interfaces podem ser obtidas usando o método QueryInterface dessa interface, consulte o tópico para o objeto no qual essa interface é implementada.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interfaces**](interfaces.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> <dt>

[**Objeto de leitor**](reader-object.md)
</dt> <dt>

[**Objeto de leitor síncrono**](synchronous-reader-object.md)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

