---
title: Classe Win32_TSLicenseReport
description: Fornece instâncias de Serviços de Área de Trabalho Remota licença de acesso para cliente por usuário (RDS \ 160; CAL por usuário) relatórios de uso que são gerados no servidor de licença Área de Trabalho Remota e métodos para operações de geração de relatório de licença, busca e exclusão.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReport Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReport classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824210"
---
# <a name="win32_tslicensereport-class"></a>\_Classe Win32 TSLicenseReport

Fornece instâncias de Serviços de Área de Trabalho Remota relatórios de uso de licença de acesso para cliente por usuário (RDS por CAL) que são geradas no servidor de licença Área de Trabalho Remota e métodos para operações de geração de relatório de licença, busca e exclusão.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSLicenseReport** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSLicenseReport** tem esses métodos.



| Método                                                                                                         | Descrição                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Exclui um objeto de relatório no servidor de licença Área de Trabalho Remota. Esse não é um método estático.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Recupera entradas no objeto de relatório.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Recupera detalhes das licenças de acesso para cliente por usuário com falha Serviços de Área de Trabalho Remota (RDS CALs por usuário) do relatório.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Recupera informações resumidas de falhas de Serviços de Área de Trabalho Remota por licenças de acesso para cliente por usuário (RDS CALs por usuário) do relatório.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Recupera informações de Serviços de Área de Trabalho Remota emitidos por licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) do relatório.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Recupera resumos de licenças do objeto de relatório.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Não há suporte para o método.<br/> **Windows server 2008 R2 e Windows server 2008:** Gera um relatório de uso de licença por usuário atual no servidor de licença Área de Trabalho Remota.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Gera um relatório de uso de licença por usuário atual no servidor de licença Área de Trabalho Remota.<br/>                                                                                              |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseReport** tem essas propriedades.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome do relatório.

</dd> <dt>

**GenerationDateTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora de geração de relatório de Licenciamento RD.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows server 2008 R2 e Windows server 2008:** Número de CALs por usuário do RDS que estão instaladas.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows server 2008 R2 e Windows server 2008:** Número de CALs por usuário do RDS que estão em uso no momento.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows server 2008 R2 e Windows server 2008:** Tipo de escopo do relatório de Licenciamento RD.

</dd> <dt>

**Escopovalue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows server 2008 R2 e Windows server 2008:** Valor de escopo do relatório de Licenciamento RD.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do relatório de Licenciamento RD.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os relatórios gerados usando o WMI são exibidos no Gerenciador de Licenciamento RD. Os relatórios excluídos usando o WMI também são excluídos do Gerenciador de Licenciamento RD.

Você deve ser um membro do grupo Administradores para usar essa classe.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

