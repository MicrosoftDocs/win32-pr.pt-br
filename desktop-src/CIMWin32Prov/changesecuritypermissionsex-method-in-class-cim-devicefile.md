---
description: Altera as permissões de segurança para o arquivo de dispositivo especificado no caminho do objeto (esse método é uma versão estendida do método ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Método ChangeSecurityPermissionsEx da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6d70c11077873154040e30cabfb460546f79b1088ff124884e35f3698aaf78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959135"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a>Método ChangeSecurityPermissionsEx da classe \_ DeviceFile CIM

O **método ChangeSecurityPermissionsEx** altera as permissões de segurança para o arquivo de dispositivo especificado no caminho do objeto (esse método é uma versão estendida do [**método ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-cim-devicefile.md) Se o arquivo lógico for um diretório, esse método atuará recursivamente, alterando as permissões de segurança para todos os arquivos e subdados que o diretório contém. Esse método é herdado de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

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

> [!Caution]  
> Uma  ACL NULA na estrutura [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede acesso ilimitado.

 

</dd> <dt>

*Opção* \[ Em\]
</dt> <dd>

Privilégio de segurança a ser modificado. Por exemplo, para alterar o proprietário e a segurança da DACL, use

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

Altere a ACL do arquivo lógico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**ALTERAR \_ INFORMAÇÕES DE \_ SEGURANÇA \_ SACL** (8)


</dt> <dd>

Altere a ACL do sistema do arquivo lógico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será **nulo** se o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ in, opcional\]
</dt> <dd>

Arquivo filho (ou diretório) a ser usado como um ponto de partida para esse método. Normalmente, o *parâmetro StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for **nulo,** a operação será executada no arquivo (ou diretório) especificado na [**chamada ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Recursivo* \[ in, opcional\]
</dt> <dd>

Se **TRUE**, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela [**instância de \_ DeviceFile cim.**](cim-devicefile.md) Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

<dl> <dt>


</dt> <dd>

0

Sucesso.

</dd> <dt>


</dt> <dd>

2

Acesso negado

</dd> <dt>


</dt> <dd>

8

Falha não especificada.

</dd> <dt>


</dt> <dd>

9

Objeto inválido.

</dd> <dt>


</dt> <dd>

10

O objeto já existe.

</dd> <dt>


</dt> <dd>

11

Sistema de arquivos não NTFS.

</dd> <dt>


</dt> <dd>

12

Plataforma não Windows.

</dd> <dt>


</dt> <dd>

13

A unidade não é a mesma.

</dd> <dt>


</dt> <dd>

14

O diretório não está vazio.

</dd> <dt>


</dt> <dd>

15

Violação de compartilhamento.

</dd> <dt>


</dt> <dd>

16

Arquivo inicial inválido.

</dd> <dt>


</dt> <dd>

17

Privilégio não mantido.

</dd> <dt>


</dt> <dd>

21

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

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

[CIM \_ DeviceFile](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

