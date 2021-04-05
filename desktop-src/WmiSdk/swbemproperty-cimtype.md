---
description: A propriedade CIMType do objeto SWbemProperty é um inteiro que pode ser usado para determinar o tipo CIM dessa propriedade. Esta propriedade é somente para leitura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Propriedade SWbemProperty. CIMType (Wbemdisp. h)
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
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921885"
---
# <a name="swbempropertycimtype-property"></a>Propriedade SWbemProperty. CIMType

A propriedade **CIMType** do objeto [**SWbemProperty**](swbemproperty.md) é um inteiro que pode ser usado para determinar o tipo CIM dessa propriedade. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para obter mais informações sobre tipos válidos para essa propriedade, consulte [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

As instâncias de objetos inseridos são armazenadas em objetos compostos como propriedades do tipo **\_ objeto CIM**. Para determinar a classe de um objeto incorporado em uma instância de uma classe composta, você deve examinar o qualificador **CIMType** da propriedade tipo de **\_ objeto CIM** .

As referências de objeto em uma classe de associação são armazenadas em Propriedades do tipo **\_ referência de CIM**. Para determinar os caminhos de objeto reais, você deve examinar o qualificador **CIMType** da Propriedade do tipo de **\_ referência CIM** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | ISWbemProperty de IID \_<br/>                                                          |



 

 




