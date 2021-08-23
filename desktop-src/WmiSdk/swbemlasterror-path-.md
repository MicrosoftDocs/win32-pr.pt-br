---
description: A propriedade Path \_ do objeto SWbemLastError retorna um objeto SWbemObjectPath que representa o caminho do objeto da classe ou instância atual. Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_ propriedade (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5503d11d5c73f2bf955b25da9b5dbccbc18d41b9bc9b84bc3235993562938b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612196"
---
# <a name="swbemlasterrorpath_-property"></a>Propriedade SWbemLastError.Path \_

A **\_ propriedade Path** do [**objeto SWbemLastError**](swbemlasterror.md) retorna um [**objeto SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual. Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Somente a [**propriedade Class**](swbemobjectpath-class.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada pode ser modificada. Se você tentar modificar qualquer outra propriedade ou tentar chamar os métodos [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingread,**](swbemobjectpath-setassingleton.md) obterá um erro de **wbemErrReadOnly.**

Por isso, você não pode modificar o objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é o valor da propriedade [**Keys**](swbemobjectpath-keys.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada. Se você tentar chamar os métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) nesse valor, obterá um erro **wbemErrReadOnly.** Além disso, você não pode modificar [**nenhum SWbemNamedValue**](swbemnamedvalue.md) obtido desta coleção. As tentativas de modificar [**a propriedade Value**](swbemnamedvalue-value.md) retornam o mesmo código de erro.

No entanto, se você chamar [**SWbemObject.Clone \_**](swbemobject-clone-.md) para criar uma cópia, a propriedade [**Path \_**](swbemobject-path-.md) da cópia será totalmente modificável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLastError<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemLastError<br/>                                                         |



 

 




