---
description: A tabela a seguir descreve em quais threads os eventos de objeto RecognizerContext podem ser ativas. EventThreadsRecognitionFires no thread de reconhecimento em segundo plano ou no thread que chama o método Recognize do objeto RecognizerContext. RecognitionWithAlternatesFires no thread de reconhecimento em segundo plano.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventos de objeto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c8fa7aad4e7c6ba0dde2b38db4b82437b0732dda565aed8cc42750a339b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091436"
---
# <a name="recognizercontext-object-events"></a>Eventos de objeto RecognizerContext

A tabela a seguir descreve em quais threads os [**eventos de objeto RecognizerContext**](inkrecognizercontext-class.md) podem ser ativas.



| Evento                                                                               | Threads                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reconhecimento**](inkrecognizercontext-recognition.md)                             | Dispara no thread de reconhecimento em segundo plano ou no thread que chama o método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) do objeto [**RecognizerContext.**](inkrecognizercontext-class.md)<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Ativas no thread de reconhecimento em segundo plano.<br/>                                                                                                                                                               |



 

 

 




