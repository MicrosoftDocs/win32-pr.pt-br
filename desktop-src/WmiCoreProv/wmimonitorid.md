---
description: Representa as informações de identificação sobre um monitor de vídeo, como nome do fabricante, ano de fabricação ou número de série.
ms.assetid: 85c8c4b1-20e2-4c0b-9209-a3724509a2f0
title: Classe WmiMonitorID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorID
- WmiMonitorID.Active
- WmiMonitorID.InstanceName
- WmiMonitorID.ManufacturerName
- WmiMonitorID.ManufacturerNameLength
- WmiMonitorID.ProductCodeID
- WmiMonitorID.SerialNumberID
- WmiMonitorID.WeekOfManufacture
- WmiMonitorID.YearOfManufacture
- WmiMonitorID.UserFriendlyName
- WmiMonitorID.UserFriendlyNameLength
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.custom: project-verbatim
ms.openlocfilehash: 552e66a4e3a0c6f120bcc95123e3a2674fc579457de16c9ef8cd1e80161f175e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051144"
---
# <a name="wmimonitorid-class"></a>Classe WmiMonitorID

A **classe WMI WmiMonitorID** representa as informações de identificação sobre um monitor de vídeo, como nome do fabricante, ano de fabricação ou número de série. Os dados nessa classe correspondem aos dados no bloco De identificação de fornecedor/produto da definição de entrada de vídeo do padrão E-EDID (Video Electronics Standard Association) enhanced Display Identification Data (E-EDID).

## <a name="syntax"></a>Sintaxe

``` syntax
class WmiMonitorID : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint16  ManufacturerName[];
  uint16  ManufacturerNameLength;
  uint16  ProductCodeID[];
  uint16  SerialNumberID[];
  uint8   WeekOfManufacture;
  uint16  YearOfManufacture;
  uint16  UserFriendlyName[];
  uint16  UserFriendlyNameLength;
};
```

## <a name="members"></a>Membros

A **classe WmiMonitorID** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe WmiMonitorID** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o monitor ativo.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Nome da instância de monitor específica.

</dd> <dt>

**ManufacturerName**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do fabricante.

</dd> <dt>

**ManufacturerNameLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Comprimento do nome do fabricante localizado na **propriedade ManufacturerName.**

</dd> <dt>

**ProductCodeID**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

ID do código do produto atribuída pelo fornecedor.

</dd> <dt>

**SerialNumberID**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de série.

</dd> <dt>

UserFriendlyName
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome amigável do monitor. O tamanho do nome é o comprimento especificado pela propriedade UserFriendlyNameLength.

</dd> <dt>

UserFriendlyNameLength
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de caracteres no nome localizado na propriedade UserFriendlyName.

</dd> <dt>

**WeekOfManufacture**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Semana de fabricação por número da semana. O intervalo é de 1 a 53. Zero (0) é indefinido.

</dd> <dt>

**YearOfManufacture**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ano de fabricação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter uma discussão sobre como traduzir as matrizes que armazenam as IDs de número de série, consulte o artigo Informações do Monitor de Relatórios [Gerenciador de Configurações](/archive/blogs/kmongwa/reporting-monitor-information-with-configuration-manager) blog.

## <a name="examples"></a>Exemplos

O exemplo do PowerShell a seguir recupera o número de série de vários monitores.


```PowerShell
gwmi WmiMonitorID -Namespace root\wmi | ForEach-Object {($_.UserFriendlyName -ne 0 | foreach {[char]$_}) -join ""; ($_.SerialNumberID -ne 0 | foreach {[char]$_}) -join ""}
```



O código VBScript a seguir também recupera informações de ID do monitor de um sistema.


```VB
Option Explicit

Dim strComputer, objWMIService, colItems, objItem

strComputer = "MyComputer"

Set objWMIService = GetObject("winmgmts:" _ 
  & "{impersonationLevel=impersonate,authenticationLevel=Pkt}!\\" _ 
  & strComputer & "\root\wmi") 

Set colItems = objWMIService.ExecQuery _
  ("SELECT * FROM WMIMonitorID")

For Each objItem In colItems
  Wscript.Echo objItem.InstanceName
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | WMI \\ raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

