---
title: Classe Win32_TSLicenseReportEntry
description: Fornece detalhes do Serviços de Área de Trabalho Remota emitido por licença de acesso para cliente por usuário (RDS \ 160; CAL por usuário).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSLicenseReportEntry Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSLicenseReportEntry classe, descrita
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
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369263"
---
# <a name="win32_tslicensereportentry-class"></a>\_Classe Win32 TSLicenseReportEntry

Fornece detalhes do Serviços de Área de Trabalho Remota emitido por licença de acesso para cliente por usuário (RDS CAL por usuário).

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

A classe **Win32 \_ TSLicenseReportEntry** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSLicenseReportEntry** tem essas propriedades.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de CAL emitida. Esse será um dos valores a seguir.

**Windows server 2008 R2 e Windows server 2008:** Não há suporte para essa propriedade.

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

Data de validade da licença que foi emitida para o usuário.

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

