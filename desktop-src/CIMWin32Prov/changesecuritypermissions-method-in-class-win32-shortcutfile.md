---
description: Altera as permissões de segurança para o arquivo de atalho lógico especificado no caminho do objeto.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe Win32_ShortcutFile dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 43d69f8a04fd937591675fe13fefd9499fe4c0dd59f70da02077cb97f7b06fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010098"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a>Método ChangeSecurityPermissions da classe ShortcutFile win32 \_

O método de classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de atalho lógico especificado no caminho do objeto. Se o arquivo lógico for um diretório, **ChangeSecurityPermissions** será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretivos que o diretório contém. **ChangeSecurityPermissions** retornará um valor inteiro de 0 (zero) se as permissões são alteradas e um número diferente para indicar um erro.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecurityDescriptor* \[ Em\]
</dt> <dd>

Expressão que é resolvida para uma instância do [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Esse descritor contém novas permissões de segurança para a instância do [**Win32 \_ PageFile.**](win32-pagefile.md)

</dd> <dt>

*Opção* \[ Em\]
</dt> <dd>

Privilégio de segurança real a ser modificado. Por exemplo, para alterar o proprietário e a segurança da DACL, use:

`Option = 1 + 4`

ou

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**ALTERAR \_ INFORMAÇÕES \_ DE SEGURANÇA DO \_ PROPRIETÁRIO** (1)


</dt> <dd>

Altere o proprietário do arquivo lógico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**ALTERAR \_ INFORMAÇÕES \_ DE SEGURANÇA DE \_ GRUPO** (2)


</dt> <dd>

Altere o grupo do arquivo lógico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**ALTERAR \_ INFORMAÇÕES DE \_ SEGURANÇA \_ DACL** (4)


</dt> <dd>

Altere a DACL (lista de controle de acesso discricionário) do arquivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**ALTERAR \_ INFORMAÇÕES DE \_ SEGURANÇA \_ SACL** (8)


</dt> <dd>

Altere a SACL (lista de controle de acesso do sistema) do arquivo lógico.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) se as permissões são alteradas e um número diferente para indicar um erro.

<dl> <dt>

**Êxito**
</dt> <dd>

0

A solicitação foi bem-sucedida.

</dd> <dt>

**Acesso negado**
</dt> <dd>

2

Acesso negado.

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

A plataforma não é Windows.

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

**Arquivo inicial inválido**
</dt> <dd>

16

O arquivo inicial especificado não é válido.

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
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ ShortcutFile**](win32-shortcutfile.md)
</dt> </dl>

 

