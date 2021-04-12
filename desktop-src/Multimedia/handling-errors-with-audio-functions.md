---
title: Tratamento de erros com funções de áudio
description: Tratamento de erros com funções de áudio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- áudio de multimídia, erros de áudio de onda
- áudio, erros de áudio de onda
- áudio de multimídia, erros auxiliares de áudio
- áudio, erros auxiliares de áudio
- áudio de onda, erros
- áudio auxiliar, erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293943"
---
# <a name="handling-errors-with-audio-functions"></a>Tratamento de erros com funções de áudio

As funções Wave-audio e auxiliar-Audio retornam um valor diferente de zero quando ocorre um erro. O Windows fornece funções que convertem esses valores de erro em descrições textuais dos erros. O aplicativo ainda deve examinar os valores de erro para determinar como proceder, mas descrições textuais de erros podem ser usadas em caixas de diálogo que descrevem erros para os usuários.

Você pode usar as seguintes funções para recuperar descrições textuais de valores de erro de áudio:



| Função                                           | Descrição                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Recupera uma descrição textual de um erro de entrada de wave-áudio especificado.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Recupera uma descrição textual de um erro de saída de wave-áudio especificado. |



 

As únicas funções de áudio que não retornam valores de erro são [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)e [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs). Essas funções retornarão zero se nenhum dispositivo estiver presente em um sistema ou se encontrar erros.

 

 