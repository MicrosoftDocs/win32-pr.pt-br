---
title: Signature_Name
description: O atributo \_ Nome da Assinatura contém o nome no certificado usado para assinar o arquivo. Esse atributo só será válido se o atributo For \_ Confiável estiver definido como True.
ms.assetid: 3f3ab10c-731b-4075-8f73-3c2e62e010b9
keywords:
- Signature_Name formato de mídia do Windows
topic_type:
- apiref
api_name:
- Signature_Name
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bff0516353468733ef5c834d51dddc7bbc85e322d98b82929e092913bc375a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845847"
---
# <a name="signature_name"></a>Nome da \_ Assinatura

O **atributo \_ Nome** da Assinatura contém o nome no certificado usado para assinar o arquivo. Esse atributo só será válido se o [**atributo For \_ Confiável**](is-trusted.md) estiver definido como True.

## <a name="global-constant"></a>Constante global

g \_ wszWMSignature \_ Name

## <a name="data-type"></a>Tipo de Dados

**CADEIA DE CARACTERES DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

Esse é um atributo codificado.

Esse atributo não pode ser duplicado no nível do arquivo. Se esse atributo for usado para um fluxo individual, ele será tratado como metadados personalizados e não transmitirá seu significado normal para os objetos do SDK Windows Formato de Mídia.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




