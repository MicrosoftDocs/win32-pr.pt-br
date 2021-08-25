---
description: Inicializando o objeto ContentInfo de um novo arquivo ASF
ms.assetid: a4f6c90e-1b38-4c70-8bc5-e2e16af3d87a
title: Inicializando o objeto ContentInfo de um novo arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf0180eb4e9369447355a9a4cd607f630bfb3664108ad77d6d008c281f92fdf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114246"
---
# <a name="initializing-the-contentinfo-object-of-a-new-asf-file"></a>Inicializando o objeto ContentInfo de um novo arquivo ASF

Depois de criar um objeto ContentInfo vazio chamando a função [**MFCreateASFContentInfo,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) o aplicativo deve chamar [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para fornecer o perfil de codificação. Para obter informações sobre como criar um perfil, consulte [Criando um perfil ASF](creating-an-asf-profile.md).

Antes que as informações possam ser lidas do perfil, o método **SetProfile** deve validar o objeto de perfil especificado verificando os identificadores de fluxo ou tipos de mídia. Se o perfil passar na validação, vários objetos de header serão gerados, como o Objeto de Propriedades do Arquivo, o Objeto propriedades de taxa de bits de fluxo, o objeto Propriedades do Fluxo e o Objeto de Exclusão Mútua.

**SetProfile** calcula e define valores recomendados para determinadas propriedades, como o valor de pré-roll. Se isso ainda não estiver definido, o valor de pré-roll recomendado em milissegundos dependerá da janela de buffer máxima do bucket de vazamento especificado para os fluxos no perfil. Da mesma forma, os tamanhos mínimo e máximo de pacotes de dados também são definidos. Os valores recomendados podem substituir os tamanhos de pacotes definidos no perfil por meio de atributos.

Como o arquivo está no processo de criação, o arquivo é categorizado como um tipo de difusão, que é anotado pelo campo Sinalizadores do Objeto de Propriedades do Arquivo. Determinados valores desconhecidos, como o número de pacotes de dados, a duração da reprodução e a duração do envio são definidos como zero. Esses valores são representados por atributos **\_ MF PD \_ ASF \_ xxx** e devem ser atualizados pelo aplicativo após a conclusão da criação do arquivo.

O objeto de perfil especificado substitui qualquer perfil existente associado ao objeto ContentInfo, remove os objetos de título referenciados e redefine as propriedades globais do arquivo, como pré-registro e tamanho do pacote de dados.

O **método SetProfile** também cria o objeto de dados que representa o objeto de dados ASF. Se você reutilizar um objeto ContentInfo que inclui informações sobre pacotes de dados, **SetProfile** falhará e retornará o erro MF E ALREADY INITIALIZED indicando que ele já está associado a um objeto de dados \_ \_ \_ ASF existente. Por padrão, para um novo objeto ContentInfo, a contagem de pacotes de dados é definida como zero e o tamanho do objeto de dados é definido como 50 bytes. Se você usar o multiplexador para gerar pacotes de dados, o multiplexador atualizará o objeto ContentInfo para refletir novos valores, como a contagem de pacotes de dados. Para obter mais informações sobre a geração de pacotes de dados, [consulte Gerando novos pacotes de](generating-new-asf-data-packets.md)dados ASF .

Depois que todos os Objetos de Header são adicionados ao Objeto de Header ASF final, o tamanho total do header pode ser recuperado chamando [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize). Esse tamanho inclui o tamanho do objeto de dados inicial.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md)
</dt> <dt>

[Escrevendo um objeto de header ASF para um novo arquivo](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 



