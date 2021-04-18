---
description: Use a propriedade Count do objeto SWbemObjectSet para determinar quantos itens estão em uma coleção SWbemObjectSet. Esta propriedade é somente para leitura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propriedade SWbemObjectSet. Count (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3154e22bbdbc75080ceebdf8b1eef602cf5c3be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764388"
---
# <a name="swbemobjectsetcount-property"></a>Propriedade SWbemObjectSet. Count

Use a propriedade **Count** do objeto [**SWbemObjectSet**](swbemobjectset.md) para determinar quantos itens estão em uma coleção **SWbemObjectSet** . Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Um ponto a ser cuidadoso ao usar Count é que o WMI não mantém uma contagem em execução do número de itens em uma coleção. Se você solicitar a contagem de uma coleção, o WMI não poderá responder instantaneamente com um número; em vez disso, ele deve contar literalmente os itens, enumerando a coleção inteira. Para uma coleção que tem relativamente poucos itens, como serviços, essa enumeração provavelmente levará menos de um segundo. A contagem do número de eventos em uma coleção de log de eventos, no entanto, pode demorar consideravelmente mais.

E, em seguida, suponha que você deseja exibir os valores de propriedade para cada evento na coleção. Nesse caso, o WMI terá que enumerar toda a coleção uma segunda vez.

> [!Note]  
> Se você tentar obter essa propriedade de um objeto [**SWbemObjectSet**](swbemobjectset.md) que é retornado de um método em que os sinalizadores especificados estão incluídos no sinalizador wbemFlagForwardOnly, você receberá um erro wbemErrFailed.

 

## <a name="examples"></a>Exemplos

Na maior parte, a única coisa que você fará com um SWbemObjectSet é enumerar todos os objetos contidos na coleção em si. No entanto, a contagem de contagem que pode ser útil no script de administração do sistema. Como o nome implica, Count informa o número de itens na coleção. Por exemplo, esse script recupera uma coleção de todos os serviços instalados em um computador e, em seguida, ecoa o número total de serviços encontrados:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



O que torna a contagem útil é que ele pode informar se uma instância específica está disponível em um computador. Por exemplo, esse script recupera uma coleção de todos os serviços em um computador que tem o nome W3SVC. Se a contagem for 0 (e for válida para que as coleções não tenham nenhuma instância), isso significará que o serviço W3SVC não está instalado no computador.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | ISWbemObjectSet de IID \_<br/>                                                         |



 

 




