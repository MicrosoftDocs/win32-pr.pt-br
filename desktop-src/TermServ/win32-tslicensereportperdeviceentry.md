---
title: Classe Win32_TSLicenseReportPerDeviceEntry
description: Fornece detalhes sobre a Serviços de Área de Trabalho Remota com falha por licença de acesso para cliente por dispositivo (RDS \ 160; CAL por dispositivo).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportPerDeviceEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportPerDeviceEntry classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbcdad271a346820b318c94bed7ce6b9b9527d3fdd7df9cc3f1dc9d9a97aae3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008416"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a>\_Classe Win32 TSLicenseReportPerDeviceEntry

Fornece detalhes sobre o Serviços de Área de Trabalho Remota com falha por licença de acesso para cliente por dispositivo (RDS CAL por dispositivo).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSLicenseReportPerDeviceEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseReportPerDeviceEntry** tem essas propriedades.

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

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data de validade da licença.

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

somente os servidores que executam Windows Server 2012, Windows server 2008 R2 ou Windows server 2008 têm suporte com esta licença.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

somente os servidores que executam o Windows server 2008 R2 ou o Windows server 2008 têm suporte com esta licença.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

somente os servidores que executam o Windows Server 2008 têm suporte com esta licença.

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

Sem suporte.

</dd> <dt>

0
</dt> <dd>

Sem suporte.

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O identificador de hardware do computador.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do computador para o qual a emissão de licença foi tentada.

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

[**FetchReportPerDeviceEntries**](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 

