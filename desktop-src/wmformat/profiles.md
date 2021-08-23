---
title: Perfis
description: Perfis
ms.assetid: 6e70393f-3dab-4036-8d34-a672ef1795c6
keywords:
- Windows SDK do formato de mídia, perfis
- ASF (Advanced Systems Format), perfis
- ASF (formato de sistemas avançados), perfis
- Windows SDK do formato de mídia, arquivos. prx
- Formato de sistema avançado (ASF), arquivos. prx
- ASF (formato de sistemas avançados), arquivos. prx
- Windows SDK do formato de mídia, editor de perfil
- ASF (Advanced Systems Format), editor de perfil
- ASF (formato de sistemas avançados), editor de perfil
- arquivos. prx
- arquivos PRX
- Editor de perfil
- Windows Codificador de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64a89c06f031c9cf8214888efb35f2986135f88207fc94a631e1e111c94ce16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707406"
---
# <a name="profiles"></a>Perfis

Um perfil é uma coleção de dados que descreve a configuração de um arquivo ASF. No mínimo, um perfil deve conter definições de configuração para um único fluxo.

As informações de fluxo em um perfil contêm a taxa de bits, a janela de buffer e as propriedades de mídia para o fluxo. As informações de fluxo para áudio e vídeo descrevem exatamente como a mídia é configurada no arquivo, incluindo qual codec (se houver) será usado para compactar os dados.

Um perfil também contém informações sobre os vários recursos de arquivo ASF que serão usados em arquivos criados com ele. Isso inclui [exclusão mútua](mutual-exclusion.md), [priorização de fluxo](stream-prioritization.md), [compartilhamento de largura de banda](bandwidth-sharing.md)e extensões de unidade de [dados](data-unit-extensions.md).

as versões anteriores do SDK do formato de mídia do Windows forneciam perfis de sistema pré-configurados, que poderiam ser usados para criar tipos comuns de arquivos ou alterados um pouco para atender às necessidades do seu aplicativo. os perfis de sistema não têm suporte para os codecs da série Windows Media 9. Isso ocorre porque o número de tipos "comuns" de arquivos cresceu exponencialmente com a adição de novos recursos. Espera-se que praticamente todo criador de conteúdo precise que vá além das soluções simples fornecidas por perfis de sistema. Você ainda pode usar os perfis de sistema antigos como um local inicial. Para obter mais informações, consulte [usando perfis de sistema](using-system-profiles.md).

Você deve fornecer ao gravador um perfil para cada arquivo que você escrever. Você pode especificar um perfil a ser usado com o gravador chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).

os dados de perfil existem em vários formulários diferentes que podem ser usados pelo SDK do formato de mídia Windows. As informações de perfil também podem ser acessadas de várias maneiras. Isso pode levar à confusão sobre o que é um perfil e como ele é usado.

O diagrama a seguir mostra como os dados de perfil são usados no SDK.

![diagrama mostrando o fluxo de informações de perfil.](images/formatsdk01.png)

Os dados de perfil assumem três formas diferentes: dados contidos em um objeto de perfil em um aplicativo, um arquivo XML em disco e dados no cabeçalho de um arquivo ASF. Cada uma dessas formas de dados é mostrada como um retângulo sombreado no diagrama.

## <a name="data-in-a-profile-object"></a>Dados em um objeto de perfil

Ao editar um perfil, você usa um objeto de perfil, que encapsula todos os dados de perfil. Você pode criar um objeto de perfil vazio usando o objeto do Gerenciador de perfis. Você também pode usar o objeto do Gerenciador de perfis para carregar dados de perfil existentes em um objeto de perfil.

A maioria dos dados de perfil deve ser adicionada e manipulada por meio do uso de objetos que representam partes individuais do perfil. Isso inclui objetos de configuração de fluxo, objetos de exclusão mútua, objetos de compartilhamento de largura de banda e um objeto de priorização de fluxo. Cada um desses tipos de objeto pode ser criado usando métodos no objeto de perfil. Fazer alterações nesses objetos não afetará o objeto de perfil até que você use um método no objeto de perfil para incluir os dados atualizados do outro objeto.

