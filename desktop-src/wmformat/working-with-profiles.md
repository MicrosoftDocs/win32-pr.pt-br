---
title: Trabalhando com perfis
description: Trabalhando com perfis
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows SDK de Formato de Mídia, perfis
- Windows SDK de Formato de Mídia, interface IWMCodecInfo3
- perfis, sobre
- profiles,Windows SDK de Formato de Mídia
- profiles,IWMCodecInfo3
- IWMCodecInfo3, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68982a47b743aaa12397e937ad9bd213fbd7ac0a78b41087d01929c1d42bb622
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055426"
---
# <a name="working-with-profiles"></a>Trabalhando com perfis

Esta seção descreve como projetar, criar e modificar perfis. Cada perfil descreve os fluxos que comão um arquivo e suas relações entre si. Um objeto de perfil contém informações de configuração de fluxo para cada fluxo, informações de exclusão mútua para fluxos que não podem ser entregues simultaneamente, informações de compartilhamento de largura de banda e informações de priorização de fluxo.

A principal finalidade dos perfis é fornecer informações de configuração de fluxo para o objeto de autor. O autor usa as informações em um perfil para coordenar com os codecs o processo de compactação de entradas. Ao configurar um fluxo de mídia compactado, você especifica o codec usado para compactar os dados e as configurações que o codec usa. Você também pode criar perfis para fluxos descompactados. Há suporte para vários tipos de fluxo descompactados. Embora eles não exigem um codec, esses tipos têm seus próprios requisitos para a configuração de fluxo. Para obter mais informações, [consulte Configuring Fluxos](configuring-streams.md) [and Using Uncompressed Audio and Video Fluxos](using-uncompressed-audio-and-video-streams.md).

As informações de configuração de fluxo para um fluxo usando um dos codecs Windows Media devem ser obtidas do codec usando os métodos da interface [**IWMCodecInfo3.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) O procedimento para usar formatos de fluxo é diferente para codecs de vídeo do que para codecs de áudio, mas em ambos os casos, você deve começar obtendo o formato do codec. Você nunca deve tentar configurar manualmente um fluxo usando um dos codecs Windows Media, pois pequenos erros no perfil podem ter um efeito profundo no arquivo ASF.

As etapas básicas na criação e/ou modificação de perfis são:

1.  Crie um perfil vazio ou carregue um perfil existente para editar.
2.  Configure cada um dos fluxos, se necessário, com base nos dados de perfil com suporte recuperados do codec que será usado para codificar o fluxo.
3.  Configure a exclusão mútua, se necessário.
4.  Configure o compartilhamento de largura de banda, se necessário.
5.  De definir a prioridade dos fluxos no arquivo, se necessário.

As seções a seguir explicam o processo de criação e edição de perfis.



| Seção                                                        | Descrição                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Projetando perfis](designing-profiles.md)                   | Descreve como criar um perfil.                                                                 |
| [Criando perfis](creating-profiles.md)                     | Descreve como criar um perfil vazio.                                                          |
| [Configurando Fluxos](configuring-streams.md)                 | Descreve como configurar fluxos e incluí-los em um perfil.                                  |
| [Usando a exclusão mútua](using-mutual-exclusion.md)           | Descreve como criar objetos de exclusão mútua e incluí-los em um perfil.                    |
| [Usando o compartilhamento de largura de banda](using-bandwidth-sharing.md)         | Descreve como usar o compartilhamento de largura de banda em um perfil.                                               |
| [Usando a priorização de fluxo](using-stream-prioritization.md) | Descreve como usar a priorização de fluxo em um perfil.                                           |
| [Salvando perfis](saving-profiles.md)                         | Descreve como salvar seus perfis personalizados em um arquivo.                                              |
| [Usando perfis do sistema](using-system-profiles.md)             | Descreve como trabalhar com perfis de sistema para economizar tempo e esforço na criação de perfis.           |
| [Gerenciamento do tamanho do pacote](managing-packet-size.md)               | Discute como controlar o tamanho dos pacotes nos fluxos de dados de arquivos feitos usando seu perfil. |



 

**Observação** Os usuários de versões anteriores do SDK Windows Formato de Mídia podem estar acostumados a usar perfis do sistema sem modificação para criar seus arquivos. O SDK Windows Media Format 9 series ou posterior não inclui nenhum novo perfil de sistema que use o Windows Media 9 Series ou codecs posteriores. Isso se deve ao número crescente de perfis que seriam necessários para cobrir os vários recursos agora oferecidos pelos codecs. Você ainda pode usar os perfis do sistema versão 8 como um ponto de partida para seus perfis. Para obter mais informações, [consulte Usando perfis do sistema](using-system-profiles.md). Para obter informações sobre o novo mecanismo de direcionamento de perfis para dispositivos de entrega específicos, consulte [Trabalhando com modelos de conformidade do dispositivo.](working-with-device-conformance-templates.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




