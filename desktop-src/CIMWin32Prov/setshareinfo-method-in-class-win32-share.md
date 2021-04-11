---
description: SetShareInfo&\# 8194; O método de classe WMI define os parâmetros de um recurso compartilhado.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Método SetShareInfo da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 54b599ed3124c0d06468bd15589d6aa8a93fb7c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164172"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Método SetShareInfo da classe de \_ compartilhamento do Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** define os parâmetros de um recurso compartilhado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*MaximumAllowed* \[ em, opcional\]
</dt> <dd>

Limite do número máximo de usuários com permissão para usar este recurso simultaneamente.

Exemplo: 10. Esse parâmetro é opcional.

</dd> <dt>

*Descrição* \[ do em, opcional\]
</dt> <dd>

Comentário opcional para descrever o recurso que está sendo compartilhado.

</dd> <dt>

*Acesso* \[ ao em, opcional\]
</dt> <dd>

Descritor de segurança para permissões de nível de usuário. Um descritor de segurança contém informações sobre a permissão, o proprietário e os recursos de acesso do recurso. Para obter mais informações, consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores listados na lista a seguir ou qualquer outro valor para indicar um erro.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Nome inválido** (9)
</dt> <dt>

**Nível inválido** (10)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Compartilhamento duplicado** (22)
</dt> <dt>

**Caminho Redirecionado** (23)
</dt> <dt>

**Dispositivo ou diretório desconhecido** (24)
</dt> <dt>

**Nome de rede não encontrado** (25)
</dt> <dt>

**Outro** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

O método **SetShareInfo** é um método de objeto dinâmico e é usado em uma ocorrência dessa classe.

Somente os membros do grupo local Administradores ou operadores de contas ou aqueles com associação de grupo de operador de servidor, impressão ou comunicação podem executar **SetShareInfo** com êxito. O operador Print só pode definir filas de impressora. O operador de comunicação só pode definir filas do dispositivo de comunicação.

## <a name="examples"></a>Exemplos

O exemplo do PowerShell a seguir atualiza o nome do compartilhamento **newShare** .


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



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

[**Compartilhamento do Win32 \_**](win32-share.md)
</dt> </dl>

 

