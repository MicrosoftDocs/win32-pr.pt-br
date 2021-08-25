---
description: Cada localidade tem um tipo de calendário padrão (tipo de dados CALTYPE) associado a ele. Uma localidade também pode ter um tipo de calendário alternativo. Para obter detalhes sobre os tipos de calendário, consulte informações de tipo de calendário.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Data e calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f200ccd60a5a5d121a8774c01808794e744b98d8611210fcc98b0f8e5e1f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822806"
---
# <a name="date-and-calendar"></a>Data e calendário

Cada [localidade](locales-and-languages.md) tem um tipo de calendário padrão (tipo de dados CALTYPE) associado a ele. Uma localidade também pode ter um tipo de calendário alternativo. Para obter detalhes sobre os tipos de calendário, consulte [informações de tipo de calendário](calendar-type-information.md).

> [!Note]  
> Para usar um tipo de calendário alternativo para uma localidade, seu aplicativo deve definir a constante [ \_ IOPTIONALCALENDAR de localidade](locale-ioptionalcalendar.md) como o tipo de calendário alternativo para a localidade.

 

A maioria das localidades usa o calendário gregoriano padrão e um número definido de formatos de data. Essas opções padrão para formatos de data estão disponíveis para exibição usando a função [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) ou [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .

Algumas localidades exigem considerações especiais ao criar uma lista completa de opções de formato. Algumas dessas localidades exigem que as cadeias de texto sejam inseridas na cadeia de caracteres de formato de data, enquanto outras exigem um método completamente diferente de computação dos valores. Um aplicativo resolve esses requisitos especiais pela adição de determinados tipos de informações de localidade e tipos de calendário.

Para obter detalhes sobre como implementar datas e calendários em seus aplicativos, consulte [recuperando informações de data e hora](retrieving-time-and-date-information.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o suporte ao idioma nacional](about-national-language-support.md)
</dt> <dt>

[Informações de tipo de calendário](calendar-type-information.md)
</dt> <dt>

[Recuperando informações de data e hora](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



