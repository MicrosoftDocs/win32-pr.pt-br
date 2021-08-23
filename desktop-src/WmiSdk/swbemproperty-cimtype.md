---
description: A propriedade CIMType do objeto SWbemProperty é um inteiro que pode ser usado para determinar o tipo CIM dessa propriedade. Esta propriedade é somente para leitura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Propriedade SWbemProperty.CIMType (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f3b92cca8d17af8814a7891d0d4f97c7e003b1a999a42c63b6abe59d50e8ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991926"
---
# <a name="swbempropertycimtype-property"></a>Propriedade SWbemProperty.CIMType

A **propriedade CIMType** do [**objeto SWbemProperty**](swbemproperty.md) é um inteiro que pode ser usado para determinar o tipo CIM dessa propriedade. Esta propriedade é somente para leitura.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para obter mais informações sobre tipos válidos para essa propriedade, [**consulte WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Instâncias de objetos inseridos são armazenadas em objetos compostos como propriedades do tipo **CIM \_ OBJECT**. Para determinar a classe de um objeto inserido em uma instância de uma classe composta, você deve examinar o qualificador **CIMType** da **propriedade de tipo CIM \_ OBJECT.**

As referências de objeto em uma classe de associação são armazenadas em propriedades do tipo **CIM \_ REFERENCE**. Para determinar os caminhos de objeto reais, você deve examinar o qualificador **CIMType** da **propriedade de tipo CIM \_ REFERENCE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




