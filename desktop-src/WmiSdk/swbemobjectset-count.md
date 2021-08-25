---
description: Use a propriedade Count do objeto SWbemObjectSet para determinar quantos itens estão em uma coleção SWbemObjectSet. Esta propriedade é somente para leitura.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propriedade SWbemObjectSet.Count (Wbemdisp.h)
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
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857226"
---
# <a name="swbemobjectsetcount-property"></a>Propriedade SWbemObjectSet.Count

Use a **propriedade Count** do objeto [**SWbemObjectSet**](swbemobjectset.md) para determinar quantos itens estão em uma **coleção SWbemObjectSet.** Esta propriedade é somente para leitura.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Uma coisa a ser cuidadosa ao usar Count é que o WMI não mantém uma contagem em execução do número de itens em uma coleção. Se você solicitar Contagem para uma coleção, o WMI não poderá responder instantaneamente com um número; em vez disso, ele deve contar literalmente os itens, enumerando toda a coleção. Para uma coleção que tem relativamente poucos itens, como serviços, essa enumeração provavelmente leva menos de um segundo. No entanto, contar o número de eventos em uma coleção de log de eventos pode levar consideravelmente mais tempo.

E, em seguida, suponha que você deseja exibir os valores de propriedade para cada evento na coleção. Se sim, o WMI terá que enumerar toda a coleção uma segunda vez.

> [!Note]  
> Se você tentar obter essa propriedade de um objeto [**SWbemObjectSet**](swbemobjectset.md) retornado de um método em que os sinalizadores especificados estão incluídos no sinalizador wbemFlagForwardOnly, você receberá um erro wbemErrFailed.

 

## <a name="examples"></a>Exemplos

Na maior parte do tempo, a única coisa que você fará com um SWbemObjectSet é enumerar todos os objetos contidos na própria coleção. No entanto, a Contagem de Contagem que pode ser útil no script de administração do sistema. Como o nome indica, Count informa o número de itens na coleção. Por exemplo, esse script recupera uma coleção de todos os serviços instalados em um computador e, em seguida, ecoa o número total de serviços encontrados:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



O que torna a Contagem útil é que ela pode dizer se uma instância específica está disponível em um computador. Por exemplo, esse script recupera uma coleção de todos os serviços em um computador que tem o nome W3SVC. Se Count for 0 (e for válido para que as coleções não tenham instâncias), isso significa que o serviço W3SVC não está instalado no computador.


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
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




