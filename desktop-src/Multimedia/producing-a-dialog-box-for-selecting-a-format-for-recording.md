---
title: Produzindo uma caixa de diálogo para selecionar um formato para gravação
description: Produzindo uma caixa de diálogo para selecionar um formato para gravação
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (gerenciador de compactação de áudio), produzindo caixas de diálogo
- Exemplos do ACM, produzindo caixas de diálogo
- produzindo caixas de diálogo
- Função acmFormatChoose
- gerenciador de compactação de áudio (ACM), selecionando o formato para recodificação
- ACM (gerenciador de compactação de áudio), selecionando o formato para recodificação
- Exemplos do ACM, selecionando o formato para recodificação
- selecionando o formato para recodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4650732e290b626eb26cd2eea321124f16b5572a7660aabf09bbe3740934e52d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037676"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Produzindo uma caixa de diálogo para selecionar um formato para gravação

Um aplicativo pode permitir que o usuário selecione um formato para o qual um dispositivo waveform-audio instalado fornece suporte nativo. Por exemplo, talvez você queira que um editor waveform-audio grave novos dados waveform-audio sem usar um descompactador ou um descompactador do ACM para fornecer uma camada de tradução. Para fazer isso, use [**a função acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) especificando os sinalizadores \_ ACM FORMATENUMF HARDWARE e \_ ACM \_ FORMATENUMF INPUT no membro \_ **fdwEnum** da estrutura [**ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)

 

 




