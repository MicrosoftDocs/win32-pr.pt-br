---
title: Win32_TSLicenseReport classe
description: Fornece instâncias do Serviços de Área de Trabalho Remota por usuário de acesso ao cliente (RDS \ 160; Por CAL de Usuário) relatórios de uso gerados no servidor de licença Área de Trabalho Remota e métodos para operações de geração, busca e exclusão de relatórios de licença.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReport classe Serviços de Área de Trabalho Remota
- Win32_TSLicenseReport classe Serviços de Área de Trabalho Remota , descrito
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
ms.openlocfilehash: 93280c00cbd20993907901e1f9b8c16330863a47bddd4e08bc86d51b4b837233
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137829"
---
# <a name="win32_tslicensereport-class"></a>Classe Win32 \_ TSLicenseReport

Fornece instâncias de relatórios de uso de RDS por CAL (licença de acesso de cliente por usuário) do Serviços de Área de Trabalho Remota que são gerados no servidor de licença do Área de Trabalho Remota e métodos para operações de geração, busca e exclusão de relatórios de licença.

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

A **classe Win32 \_ TSLicenseReport** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ TSLicenseReport** tem esses métodos.



| Método                                                                                                         | Descrição                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteReport**](deletereport-win32-tslicensereport.md)                                                     | Exclui um objeto de relatório no servidor de Área de Trabalho Remota licença. Esse não é um método estático.<br/>                                                                                           |
| [**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)                                         | Recupera entradas no objeto de relatório.<br/>                                                                                                                                              |
| [**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)               | Recupera detalhes de licenças de acesso de cliente Serviços de Área de Trabalho Remota por usuário com falha (CALs de RDS por usuário) do relatório.<br/>                                                             |
| [**FetchReportFailedPerUserSummaryEntries**](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | Recupera informações resumidas de falhas Serviços de Área de Trabalho Remota licenças de acesso de cliente por usuário (CALs de RDS por usuário) do relatório.<br/>                                                 |
| [**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)                       | Recupera informações de licenças de acesso de cliente Serviços de Área de Trabalho Remota por dispositivo emitidas (CALs de RDS por dispositivo) do relatório.<br/>                                                     |
| [**FetchReportSummaryEntries**](win32-tslicensereport-fetchreportsummaryentries.md)                           | Recupera os resumos de licença do objeto de relatório.<br/>                                                                                                                                  |
| [**GenerateReport**](generatereport-win32-tslicensereport.md)                                                 | Não há suporte para o método.<br/> **Windows Server 2008 R2 e Windows Server 2008:** Gera um relatório de uso de licença atual por usuário no servidor de Área de Trabalho Remota licença.<br/> |
| [**GenerateReportEx**](generatereportex-win32-tslicensereport.md)                                             | Gera um relatório de uso de licença atual por usuário no servidor de Área de Trabalho Remota licença.<br/>                                                                                              |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSLicenseReport** tem essas propriedades.

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

Tipo de dados: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora de geração de relatório de licenciamento de RD.

</dd> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows Server 2008 R2 e Windows Server 2008:** Número de CALs de RDS por usuário instaladas.

</dd> <dt>

**LicenseUsageCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows Server 2008 R2 e Windows Server 2008:** Número de CALs de RDS por usuário que estão em uso no momento.

</dd> <dt>

**ScopeType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows Server 2008 R2 e Windows Server 2008:** Tipo de escopo do relatório de licenciamento de área de trabalho de área de trabalho.

</dd> <dt>

**ScopeValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **PRETERIDO**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Não há suporte a esta propriedade.

**Windows Server 2008 R2 e Windows Server 2008:** Valor do escopo do relatório de licenciamento de área de trabalho de área de trabalho.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do relatório de licenciamento de RD.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os relatórios gerados usando o WMI são exibidos no Gerenciador de Licenciamento de Área de Trabalho Local. Os relatórios excluídos usando o WMI também são excluídos do Gerenciador de Licenciamento de RD.

Você deve ser um membro do grupo Administradores para usar essa classe.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

