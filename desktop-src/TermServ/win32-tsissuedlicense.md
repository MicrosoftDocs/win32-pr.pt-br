---
title: Win32_TSIssuedLicense classe
description: Descreve instâncias de licenças Serviços de Área de Trabalho Remota acesso de cliente por dispositivo (RDS \ 160; Por CALs de dispositivo) que são emitidas de um Área de Trabalho Remota de licença.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense classe Serviços de Área de Trabalho Remota
- Win32_TSIssuedLicense classe Serviços de Área de Trabalho Remota , descrita
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76127d41c6a571b6bc75bc74378b21f76f4b38c05f0a223d36e979dccf89a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656156"
---
# <a name="win32_tsissuedlicense-class"></a>Classe Win32 \_ TSIssuedLicense

Descreve as instâncias do Serviços de Área de Trabalho Remota por dispositivo de acesso ao cliente (CALs RDS por dispositivo) emitidas de um servidor de Área de Trabalho Remota licença.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a>Membros

A **classe \_ Win32 TSIssuedLicense** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Win32 TSIssuedLicense** tem esses métodos.



| Método                                         | Descrição                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Revogar**](revoke-win32-tsissuedlicense.md) | Revoga as CALs de RDS por dispositivo representadas pelo objeto **\_ Win32 TSIssuedLicense.**<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ Win32 TSIssuedLicense** tem essas propriedades.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DATETIME**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a data em que a licença expirará.

</dd> <dt>

**Issuedate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DATETIME**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a data em que a licença foi emitida.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica o pacote Serviços de Área de Trabalho Remota chave de licença.

</dd> <dt>

**LicenseId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador exclusivo para esta licença.

</dd> <dt>

**StatusLicença**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Status da licença.

<dt>

0
</dt> <dd>

O status da licença é desconhecido.

</dd> <dt>

1
</dt> <dd>

A licença é uma licença temporária.

</dd> <dt>

2
</dt> <dd>

A licença está ativa.

</dd> <dt>

3
</dt> <dd>

A licença é uma licença de atualização.

</dd> <dt>

4
</dt> <dd>

A licença foi revogada.

</dd> <dt>

5
</dt> <dd>

O status da licença está pendente.

</dd> <dt>

6
</dt> <dd>

A licença é uma licença simultânea.

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador de hardware para o qual a licença foi emitida.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador para o qual a licença foi emitida.

</dd> <dt>

**sIssuedToUser**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome de usuário para o qual a licença foi emitida.

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

