---
title: Propriedade SystemMonitor SqlDsnName
description: Recupera ou define o nome da fonte de dados ODBC (DSN).
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Propriedade SqlDsnName SysMon
- Propriedade SqlDsnName SysMon, interface SystemMonitor
- Interface SystemMonitor SysMon, Propriedade SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369200"
---
# <a name="systemmonitorsqldsnname-property"></a>Propriedade SystemMonitor:: SqlDsnName

Recupera ou define o nome da fonte de dados ODBC (DSN).

## <a name="syntax"></a>Syntax


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Valor da propriedade

O nome da fonte de dados ODBC que aponta para um banco de dado que contém as tabelas Perfmon corretas. O formato é SQL: DSN.

## <a name="remarks"></a>Comentários

Você deve usar o snap-in do MMC Perfmon. msc para gerar o arquivo de log do SQL. Os logs de contador estão localizados em **logs e alertas de desempenho**. Para especificar um log SQL, clique com o botão direito do mouse no arquivo de log que você criou e selecione **Propriedades** no menu. Na página de propriedades **arquivos de log** , selecione **banco de dados SQL** na caixa de listagem suspensa **tipo de arquivo de log** .

**Antes do Windows Vista:** Você não poderá modificar essa propriedade se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). Você deve primeiro especificar o nome e, em seguida, definir **SystemMonitor. DataSourceType** como **DataSourceTypeConstants.sysmonSqlLog**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





