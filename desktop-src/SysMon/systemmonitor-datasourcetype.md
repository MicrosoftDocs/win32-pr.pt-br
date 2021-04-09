---
title: Propriedade DataSourceType SystemMonitor
description: Recupera ou define a origem dos dados do contador de desempenho.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Propriedade DataSourceType SysMon
- Propriedade DataSourceType SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, Propriedade DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009583"
---
# <a name="systemmonitordatasourcetype-property"></a>SystemMonitor: Propriedade ataSourceType de:D

Recupera ou define a origem dos dados do contador de desempenho.

## <a name="syntax"></a>Syntax


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Valor da propriedade

Origem dos dados do contador de desempenho. Para obter os valores possíveis, consulte [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).

## <a name="exceptions"></a>Exceções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de exceção</th>
<th>Condição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System. ArgumentException</strong></td>
<td>Você pode receber essa exceção por um dos seguintes motivos:
<ul>
<li>O valor da fonte de dados especificada não é válido.</li>
<li>Se a fonte de dados for um arquivo de log, o SYSMON não poderá localizar um dos arquivos especificados. O valor Err. Number é 0xC0000BD1.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

**Antes do Windows Vista:** Você não poderá adicionar ou remover arquivos de log da [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor dessa propriedade for definido como sysmonLogFiles. Defina o valor dessa propriedade como sysmonLogFiles depois de criar ou modificar a coleção de arquivos de log.

Além disso, você não pode modificar as propriedades [**SqlDsnName**](systemmonitor-sqldsnname.md) e [**SqlLogSetName**](systemmonitor-sqllogsetname.md) se o valor dessa propriedade não deve ser definido como sysmonSqlLog. Defina o valor dessa propriedade como sysmonSqlLog depois de modificar os nomes do servidor e do banco de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





