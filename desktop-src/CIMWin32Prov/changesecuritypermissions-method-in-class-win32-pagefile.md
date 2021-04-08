---
description: Altera as permissões de segurança para o arquivo de paginação lógica especificado no caminho do objeto.
ms.assetid: 3abdfa1d-49d8-4676-b7a5-3be528938ec4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: cc30d8780f7c0573b9a63ff83f16ad46b9d2a70f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920421"
---
# <a name="changesecuritypermissions-method-of-the-win32_pagefile-class"></a>Método ChangeSecurityPermissions da classe de \_ arquivo de paginação Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de paginação lógica especificado no caminho do objeto. Se o arquivo lógico for um diretório, **ChangeSecurityPermissions** será recursivo e alterará as permissões de segurança de todos os arquivos e subdiretórios que o diretório contém.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecurityDescriptor* \[ no\]
</dt> <dd>

Expressão que resolve para uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Este descritor contém novas permissões de segurança para a instância do [**\_ arquivo de paginação Win32**](win32-pagefile.md).

</dd> <dt>

*Opção* \[ no\]
</dt> <dd>

Privilégio de segurança a ser modificado. Por exemplo, para alterar a segurança do proprietário e da DACL (lista de controle de acesso discricionário), use:

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

Altere a DACL do arquivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)


</dt> <dd>

Altere a lista de controle de acesso do sistema (SACL) do arquivo lógico.

</dd> </dl> </dd> </dl>

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

Um privilégio necessário para a operação está ausente.

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

[**\_Arquivo de paginação Win32**](win32-pagefile.md)
</dt> </dl>

 

