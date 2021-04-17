---
description: O Windows Imaging Component (WIC) simplifica o gerenciamento de cores, fornecendo a interface IWICColorContext e a interface IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Visão geral do gerenciamento de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1552375ee896173ba8d1fdbf4a9ae19c2af6e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782526"
---
# <a name="color-management-overview"></a>Visão geral do gerenciamento de cores

As imagens digitais são originadas de e são destinadas a uma variedade de dispositivos, cada um dos quais tem sua própria gama e intervalo dinâmico. Se um fotógrafo fosse capturar a mesma cena em duas câmeras diferentes, as cores nas imagens resultantes não apareceriam exatamente iguais, mesmo quando processadas no mesmo dispositivo de saída porque os recursos de gama de cores dos dois dispositivos de origem eram diferentes. Da mesma forma, a mesma imagem renderizada em dois dispositivos de destino diferentes aparecerá de forma diferente porque os dispositivos de destino têm perfis de cores diferentes. Para garantir a reprodução de cores consistente entre os dispositivos, é necessário criar um mapeamento do perfil de cor do dispositivo de origem para o perfil de cor do dispositivo de destino. O gerenciamento de cores procura produzir uma correspondência visual mais próxima e consistente e é um recurso crítico em imagens profissionais.

Ser capaz de reproduzir de forma consistente a cor entre scanners, monitores, impressoras e aplicativos parece uma meta simples, mas sem um sistema de gerenciamento de cores no sistema operacional, é difícil alcançar. Se cada aplicativo for necessário para gerar seus próprios perfis de cor, será quase impossível alcançar um intercâmbio de cores consistente ao longo do processo de publicação, que inclui verificação, edição e composição, verificação e distribuição.

O Windows Imaging Component (WIC) simplifica o gerenciamento de cores, fornecendo a interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e a interface [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) . Você pode obter um objeto [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) usando [**IWICFactory:: CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer). O [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) é uma abstração para o perfil de cor do dispositivo. **IWICColorContext** é inicializado com um quadro de bitmap, o perfil de cor do dispositivo de origem e o perfil de cor do dispositivo de destino. Ele executa a conversão do quadro de bitmap.

 

 



