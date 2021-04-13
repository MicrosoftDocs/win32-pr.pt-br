---
title: Constantes de enumeração (WSManDisp. h)
description: A enumeração contém constantes, conforme listado na lista a seguir, usada no parâmetro flags por chamadas para a enumeração Session. Enumerate e IWSManSession.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369420"
---
# <a name="enumeration-constants"></a>Constantes de enumeração

A enumeração **\_ \_ WSManEnumFlags** contém constantes, conforme listado na lista a seguir, usada no parâmetro *flags* por chamadas para [**Session. Enumerate**](session-enumerate.md) e [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

Lembre-se de que **WSManFlagReturnObject** e **WSManFlagHierarchyDeep** são o padrão se o parâmetro *flags* não for especificado.

<dl> <dt>

<span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



Os lotes contêm as instâncias XML solicitadas. Esse é o valor padrão para o parâmetro Flag.

O método de script associado é [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) e o método C++ é [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Esse sinalizador controla como o parâmetro de *filtro* na chamada para [**Session. Enumerate**](session-enumerate.md) é interpretado pelo WinRM.

O formato do filtro pode ser um fragmento XML ou uma cadeia de caracteres de texto sem formatação. O formato é determinado pelo [*dialeto de filtro*](windows-remote-management-glossary.md) do [*filtro*](windows-remote-management-glossary.md) usado na chamada para [**Session. enumerar**](session-enumerate.md) ou [**IWSManSession:: enumerar**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), que é específica para a operação executada.

Se o parâmetro *dialeto* não for especificado, o WinRM tentará determinar o dialeto com base no primeiro caractere do filtro. Se o primeiro caractere for <, mas o filtro não for, na verdade, um fragmento XML, esse sinalizador deverá ser definido. Por exemplo, um filtro no formato a seguir requer que você defina **WSManFlagNonXmlText** para que o filtro seja interpretado corretamente:

`<25 && > 1`

Se o filtro for um fragmento XML, esse sinalizador não será necessário porque o fragmento começa com <, que o WinRM interpreta corretamente como XML. Por exemplo,

`<filter>select * from aDataStructure</filter>`

Se o filtro estiver em texto sem formatação que não comece com <, esse sinalizador não será necessário. Por exemplo,

`select * from aDataStructure`

O método de script associado é [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) e o método C++ é [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).


</dt> </dl> </dd> <dt>

<span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Os lotes contêm referências de ponto de extremidade (EPRs) para as instâncias XML correspondentes, mas não as instâncias reais.

O método de script associado é [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) e o método C++ é [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Os lotes contêm as instâncias XML solicitadas e os EPRs correspondentes contidos em um elemento [*WSMan: Items*](windows-remote-management-glossary.md) .

O método de script associado é [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) e o método C++ é [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



As instâncias de classe derivadas são incluídas e são representadas de acordo com seus esquemas reais.

O método de script associado é [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) e o método C++ é [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



As instâncias de classe derivadas são excluídas. Somente as instâncias do tipo solicitado são mostradas.

O método de script associado é [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) e o método C++ é [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).


</dt> </dl> </dd> <dt>

<span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



As instâncias de classe derivadas são incluídas e são representadas de acordo com o esquema de classe base. As propriedades definidas na classe derivada não são mostradas.

O método de script associado é [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) e o método C++ é [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes e enumerações do WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[Enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[Consultando instâncias específicas de um recurso](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





