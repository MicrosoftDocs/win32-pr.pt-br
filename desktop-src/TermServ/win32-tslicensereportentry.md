---
title: Win32_TSLicenseReportEntry classe
description: Fornece detalhes da licença de acesso do cliente Serviços de Área de Trabalho Remota por usuário (RDS \ 160; CAL por usuário).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry classe Serviços de Área de Trabalho Remota
- Win32_TSLicenseReportEntry classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08041ac0878f3466712001a0a5e2cc90eb74ea1e360da9785b5d84805574389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126516"
---
# <a name="win32_tslicensereportentry-class"></a>Classe Win32 \_ TSLicenseReportEntry

Fornece detalhes sobre a licença de acesso do cliente Serviços de Área de Trabalho Remota por usuário emitida (CAL de RDS por usuário).

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSLicenseReportEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSLicenseReportEntry** tem essas propriedades.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de CAL emitido. Esse será um dos valores a seguir.

**Windows Server 2008 R2 e Windows Server 2008:** Não há suporte para essa propriedade.

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

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DATETIME**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data de validade da licença que foi emitida para o usuário.

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

Identificador de versão do produto para o Serviços de Área de Trabalho Remota de chaves de licença.

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

**Usuário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome do usuário para o qual a licença foi emitida.

</dd> </dl>

## <a name="remarks"></a>Comentários

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

