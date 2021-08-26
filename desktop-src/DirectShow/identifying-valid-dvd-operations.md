---
description: Identificando operações de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificando operações de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd1b99a38949ca0ff54d391e9ad5458bbe854a5c4af4140b15deaf4177147aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051976"
---
# <a name="identifying-valid-dvd-operations"></a>Identificando operações de DVD válidas

Vários fatores determinam se você pode executar uma determinada operação de DVD:

-   O domínio atual. Alguns comandos só são válidos em determinados domínios. Quando o domínio é alterado, o navegador envia um evento EC \_ DVD \_ DOMAIN \_ CHANGE. Você também pode chamar [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obter o domínio atual.
-   Sinalizadores UOPS. Esses são sinalizadores gravados no disco que indicam quais operações são permitidas. Sempre que os sinalizadores mudarem, o navegador enviará um evento UOPS CHANGE VÁLIDO de DVD de EC \_ \_ com os novos \_ \_ sinalizadores. Você também pode chamar [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) para obter os sinalizadores UOPS atuais.
-   Conteúdo do DVD. Alguns comandos podem não ser relevantes com base no conteúdo do DVD. Por exemplo, o [**método IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) pode ser permitido de acordo com o domínio atual e os sinalizadores UOPS, mas o vídeo pode ter apenas um ângulo. Nesse caso, a **chamada SelectAngle** é permitida, mas não é uma opção significativa.

Em caso de dúvida, permita uma ação. Na pior das hipóteses, [**o método IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) falhará e você poderá fazer comentários ao usuário. Os comentários devem ser relativamente discretos. Por exemplo, você pode piscar um pequeno X vermelho para alertar o usuário. O Navegador de DVD retorna INVALIDDOMAIN de VFW E DVD quando o domínio proíbe uma operação e a \_ OPERAÇÃO DE DVD DO \_ \_ VFW E FOI INOCedida quando os sinalizadores de UOPS proíbem \_ \_ uma \_ \_ operação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



