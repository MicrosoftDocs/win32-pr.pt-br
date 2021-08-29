---
title: Produzindo uma caixa de diálogo para selecionar um formato para salvar
description: Produzindo uma caixa de diálogo para selecionar um formato para salvar
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (gerenciador de compactação de áudio), produzindo caixas de diálogo
- Exemplos do ACM, produzindo caixas de diálogo
- produzindo caixas de diálogo
- Função acmFormatChoose
- gerenciador de compactação de áudio (ACM), selecionando o formato para salvar
- ACM (gerenciador de compactação de áudio), selecionando o formato para salvar
- Exemplos do ACM, selecionando o formato para salvar
- selecionando o formato para salvar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65288e4a15712ec86bcf48a8f8088da9f6d5944f298119b21766be238168bf3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805772"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a>Produzindo uma caixa de diálogo para selecionar um formato para salvar

Talvez você queira que um aplicativo salve dados de áudio de forma de onda existentes em outro formato. Por exemplo, um editor waveform-audio pode salvar um arquivo waveform-audio como um arquivo compactado. Para listar apenas os formatos de destino sugeridos para um formato de origem especificado na caixa de diálogo criada pela [**função acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) especifique o formato de origem no membro **pwfxEnum** e o sinalizador SUGGEST ACM FORMATENUMF no membro \_ \_ **fdwEnum** da estrutura [**ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)

Da mesma forma, para listar formatos de destino válidos para um formato especificado, use o sinalizador CONVERT ACM FORMATENUMF em vez do sinalizador \_ \_ ACM \_ FORMATENUMF \_ SUGGEST.

 

 




