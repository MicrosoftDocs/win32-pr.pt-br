---
title: Classe Win32_TSLicenseReportFailedPerUserEntry
description: Fornece detalhes sobre a licença de acesso para cliente de Serviços de Área de Trabalho Remota por usuário com falha (RDS \ 160; CAL por usuário).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportFailedPerUserEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportFailedPerUserEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369262"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>\_Classe Win32 TSLicenseReportFailedPerUserEntry

Fornece detalhes sobre a licença de acesso para cliente de Serviços de Área de Trabalho Remota por usuário com falha (RDS CAL por usuário).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSLicenseReportFailedPerUserEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseReportFailedPerUserEntry** tem essas propriedades.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de CAL emitida. Esse será um dos valores a seguir.

"Interno de TS por dispositivo CAL"

"TS CAL por dispositivo"

"CAL do conector de Internet TS"

"TS CAL por usuário"

"TS ou RDS CAL por dispositivo"

"TS ou RDS CAL por usuário"

"VDI Standard Suite por licença de assinatura de dispositivo"

"VDI Premium Suite por licença de assinatura de dispositivo"

"RDS CAL por dispositivo"

"RDS CAL por usuário"

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão do Serviços de Área de Trabalho Remota para a qual a CAL RDS por usuário foi emitida. Esse será um dos valores a seguir.

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

**TriedIssuanceOn**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data em que foi tentada a emissão da licença.

</dd> <dt>

**Usuário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome do usuário para o qual a emissão de licença foi tentada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

