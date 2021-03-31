---
title: Objeto de perfil
description: Objeto de perfil
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- SDK do Windows Media Format, objetos de perfil
- ASF (Advanced Systems Format), objetos de perfil
- ASF (formato de sistemas avançados), objetos de perfil
- objetos, objetos de perfil
- perfis, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103823601"
---
# <a name="profile-object"></a>Objeto de perfil

Um objeto de perfil gerencia as configurações de um perfil. Os objetos de perfil podem ser criados para os dados de perfil existentes ou podem ser criados em branco, prontos para receber novos dados. Um objeto de perfil também é criado pelo objeto leitor (e o objeto leitor síncrono) quando um arquivo é carregado para leitura. Nesse caso, o objeto é populado com as informações de perfil armazenadas no cabeçalho do arquivo.

Para salvar o conteúdo de um objeto de perfil, você deve chamar [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).

Um perfil contém vários objetos que controlam vários aspectos do perfil (como fluxos). Todos esses objetos são subordinados ao objeto de perfil. Você não cria esses objetos com funções de criação como faria com os objetos principais desse SDK. Em vez disso, as interfaces do objeto de perfil contêm métodos que criam os objetos subordinados.

Para criar um objeto de perfil, chame um dos métodos a seguir.



| Método                                                                                | Descrição                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | Cria um objeto de perfil sem nenhum dado de perfil.                                                                                                              |
| [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | Cria um objeto de perfil populado com dados de um perfil salvo como uma cadeia de caracteres. Essa é a única maneira de criar um objeto de perfil com dados de um perfil personalizado. |
| [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | Cria um objeto de perfil populado com dados de um perfil do sistema. Usa o GUID para identificar o perfil do sistema desejado.                                       |
| [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | Cria um objeto de perfil populado com dados de um perfil do sistema. Usa o índice de perfil para identificar o perfil do sistema desejado.                              |



 

Todos os métodos na tabela anterior definiram um ponteiro para uma interface **IWMProfile** . As outras interfaces do objeto de perfil podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir têm suporte em todos os objetos de perfil.



| Interface                                  | Descrição                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | Gerencia uma lista de idiomas com suporte por um arquivo ASF.                                                                                             |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | Controla o tamanho máximo de pacotes em um arquivo.                                                                                                   |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | Controla o tamanho mínimo dos pacotes em um arquivo. Herda todos os métodos de **IWMPacketSize**.                                                 |
| [**IWMProfile**](iwmprofile.md)           | Controla as configurações básicas e os objetos incluídos em um perfil.                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | Recupera o GUID (identificador global exclusivo) associado ao perfil. Herda todos os métodos de **IWMProfile**.                       |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | Controla o compartilhamento de largura de banda e as informações de priorização de fluxo em um perfil. Herda todos os métodos de **IWMProfile** e **IWMProfile2**. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> <dt>

[**Perfis**](profiles.md)
</dt> </dl>

 

 




