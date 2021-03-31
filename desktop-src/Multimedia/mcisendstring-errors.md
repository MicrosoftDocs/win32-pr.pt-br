---
title: Erros de mciSendString
description: Erros de mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- MCIERR valores de retorno, erros de mciSendString
- referência de multimídia, erros de mciSendString
- referência para multimídia, erros de mciSendString
- MCI (interface de controle de mídia), erros de mciSendString
- MCI (interface de controle de mídia), erros de mciSendString
- referência para MCI, erros de mciSendString
- Referência de MCI, erros de mciSendString
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- erros de mciSendString
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823729"
---
# <a name="mcisendstring-errors"></a>Erros de mciSendString

Os erros a seguir são retornados pela função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) , mas não por [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):



| Valor                             | Significado                                           |
|-----------------------------------|---------------------------------------------------|
| \_constante MCIERR inadequada \_             | O valor especificado para um parâmetro é desconhecido.   |
| MCIERR \_ inteiro inválido \_              | Um inteiro no comando era inválido ou estava ausente. |
| MCIERR \_ sinalizadores duplicados \_          | Um sinalizador ou valor foi especificado duas vezes.              |
| MCIERR \_ \_ cadeia de caracteres de comando ausente \_  | Nenhum comando foi especificado.                         |
| MCIERR \_ \_ nome do dispositivo ausente \_     | Nenhum nome de dispositivo foi especificado.                     |
| MCIERR \_ \_ argumento de cadeia de caracteres ausente \_ | Um valor de cadeia de caracteres estava ausente no comando.      |
| MCIERR \_ New \_ requer \_ alias      | Um alias deve ser usado com o nome do dispositivo "novo". |
| MCIERR \_ sem \_ aspas de fechamento \_        | Está faltando um sinal de aspas de fechamento.              |
| MCIERR \_ notificar \_ ao \_ \_ abrir automaticamente    | O sinalizador "Notify" é inválido com a abertura automática.      |
| \_estouro de param MCIERR \_           | A cadeia de caracteres de saída não era longa o suficiente.            |
| MCIERR do \_ analisador \_ interno          | Ocorreu um erro interno do analisador.                |
| MCIERR \_ \_ palavra-chave não reconhecida     | Um parâmetro de comando desconhecido foi especificado.       |



 

 

 