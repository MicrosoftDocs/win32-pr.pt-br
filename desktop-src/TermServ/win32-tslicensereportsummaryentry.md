---
title: Win32_TSLicenseReportSummaryEntry classe
description: Fornece um resumo das licenças de acesso do cliente Serviços de Área de Trabalho Remota por usuário instaladas e emitidas (RDS \ 160; CALs por usuário).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportSummaryEntry classe Serviços de Área de Trabalho Remota
- Win32_TSLicenseReportSummaryEntry classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58efc2c70019037219d8eca986fa8afd81e4dc2d06cd638ee24fc59947e3bf3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137789"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>Classe Win32 \_ TSLicenseReportSummaryEntry

Fornece um resumo das licenças de acesso do cliente Serviços de Área de Trabalho Remota por usuário instaladas e emitidas (CALs de RDS por usuário).

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSLicenseReportSummaryEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSLicenseReportSummaryEntry** tem essas propriedades.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de CALs de RDS por usuário instaladas.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de CALs de RDS por usuário emitidas.

</dd> <dt>

**Productversion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do Serviços de Área de Trabalho Remota para a qual a CAL de RDS por usuário foi emitida.

<dt>

"Windows Server 2012"
</dt> <dd>

Somente servidores que executam Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com essa licença.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Somente servidores que executam Windows Server 2008 R2 ou Windows Server 2008 têm suporte com essa licença.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Somente servidores que executam Windows Server 2008 têm suporte com essa licença.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de versão do produto para Serviços de Área de Trabalho Remota pacote de chaves de licença.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

Sem suporte.

</dd> <dt>

0
</dt> <dd>

Sem suporte.

</dd> </dl>

</dd> <dt>

**TSCALAvailability**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A disponibilidade das CALs de RDS por usuário. Esse será um dos valores a seguir.

<dt>

"Disponível"
</dt> <dd>

As CALs de RDS por usuário estão disponíveis.

</dd> <dt>

"Limitado"
</dt> <dd>

A disponibilidade das CALs de RDS por usuário é limitada.

</dd> <dt>

"None"
</dt> <dd>

As CALs de RDS por usuário não estão disponíveis.

</dd> <dt>

"Não acompanhando"
</dt> <dd>

A disponibilidade das CALs de RDS por usuário não está sendo controlada.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de CALs de RDS por usuário. Esse será um dos valores a seguir.

<dt>

"Por Dispositivo"
</dt> <dd>

As CALs de RDS por usuário são emitidas por dispositivo.

</dd> <dt>

"Por Usuário"
</dt> <dd>

As CALs de RDS por usuário são emitidas por usuário.

</dd> <dt>

"Desconhecido"
</dt> <dd>

O tipo de CALs de RDS por usuário é desconhecido.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