## <a name="data-in-an-xml-file"></a>Dados em um arquivo XML

Os dados de perfil são armazenados em disco na forma de um arquivo XML com a extensão de nome de arquivo. prx. incluído com o SDK do formato de mídia Windows é uma coleção de perfis chamada perfis de sistema que abrangem os tipos mais comuns de arquivos ASF. Os perfis de sistema são armazenados em um arquivo chamado WMSysPr9. prx. (observe que esse arquivo realmente não contém perfis de sistema para Windows Media 9 Series porque o conceito de perfis de sistema não é mais usado.) Ao salvar seus próprios perfis personalizados, você deve salvá-los em seus próprios arquivos.

Você pode usar o objeto do Gerenciador de perfis para salvar os dados de um objeto de perfil em uma cadeia de caracteres de texto XML. Em seguida, você pode usar quaisquer funções de e/s de arquivo que gosta de salvar a cadeia de caracteres em um arquivo no disco.

## <a name="data-in-the-header-of-an-asf-file"></a>Dados no cabeçalho de um arquivo ASF

O gravador pega as informações do perfil e as usa para criar os fluxos que vão para a seção de dados do arquivo ASF. A massa dos dados do perfil é armazenada na seção de cabeçalho do arquivo quando um arquivo é gravado. Na reprodução, o objeto leitor (ou o objeto leitor síncrono) pode acessar as informações no cabeçalho do arquivo. Nesse caso, o objeto de leitura cria um objeto de perfil e o popula com os dados do cabeçalho.

Ao acessar os dados de perfil usando o leitor (ou leitor síncrono), você pode fazer alterações nas informações de perfil, mas não há como aplicar essas alterações ao arquivo no leitor. Você pode aplicar as informações de perfil de um arquivo em um leitor a um perfil em um gravador para criar um novo arquivo com as mesmas configurações do arquivo no leitor. Nesse caso, quaisquer alterações feitas nas informações de perfil antes de definir o perfil no gravador serão refletidas nas informações de perfil registradas pelo gravador.

## <a name="using-profile-editor"></a>Usando o editor de perfil

em vez de criar perfis usando o SDK do formato de mídia Windows, você pode usar o Editor de perfil, um utilitário incluído com o codificador de mídia Windows. No seu aplicativo de codificação, use o método **IWMProfileManager:: LoadProfileByData** para carregar o perfil salvo. Em alguns cenários, por exemplo, se você usar um número limitado de perfis que nunca são modificados dinamicamente, talvez seja mais conveniente usar o editor de perfil para criar seus perfis.

No entanto, se você usar o editor de perfil, é recomendável não usar a configuração "tamanho do vídeo: igual à entrada de vídeo". Quando essa caixa de seleção estiver marcada, o editor de perfil criará um perfil com a altura e a largura de saída do vídeo definida como zero. quando Windows o codificador de mídia encontra esses perfis, ele define os valores corretos para corresponder à entrada de vídeo. no entanto, o gravador no SDK do formato de mídia Windows não faz isso automaticamente, portanto, você deve garantir que seu aplicativo defina o tamanho do quadro de vídeo em casos em que o perfil tenha nenhum.

**Observação** Alguns itens de configuração de fluxo não são armazenados no perfil. Os dados no perfil descrevem o formato do arquivo ASF concluído. As propriedades de mídia de entrada e outros dados de configuração usados pelo objeto gravador para configurar os codecs não são salvos no perfil. Isso inclui todas as propriedades definidas usando o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto de compartilhamento de largura de banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Conceitos**](concepts.md)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Objeto de exclusão mútua**](mutual-exclusion-object.md)
</dt> <dt>

[**Objeto do gerenciador de perfis**](profile-manager-object.md)
</dt> <dt>

[**Objeto de configuração de fluxo**](stream-configuration-object.md)
</dt> <dt>

[**Objeto de priorização de fluxo**](stream-prioritization-object.md)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




