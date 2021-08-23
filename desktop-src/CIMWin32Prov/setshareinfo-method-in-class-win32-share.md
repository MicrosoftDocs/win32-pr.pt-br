---
description: O setShareInfo&\# 8194; O método de classe WMI define os parâmetros de um recurso compartilhado.
ms.assetid: f6379261-9325-4b7f-92df-438c5029569f
ms.tgt_platform: multiple
title: Método SetShareInfo da classe Win32_Share classe
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
ms.openlocfilehash: fb9ee76a0b8336ccdca90a04ee3c2a223b7269a30a00276418d6c46a8bb3abc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800896"
---
# <a name="setshareinfo-method-of-the-win32_share-class"></a>Método SetShareInfo da classe Win32 \_ Share

O método de classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetShareInfo** define os parâmetros de um recurso compartilhado.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

*MaximumAllowed* \[ in, opcional\]
</dt> <dd>

Limite o número máximo de usuários permitidos para usar esse recurso simultaneamente.

Exemplo: 10. Esse parâmetro é opcional.

</dd> <dt>

*Descrição* \[ in, opcional\]
</dt> <dd>

Comentário opcional para descrever o recurso que está sendo compartilhado.

</dd> <dt>

*Acesso* \[ in, opcional\]
</dt> <dd>

Descritor de segurança para permissões no nível do usuário. Um descritor de segurança contém informações sobre as funcionalidades de permissão, proprietário e acesso do recurso. Para obter mais informações, [**consulte Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

**Caminho redirecionado** (23)
</dt> <dt>

**Dispositivo ou diretório desconhecido** (24)
</dt> <dt>

**Nome líquido não encontrado** (25)
</dt> <dt>

**Outros** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentários

**O método SetShareInfo** é um método de objeto dinâmico e é usado em uma ocorrência dessa classe.

Somente os membros do grupo local Administradores ou Operadores de Conta ou aqueles com associação ao grupo de operadores Comunicação, Impressão ou Servidor podem executar **SetShareInfo com êxito.** O operador de impressão só pode definir filas de impressora. O operador Comunicação só pode definir filas de dispositivo de comunicação.

## <a name="examples"></a>Exemplos

O exemplo do PowerShell a seguir atualiza o nome do **compartilhamento newShare.**


```PowerShell
$newShare = Get-WmiObject win32_share | Where-Object {$_.name -eq "newShare"}
[void]$newShare.SetShareInfo($null,"This is my new description",$null)
```



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

[**Compartilhamento \_ win32**](win32-share.md)
</dt> </dl>

 

