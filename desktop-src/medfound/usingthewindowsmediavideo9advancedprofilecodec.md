---
description: Usando o perfil avançado Windows Media Video 9
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Usando o perfil avançado Windows Media Video 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 258c32f14d1a7a42e1450c8265e2a611bd17b3b92b98f5433c93b91251e299c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012166"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Usando o perfil avançado Windows Media Video 9

Os procedimentos de vídeo básicos descritos na [seção Trabalhando com vídeo](workingwithvideo.md) também se aplicam diretamente ao perfil avançado Windows Media Video 9. Nenhum procedimento especial é necessário.

O perfil avançado Windows Media Video 9 está associado aos identificadores de classe CLSID \_ CWMV9EncMediaObject e CLSID \_ CWMVDecMediaObject. O valor FOURCC para tipos de mídia que usam esse codec é "WVC1".

O perfil avançado do Windows Media Video 9 dá suporte a todos os modos de codificação comuns, bem como codificação entrelaçada, codificação entrelaçada mista e progressiva, resoluções diferentes dos recursos de exibição e redução de intervalo. Outro recurso é a capacidade de armazenar metadados de sequência e quadro no próprio fluxo de bits; anteriormente, isso exigia o uso da ASF e da API de Extensões de Unidade de Dados.

As propriedades a seguir do perfil avançado Windows Media Video 9, que podem ser controladas usando as configurações do Registro, não têm cadeias de caracteres **IPropertyBag** ou **IPropertyStore** correspondentes:

-   Opção Dquant.
-   Força dquant.
-   Forçar Sobreposição.
-   Método de custo do vetor de movimento.

## <a name="achieving-optimal-visual-quality"></a>Obtendo a qualidade visual ideal

Para a maioria dos dados de vídeo, para obter a qualidade visual ideal usando o perfil avançado Windows Media Video 9, você pode definir a propriedade [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) como 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Sobre os codecs de perfil Windows mídia anterior 9

A versão atual do codec de perfil avançado do Windows Media Video 9 baseia-se no padrão SMPTE (Society of Motion Picture and Tv Engineers) para o perfil avançado vc-1 (SMPTE 421M). Esse codec substitui o codec anterior do Windows também chamado de codec de Perfil Avançado do Windows Media Video 9, que foi identificado pelo código FOURCC "WMVA". A versão anterior do codec VC-1 foi implementada antes que o padrão de perfil avançado VC-1 fosse finalizado e não tem mais suporte.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> 
<dt>

[Usando a configuração Configurações do codec de perfil avançado Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



