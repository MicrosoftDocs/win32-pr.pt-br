---
description: O&de GetOwner \# 8194; O método de classe WMI recupera o nome de usuário e o nome de domínio sob os quais o processo está sendo executado.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Método GetOwner da classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2fe91ef581490ab15869fa45c299c9e172c01df9d689a4fcd1546cbbf84621ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760436"
---
# <a name="getowner-method-of-the-win32_process-class"></a>Método GetOwner da classe de \_ processo do Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** recupera o nome de usuário e o nome de domínio sob o qual o processo está sendo executado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Usuário* \[ do fora\]
</dt> <dd>

Retorna o nome de usuário do proprietário deste processo.

</dd> <dt>

*Domínio* \[ do fora\]
</dt> <dd>

Retorna o nome de domínio no qual esse processo está em execução.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida** (0)
</dt> <dt>

**Acesso negado** (2)
</dt> <dt>

**Privilégio insuficiente** (3)
</dt> <dt>

**Falha desconhecida** (8)
</dt> <dt>

**Caminho não encontrado** (9)
</dt> <dt>

**Parâmetro inválido** (21)
</dt> <dt>

**Outro** (22 4294967295)
</dt> </dl>

## <a name="examples"></a>Exemplos

[A porcentagem de CPU do processo de monitor por nome com o proprietário](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) O exemplo de VBScript coleta a porcentagem de utilização da CPU ou do processador e pesquisa o proprietário do processo.

O exemplo [obter todos os servidores que uma lista de usuários está conectado](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) ao PowerShell consulta o WMI para o proprietário de todos os processos de explorer.exe.

O exemplo de código VBScript a seguir obtém o proprietário de cada processo em execução.


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
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

[**\_Processo Win32**](win32-process.md)
</dt> </dl>

 

