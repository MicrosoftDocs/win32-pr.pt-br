---
description: Altera as permissões de segurança para o arquivo de dispositivo lógico especificado no caminho do objeto.
ms.assetid: 4b3e1a0e-3c9e-45bb-8c7b-cbbc8f9d1265
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissions da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a772c17695a537e4a9a8518bf05b052c0417f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457084"
---
# <a name="changesecuritypermissions-method-of-the-cim_devicefile-class"></a>Método ChangeSecurityPermissions da classe CIM \_ devicefile

O método **ChangeSecurityPermissions** altera as permissões de segurança para o arquivo de dispositivo lógico especificado no caminho do objeto. Se o arquivo lógico for um diretório, esse método agirá de forma recursiva, alterando as permissões de segurança para todos os arquivos e subdiretórios que o diretório contém. Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Especifica as informações de segurança.

> [!Caution]  
> Uma ACL (lista de controle de acesso) **nula** na estrutura do [**\_ descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.

 

</dd> <dt>

*Opção* \[ no\]
</dt> <dd>

Privilégio de segurança a ser modificado. Por exemplo, para alterar a segurança do proprietário e da DACL, use:

`Option = 1 + 4`

ou

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

Altere a ACL do arquivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Alterar \_ \_ \_ Informações de segurança da SACL** (8)


</dt> <dd>

Altere a ACL do sistema do arquivo lógico.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

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

Acesso negado.

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

**Arquivo de início inválido**
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

Este método não está implementado no momento pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**\_Dispositivo CIM**](changesecuritypermissions-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_Dispositivo CIM**](cim-devicefile.md)
</dt> </dl>

 

