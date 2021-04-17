---
title: Classe Win32_TSIssuedLicense
description: Descreve instâncias de Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS \ 160; CALs por dispositivo) emitidas de um servidor de licença Área de Trabalho Remota.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSIssuedLicense Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSIssuedLicense classe, descrita
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
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784056"
---
# <a name="win32_tsissuedlicense-class"></a>\_Classe Win32 TSIssuedLicense

Descreve instâncias de Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) emitidas de um servidor de licença Área de Trabalho Remota.

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

A classe **Win32 \_ TSIssuedLicense** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSIssuedLicense** tem esses métodos.



| Método                                         | Descrição                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Cancelar**](revoke-win32-tsissuedlicense.md) | Revoga as CALs de RDS por dispositivo que são representadas pelo **objeto \_ TSIssuedLicense do Win32** .<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSIssuedLicense** tem essas propriedades.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a data em que a licença irá expirar.

</dd> <dt>

**Emitido**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a data em que a licença foi emitida.

</dd> <dt>

**Pacote de chaves**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica o pacote de chaves de licença Serviços de Área de Trabalho Remota.

</dd> <dt>

**Licenseid**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador exclusivo desta licença.

</dd> <dt>

**StatusLicença**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
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

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

