---
description: Altera as permissões de segurança para o arquivo codec especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe Win32_CodecFile dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a025bd9be527237b16022d6544f024e6aa10d294637b16de1df31e43cfa830b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323076"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a>Método ChangeSecurityPermissionsEx da classe CodecFile win32 \_

O método de classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo codec especificado no caminho do objeto (esse método é uma versão estendida do [**método ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-win32-directory.md) Se o arquivo lógico for um diretório, esse método será recursivo e altera as permissões de segurança de todos os arquivos e subdiretivos que o diretório contém.

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

Expressão que é resolvida para uma instância do [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Esse descritor contém novas permissões de segurança para a instância do [**\_ CodecFile win32.**](win32-codecfile.md)

</dd> <dt>

*Opção* \[ Em\]
</dt> <dd>

Privilégio de segurança real a ser modificado. Por exemplo, para alterar a segurança da DACL (lista de controle de acesso discricionário) e do proprietário, use o seguinte:

`Option = 1 + 4`

-ou-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**ALTERAR \_ INFORMAÇÕES \_ DE SEGURANÇA DO \_ PROPRIETÁRIO** (1 (0x1))


</dt> <dd>

Altere o proprietário do arquivo lógico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**ALTERAR \_ INFORMAÇÕES \_ DE \_ SEGURANÇA DE** GRUPO (2 (0x2))


</dt> <dd>

Altere o grupo do arquivo lógico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**ALTERAR \_ INFORMAÇÕES DE \_ SEGURANÇA \_ DACL** (4 (0x4))


</dt> <dd>

Altere a DACL (lista de controle de acesso discricionário) do arquivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**ALTERAR \_ INFORMAÇÕES DE \_ SEGURANÇA \_ SACL** (8 (0x8))


</dt> <dd>

Altere a SACL (lista de controle de acesso do sistema) do arquivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nome do arquivo ou diretório em que **o método ChangeSecurityPermissionsEx** falhou. Esse parâmetro é nulo quando o método é bem-sucedido.

</dd> <dt>

*StartFileName* \[ in, opcional\]
</dt> <dd>

Nomeia o arquivo ou diretório filho a ser usado como um ponto de partida **para ChangeSecurityPermissionsEx.** Normalmente, o *parâmetro StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório em que ocorreu um erro da chamada de método anterior. Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na [**chamada ExecMethod.**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod)

</dd> <dt>

*Recursivo* \[ in, opcional\]
</dt> <dd>

Se **true**, as alterações de propriedade serão aplicadas recursivamente a arquivos e diretórios no diretório especificado pela [**instância de \_ LogicalFile**](cim-logicalfile.md) cim. Para instâncias de arquivo, o *parâmetro de entrada recursiva* é ignorado.

</dd> </dl>

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

A plataforma não é Windows NT ou Windows 2000.

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

[**CodecFile do Win32 \_**](win32-codecfile.md)
</dt> </dl>

 

