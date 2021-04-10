---
description: 'Quando um aplicativo executa uma operação IPropertyStorage:: WriteMultiple em qualquer propriedade de aquisição de imagem do Windows (WIA) gravável, o driver WIA executa uma validação no novo valor da propriedade.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validação da propriedade WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164517"
---
# <a name="wia-property-validation"></a>Validação da propriedade WIA

Quando um aplicativo executa uma operação [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) em qualquer propriedade de aquisição de imagem do Windows (WIA) gravável, o driver WIA executa uma validação no novo valor da propriedade. A gravação de uma propriedade pode ter efeitos colaterais que alteram outros valores de propriedade. Cabe ao aplicativo ler todos os valores de propriedade após uma operação de gravação para determinar que todas as propriedades são definidas para os valores que o aplicativo deseja.

Várias propriedades podem ser gravadas simultaneamente usando a operação [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) . Pode haver casos em que algumas atribuições de propriedade entram em conflito. Nesses casos, a prioridade usada para resolver conflitos é a seguinte:

1.  \_tentativa de \_ atual de IPS WIA \_
2.  \_tipo de \_ dados IPA WIA
3.  \_profundidade de IPA WIA \_
4.  \_XRES IPS \_ WIA
5.  \_YRES IPS \_ WIA
6.  \_XPos IPS \_ WIA
7.  \_YPos IPS \_ WIA
8.  \_XEXTENT IPS \_ WIA
9.  \_YEXTENT IPS \_ WIA

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
