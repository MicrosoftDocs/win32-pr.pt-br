---
description: Quando um aplicativo executa uma operação IPropertyStorage::WriteMultiple em qualquer propriedade WIA (Aquisição de Imagem) que pode ser Windows, o driver WIA executa uma validação no novo valor da propriedade.
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Validação da propriedade WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1aca5879dbcb789b7e94a780c8fc99e53b703f6aea74498ae455e8e2ec6b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813046"
---
# <a name="wia-property-validation"></a>Validação da propriedade WIA

Quando um aplicativo executa uma [operação IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) em qualquer propriedade WIA (Aquisição de Imagem) Windows writeable, o driver WIA executa uma validação no novo valor da propriedade. Escrever uma propriedade pode ter efeitos colaterais que alteram outros valores de propriedade. O aplicativo deve ler todos os valores de propriedade após uma operação de gravação para determinar que todas as propriedades são definidas como valores que o aplicativo deseja.

Várias propriedades podem ser escritas simultaneamente usando a [operação IPropertyStorage::WriteMultiple.](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) Pode haver casos em que algumas atribuições de propriedade estão em conflito. Nesses casos, a prioridade usada para resolver conflitos é a seguinte:

1.  INTENÇÃO CUR \_ DO IPS \_ DO WIA \_
2.  WIA \_ IPA \_ DATATYPE
3.  PROFUNDIDADE DO \_ WIA IPA \_
4.  WIA \_ IPS \_ XRES
5.  WIA \_ IPS \_ YRES
6.  WIA \_ IPS \_ XPOS
7.  WIA \_ IPS \_ YPOS
8.  WIA \_ IPS \_ XEXTENT
9.  WIA \_ IPS \_ YEXTENT

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
