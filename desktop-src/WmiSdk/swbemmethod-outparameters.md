---
description: A propriedade Parameters do objeto SWbemMethod é um objeto SWbemObject cujas propriedades definem os parâmetros de saída e o tipo de retorno desse método. Esta propriedade é somente para leitura.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Propriedade SWbemMethod. Parameters (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2087dd545a37cdc4b82899cb261cfef5fdb1fda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105790538"
---
# <a name="swbemmethodoutparameters-property"></a>Propriedade SWbemMethod. Parameters

A propriedade **Parameters** do objeto [**SWbemMethod**](swbemmethod.md) é um objeto [**SWbemObject**](swbemobject.md) cujas propriedades definem os parâmetros de saída e o tipo de retorno desse método. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como usar essa propriedade para obter parâmetros de saída de métodos de provedor, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Observe que qualquer alteração feita nesse objeto não é refletida na definição do método subjacente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMMETHOD CLSID<br/>                                                           |
| IID<br/>                      | ISWbemMethod de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




