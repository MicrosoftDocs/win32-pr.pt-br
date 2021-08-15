---
title: Produzindo uma caixa de diálogo para selecionar formatos restritos
description: Produzindo uma caixa de diálogo para selecionar formatos restritos
ms.assetid: 486ba928-e06d-4ab0-a642-ba0fe16c8291
keywords:
- Gerenciador de compactação de áudio (ACM), produzindo caixas de diálogo
- ACM (Gerenciador de compactação de áudio), caixas de diálogo em produção
- Exemplos do ACM, caixas de diálogo de produção
- produzindo caixas de diálogo
- função acmFormatChoose
- Gerenciador de compactação de áudio (ACM), selecionando formatos restritos
- ACM (Gerenciador de compactação de áudio), selecionando formatos restritos
- Exemplos do ACM, seleção de formatos restritos
- selecionando formatos restritos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994fffa7ef13f6febe41eb766b4ecaef7eb735f11f58d36f37adfccbb152bffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802036"
---
# <a name="producing-a-dialog-box-for-selecting-restricted-formats"></a>Produzindo uma caixa de diálogo para selecionar formatos restritos

Talvez você queira usar a caixa de diálogo criada pela função [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , mas limitar ou controlar os formatos na caixa de diálogo. Você pode fazer isso usando o sinalizador ACMFORMATCHOOSE \_ STYLEF \_ ENABLEHOOK para conectar o procedimento da caixa de diálogo. O aplicativo pode, então, filtrar os formatos respondendo à mensagem [**mm \_ ACM \_ FORMATCHOOSE**](mm-acm-formatchoose.md) no procedimento de mensagem da caixa de diálogo.

 

 




