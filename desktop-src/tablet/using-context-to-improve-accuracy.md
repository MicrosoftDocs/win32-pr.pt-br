---
description: Um mecanismo de reconhecimento de manuscrito, ou reconhecedor, é um software que processa a tinta e converte essa tinta em texto.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Usando o contexto para melhorar a precisão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769143"
---
# <a name="using-context-to-improve-accuracy"></a>Usando o contexto para melhorar a precisão

Um mecanismo de reconhecimento de manuscrito, ou reconhecedor, é um software que processa a tinta e converte essa tinta em texto. Um contexto é relevante, informações específicas do aplicativo que você fornece a um reconhecedor para melhorar a precisão do reconhecimento. Em outras palavras, o contexto é qualquer informação sobre entrada que ajude o reconhecedor a processar com precisão a tinta em um campo.

Esta seção descreve as diferentes maneiras pelas quais você pode aproveitar o contexto em seu aplicativo do Tablet PC, dando ênfase à técnica de programação preferida para aplicativos que não estão habilitados para tinta.

> [!Note]  
> Há locais nas seções de tecnologia do Tablet PC do SDK (Software Development Kit) do Windows Vista, em que o termo "contexto" é usado em relação ao objeto [**RecognizerContext**](inkrecognizercontext-class.md) e suas propriedades [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) e [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) . Não confunda esses outros usos de "contexto" com a definição nesta seção.

 

 

 



