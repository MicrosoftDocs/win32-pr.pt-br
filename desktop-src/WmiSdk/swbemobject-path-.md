---
description: A \_ propriedade Path do objeto SWbemObject retorna um objeto SWbemObjectPath que representa o caminho do objeto da classe ou instância atual. Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Path_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170190"
---
# <a name="swbemobjectpath_-property"></a>Propriedade SWbemObject. Path \_

A **propriedade \_ Path** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual. Essa propriedade pode ser passada como um parâmetro para métodos que exigem um caminho de objeto.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Somente a propriedade [**Class**](swbemobjectpath-class.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada pode ser modificada. Se você tentar modificar qualquer outra propriedade ou tentar chamar os métodos [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingleton**](swbemobjectpath-setassingleton.md), receberá um erro **wbemErrReadOnly** .

Por isso, você não pode modificar o objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que é o valor da propriedade [**Keys**](swbemobjectpath-keys.md) da instância [**SWbemObjectPath**](swbemobjectpath.md) retornada. Se você tentar chamar os métodos [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) nesse valor, receberá um erro wbemErrReadOnly. Além disso, você não pode modificar nenhum [**SWbemNamedValue**](swbemnamedvalue.md) obtido dessa coleção. As tentativas de modificar a propriedade **Value** retornam o mesmo código de erro.

No entanto, se você chamar [**SWbemObject \_ . Clone**](swbemobject-clone-.md) para criar uma cópia, a propriedade [**SWbemObjectPath. Path**](swbemobjectpath-path.md) da cópia será totalmente modificável.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir, obtido da [lista de todas as classes cimv2 do WMI](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) na galeria do TechNet, usa a propriedade Path \_ para listar todas as classes cimv2 do WMI.


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



 

 




