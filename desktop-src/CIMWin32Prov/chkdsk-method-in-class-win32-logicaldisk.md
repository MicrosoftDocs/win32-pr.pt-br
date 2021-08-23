---
description: Invoca a operação chkdsk no disco.
ms.assetid: 65942702-b660-46cd-b614-e3e1ec3df7b9
ms.tgt_platform: multiple
title: Método chkdsk da classe Win32_LogicalDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDisk.Chkdsk
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 24d7052cd7d36da8a9464cbbef142904a70f83767872dadf25fda2033fa66fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959105"
---
# <a name="chkdsk-method-of-the-win32_logicaldisk-class"></a>Método chkdsk da classe do \_ LogicalDisk do Win32

O método de instância **chkdsk** invoca a operação **chkdsk** no disco.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Chkdsk(
  [in] boolean FixErrors = ,
  [in] boolean VigorousIndexCheck = ,
  [in] boolean SkipFolderCycle = ,
  [in] boolean ForceDismount = ,
  [in] boolean RecoverBadSectors = ,
  [in] boolean OKToRunAtBootUp = 
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FixErrors* \[ no\]
</dt> <dd>

Indica o que deve ser feito para erros encontrados no disco. Se **for true**, os erros serão corrigidos. O padrão é **false**.

</dd> <dt>

*VigorousIndexCheck* \[ no\]
</dt> <dd>

Se **for true**, uma verificação menos rigorosa de entradas de índice deverá ser executada. O padrão é **false**.

</dd> <dt>

*SkipFolderCycle* \[ no\]
</dt> <dd>

Se **for true**, a verificação de ciclo de pastas deverá ser ignorada. O padrão é **true**.

</dd> <dt>

*ForceDismount* \[ no\]
</dt> <dd>

Se **for true**, a unidade deverá ser forçada a desmontar antes de verificar. O padrão é **false**.

</dd> <dt>

*RecoverBadSectors* \[ no\]
</dt> <dd>

Se **for verdadeiro**, os setores inválidos devem ser localizados e as informações legíveis devem ser recuperadas desses setores. O padrão é **false**.

</dd> <dt>

*OKToRunAtBootUp* \[ no\]
</dt> <dd>

Se **for true**, a operação **chkdsk** deverá ser executada no próximo tempo de inicialização, caso a operação não possa ser executada porque o disco está bloqueado no momento em que esse método é chamado. O padrão é **false**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) se for bem-sucedido. Outros valores são listados na lista a seguir. Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Êxito-chkdsk concluído**
</dt> <dd>

0

Êxito- [**chkdsk**](chkdsk-method-in-class-win32-logicaldisk.md) concluído

</dd> <dt>

**Êxito-bloqueado e chkdsk agendado na reinicialização**
</dt> <dd>

1

</dd> <dt>

**Falha-sistema de arquivos desconhecido**
</dt> <dd>

2

</dd> <dt>

**Falha-erro desconhecido**
</dt> <dd>

3

</dd> <dt>

**Falha-sistema de arquivos sem suporte**
</dt> <dd>

4

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método só é aplicável a essas instâncias de disco lógico que representam um disco físico no computador. Ele não é aplicável a unidades lógicas mapeadas.

## <a name="examples"></a>Exemplos

O[é o conjunto de bits sujos chkdsk definido em uma](https://Gallery.TechNet.Microsoft.Com/57076851-97fb-4af6-8c5c-1e34156ceab4) amostra de código do PowerShell do servidor examina o sistema remoto e retorna um verdadeiro ou falso se o sinalizador chkdsk/f foi definido.

O exemplo de código do PowerShell de [verificação](https://Gallery.TechNet.Microsoft.Com/Remotely-scan-disk-dd4fc267) remota inicia ou agenda o disco de verificação remotamente.

O exemplo de código VBScript a seguir executa ChkDsk.exe na unidade D em um computador.


```VB
Const FIX_ERRORS = True 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objDisk = objWMIService.Get("Win32_LogicalDisk.DeviceID='D:'") 
 
errReturn = objDisk.ChkDsk(FIX_ERRORS) 
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

[**Disco \_ lógico do Win32**](win32-logicaldisk.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

