---
description: Usando o perfil do Windows Media Video 9 avançado
ms.assetid: 2abc0efc-dd11-4921-897c-209a26f8ba1d
title: Usando o perfil do Windows Media Video 9 avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692243117cde3b4b5f1179c5f7324d25842191b6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105784181"
---
# <a name="using-the-windows-media-video-9-advanced-profile"></a>Usando o perfil do Windows Media Video 9 avançado

Os procedimentos básicos de vídeo descritos na seção [trabalhando com vídeo](workingwithvideo.md) também se aplicam diretamente ao perfil do Windows Media Video 9 avançado. Nenhum procedimento especial é necessário.

O perfil do Windows Media Video 9 avançado está associado aos identificadores de classe CLSID \_ CWMV9EncMediaObject e CLSID \_ CWMVDecMediaObject. O valor FOURCC para os tipos de mídia usando esse codec é "WVC1".

O perfil Windows Media Video 9 avançado dá suporte a todos os modos de codificação comuns, bem como codificação entrelaçada, codificação entrelaçada mista e progressiva, resoluções que são diferentes dos recursos de exibição e redução de intervalo. Outro recurso é a capacidade de armazenar metadados de sequência e de quadro no próprio fluxo de bits; anteriormente, isso tinha exigido o uso do ASF e da API de extensões de unidade de dados.

As propriedades a seguir do perfil avançado do Windows Media Video 9, que podem ser controladas usando as configurações do registro, não têm as cadeias de caracteres **IPropertyBag** ou **IPropertyStore** correspondentes:

-   Opção Dquant.
-   Intensidade de Dquant.
-   Forçar sobreposição.
-   Método de custo de vetor de movimento.

## <a name="achieving-optimal-visual-quality"></a>Obtendo qualidade visual ideal

Para a maioria dos dados de vídeo, para obter a qualidade visual ideal usando o perfil do Windows Media Video 9 avançado, você pode definir a propriedade [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) como 1.

## <a name="about-the-previous-windows-media-video-9-advanced-profile-codecs"></a>Sobre os codecs de perfil avançado do Windows Media monitor 9 Advanced

A versão atual do codec de perfil avançado do Windows Media Video 9 é baseada no perfil da sociedade de imagem do Motion (421M) para VC-1 (SMPTE) (padrão de engenharia de vídeo) e avançado. Esse codec substitui o codec anterior do Windows também chamado de codec de perfil avançado do Windows Media Video 9, que foi identificado pelo código FOURCC "WMVA". A versão anterior do codec VC-1 foi implementada antes de o padrão de perfil avançado VC-1 ter sido finalizado e não é mais suportado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> 
<dt>

[Usando as configurações avançadas do codec de perfil avançado do Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)
</dt> </dl>

 

 



