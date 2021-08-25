---
description: Windows O WIC (Componente de Imagens) simplifica o gerenciamento de cores fornecendo a interface IWICColorContext e a interface IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Visão geral do gerenciamento de cores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a8c30074210a0a061fcbd26b05054591d2023805bfdff0848f0d7054dfe07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090037"
---
# <a name="color-management-overview"></a>Visão geral do gerenciamento de cores

As imagens digitais são originadas de e são direcionadas a uma variedade de dispositivos, cada um deles com sua própria gama e intervalo dinâmico. Se um profissional fosse capturar a mesma cena em duas câmeras diferentes, as cores nas imagens resultantes não apareceriam exatamente iguais, mesmo quando renderizadas no mesmo dispositivo de saída porque as funcionalidades de gama de cores dos dois dispositivos de origem eram diferentes. Da mesma forma, a mesma imagem renderizada em dois dispositivos de destino diferentes aparecerá de forma diferente porque os dispositivos de destino têm perfis de cores diferentes. Para garantir a reprodução de cores consistente entre dispositivos, é necessário criar um mapeamento do perfil de cor do dispositivo de origem para o perfil de cor do dispositivo de destino. O gerenciamento de cores busca produzir uma combinação visual próxima e consistente e é um recurso crítico em imagens profissionais.

Ser capaz de reproduzir cores consistentemente entre scanners, monitores, impressoras e aplicativos parece uma meta simples, mas sem um sistema de gerenciamento de cores no sistema operacional, é difícil alcançar. Se cada aplicativo for necessário para gerar seus próprios perfis de cor, será quase impossível obter um intercâmbio de cores consistente em todo o processo de publicação, o que inclui verificação, edição e composição, verificação e distribuição.

Windows O WIC (Componente de Imagens) simplifica o gerenciamento de cores fornecendo a interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) e a interface [**IWICColorTransform.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) Você pode obter um [**objeto IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) usando [**O IWICFactory::CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer). O [**IWICColorContext é**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) uma abstração para o perfil de cor do dispositivo. **IWICColorContext** é inicializado com um quadro de bitmap, o perfil de cor do dispositivo de origem e o perfil de cor do dispositivo de destino. Ele executa a conversão do quadro de bitmap.

 

 



