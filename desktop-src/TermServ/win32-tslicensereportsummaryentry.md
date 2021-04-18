---
title: Classe Win32_TSLicenseReportSummaryEntry
description: Fornece um resumo das licenças de acesso para cliente de Serviços de Área de Trabalho Remota instaladas e emitidas por usuário (RDS \ 160; CALs por usuário).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportSummaryEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportSummaryEntry classe, descrita
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
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811903"
---
# <a name="win32_tslicensereportsummaryentry-class"></a>\_Classe Win32 TSLicenseReportSummaryEntry

Fornece um resumo das licenças de acesso para cliente de Serviços de Área de Trabalho Remota instaladas e emitidas por usuário (RDS CALs por usuário).

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

A classe **Win32 \_ TSLicenseReportSummaryEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseReportSummaryEntry** tem essas propriedades.

<dl> <dt>

**InstalledLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de CALs por usuário do RDS que estão instaladas.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de CALs de RDS por usuário que são emitidas.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Versão do Serviços de Área de Trabalho Remota para a qual a CAL RDS por usuário foi emitida.

<dt>

"Windows Server 2012"
</dt> <dd>

Somente os servidores que executam o Windows Server 2012, Windows Server 2008 R2 ou Windows Server 2008 têm suporte com esta licença.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Somente os servidores que executam o Windows Server 2008 R2 ou o Windows Server 2008 têm suporte com esta licença.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Somente servidores que executam o Windows Server 2008 têm suporte com esta licença.

</dd> </dl>

</dd> <dt>

**ProductVersionid**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de versão do produto para o pacote de chaves de licença Serviços de Área de Trabalho Remota.

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

Não há suporte.

</dd> <dt>

0
</dt> <dd>

Não há suporte.

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

Há
</dt> <dd>

As CALs do RDS por usuário estão disponíveis.

</dd> <dt>

Certo
</dt> <dd>

A disponibilidade das CALs de RDS por usuário é limitada.

</dd> <dt>

"None"
</dt> <dd>

As CALs do RDS por usuário não estão disponíveis.

</dd> <dt>

"Sem rastreamento"
</dt> <dd>

A disponibilidade das CALs de RDS por usuário não está sendo acompanhada.

</dd> </dl>

</dd> <dt>

**TSCALType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de RDS CALs por usuário. Esse será um dos valores a seguir.

<dt>

"Por dispositivo"
</dt> <dd>

As CALs do RDS por usuário são emitidas por dispositivo.

</dd> <dt>

"Por usuário"
</dt> <dd>

As CALs do RDS por usuário são emitidas por usuário.

</dd> <dt>

Conhecidos
</dt> <dd>

O tipo de RDS CALs por usuário é desconhecido.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



 

 





