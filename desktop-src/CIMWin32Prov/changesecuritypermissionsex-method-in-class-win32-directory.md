---
description: Altera as permissões de segurança para o arquivo de entrada de diretório especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 787e48af-7cb4-4d0b-a2f1-ffa696466ef2
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4bcadd4a4ad115a1a367db4f2a2f645eb6a4742c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164006"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_directory-class"></a>Método ChangeSecurityPermissionsEx da classe do \_ diretório Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de entrada de diretório especificado no caminho do objeto (esse método é uma versão estendida do método [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-win32-directory.md) ). Se o arquivo lógico for um diretório, esse método será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

*SecurityDescriptor* \[ no\]
</dt> <dd>

Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Esse parâmetro contém novas permissões de segurança para a instância [**do \_ arquivo de paginação Win32**](win32-pagefile.md).

</dd> <dt>

*Opção* \[ no\]
</dt> <dd>

Privilégio de segurança a ser modificado. Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use o seguinte:

`Option = 1 + 4`

– ou –

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do proprietário** (1)


</dt> <dd>

Altere o proprietário do arquivo lógico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Alterar \_ \_ \_ Informações de segurança do grupo** (2)


</dt> <dd>

Altere o grupo do arquivo lógico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da DACL** (4)


</dt> <dd>

Altere a lista DACL do arquivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)


</dt> <dd>

Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ fora\]
</dt> <dd>

Nome do arquivo ou diretório em que o método **ChangeSecurityPermissionsEx** falhou. Esse parâmetro será nulo se o método tiver sucesso.

</dd> <dt>

*StartFileName* \[ em, opcional\]
</dt> <dd>

Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **ChangeSecurityPermissionsEx**. Normalmente, o parâmetro *StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório em que ocorreu um erro da chamada de método anterior. Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** . Esse parâmetro é opcional.

Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.

</dd> <dt>

*Recursivo* \[ em, opcional\]
</dt> <dd>

Se for **true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) . Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado. Esse parâmetro é opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se as permissões forem alteradas e um número diferente para indicar um erro.

<dl> <dt>

**Êxito**
</dt> <dd>

0

A solicitação foi bem-sucedida.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

O acesso foi negado.

</dd> <dt>

**Falha não especificada**
</dt> <dd>

8

Ocorreu uma falha não especificada.

</dd> <dt>

**Objeto inválido**
</dt> <dd>

9

O nome especificado não é válido.

</dd> <dt>

**O objeto já existe**
</dt> <dd>

10

O objeto especificado já existe.

</dd> <dt>

**Sistema de arquivos não NTFS**
</dt> <dd>

11

O sistema de arquivos não é um sistema de arquivos NTFS.

</dd> <dt>

**Plataforma não NT/Windows 2000**
</dt> <dd>

12

A plataforma não é o Windows.

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

Há uma violação de compartilhamento.

</dd> <dt>

**Arquivo de início inválido**
</dt> <dd>

16

O arquivo de início especificado não é válido.

</dd> <dt>

**Privilégio não mantido**
</dt> <dd>

17

Um privilégio necessário para a operação não é mantido.

</dd> <dt>

**Parâmetro inválido**
</dt> <dd>

21

Um parâmetro especificado não é válido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Diretório Win32**](win32-directory.md)
</dt> </dl>

 

