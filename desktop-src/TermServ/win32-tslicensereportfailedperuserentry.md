---
title: Win32_TSLicenseReportFailedPerUserEntry classe
description: Fornece detalhes sobre a licença de acesso Serviços de Área de Trabalho Remota cliente por usuário com falha (RDS \ 160; CAL por usuário).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportFailedPerUserEntry classe Serviços de Área de Trabalho Remota
- Win32_TSLicenseReportFailedPerUserEntry classe Serviços de Área de Trabalho Remota , descrito
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
ms.openlocfilehash: c02d56c1a7e2c715f068d808d45ac6ae3295b16bb7382179ec0e32c93beee096
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420836"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a>Classe Win32 \_ TSLicenseReportFailedPerUserEntry

Fornece detalhes sobre a licença de acesso Serviços de Área de Trabalho Remota cliente por usuário com falha (CAL de RDS por usuário).

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

A **classe Win32 \_ TSLicenseReportFailedPerUserEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSLicenseReportFailedPerUserEntry** tem essas propriedades.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de CAL emitido. Esse será um dos valores a seguir.

"TS por CAL de dispositivo integrado"

"TS por CAL do dispositivo"

"CAL do Conector da Internet do TS"

"TS per User CAL"

"TS ou RDS por CAL de dispositivo"

"TS ou RDS por CAL de usuário"

"Licença de assinatura do VDI Standard Suite per Device"

"Licença de assinatura do VDI Premium Suite per Device"

"CAL de RDS por dispositivo"

"CAL de RDS por usuário"

</dd> <dt>

**Productversion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão do Serviços de Área de Trabalho Remota para a qual a CAL de RDS por usuário foi emitida. Esse será um dos valores a seguir.

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

**TriedIssuanceOn**
</dt> <dd> <dl> <dt>

Tipo de dados: **DATETIME**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data em que foi tentada a emissão de licença.

</dd> <dt>

**Usuário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome do usuário ao qual a emissão de licença foi tentada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FetchReportFailedPerUserEntries**](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 

