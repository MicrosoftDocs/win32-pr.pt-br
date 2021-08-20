---
description: Altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 29155533-0898-4f8f-af08-f3ea46c8c1d3
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe CIM_LogicalFile dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b550ca2c3297d4f2185918036bc283138e619dda2e1facff696ec8fe868e07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081020"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_logicalfile-class"></a>Método ChangeSecurityPermissionsEx da classe \_ LogicalFile CIM

O **método ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo lógico especificado no caminho do objeto (esse método é uma versão estendida do [**método ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-cim-logicalfile.md) Se o arquivo lógico for um diretório, esse método atuará recursivamente, alterando as permissões de segurança para todos os arquivos e subdados que o diretório contém.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecurityDescriptor* \[ Em\]
</dt> <dd>

Especifica as informações de segurança.

</dd> <dt>

*Opção* \[ Em\]
</dt> <dd>

Privilégio de segurança a ser modificado. Por exemplo, para alterar o proprietário e a segurança da DACL, use

`Option = 1 + 4`

ou

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Alterar \_ Informações \_ de segurança do \_ proprietário** (1)


</dt> <dd>

Altere o proprietário do arquivo lógico.

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Alterar \_ Informações \_ de \_ segurança de** grupo (2)


</dt> <dd>

Altere o grupo do arquivo lógico.

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Alterar \_ Informações de \_ segurança \_ da dacl** (4)


</dt> <dd>

Altere a ACL do arquivo lógico.

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Alterar \_ Informações de \_ \_ segurança do Sacl** (8)


</dt> <dd>

Altere a ACL do sistema do arquivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro terá um valor **nulo se** o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ in, opcional\]
</dt> <dd>

Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como um ponto de partida para esse método. Normalmente, o *parâmetro StartFileName* é o parâmetro *StopFileName* que especifica o arquivo (ou diretório) no qual ocorreu um erro da chamada de método anterior. Se o valor do parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na [**chamada ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Recursivo* \[ in, opcional\]
</dt> <dd>

Se **TRUE**, as permissões de segurança serão aplicadas recursivamente a arquivos e diretórios dentro do diretório especificado pela [**instância de \_ LogicalFile cim.**](cim-logicalfile.md) Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**Êxito**
</dt> <dd>

0

Sucesso.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

Acesso negado

</dd> <dt>

**Falha não especificada**
</dt> <dd>

8

Falha não especificada.

</dd> <dt>

**Objeto inválido**
</dt> <dd>

9

Objeto inválido.

</dd> <dt>

**O objeto já existe**
</dt> <dd>

10

O objeto já existe.

</dd> <dt>

**Sistema de arquivos não NTFS**
</dt> <dd>

11

Sistema de arquivos não NTFS.

</dd> <dt>

**Plataforma não NT/Windows 2000**
</dt> <dd>

12

Plataforma não Windows.

</dd> <dt>

**A unidade não é a mesma**
</dt> <dd>

13

A unidade não é a mesma.

</dd> <dt>

**Diretório não vazio**
</dt> <dd>

14

O diretório não está vazio.

</dd> <dt>

**Violação de compartilhamento**
</dt> <dd>

15

Violação de compartilhamento.

</dd> <dt>

**Arquivo inicial inválido**
</dt> <dd>

16

Arquivo inicial inválido.

</dd> <dt>

**Privilégio não mantido**
</dt> <dd>

17

Privilégio não mantido.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalFile**](changesecuritypermissionsex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> </dl>

 

