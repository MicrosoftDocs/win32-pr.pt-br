---
title: Método Restore da classe SystemRestore
description: Inicia uma restauração do sistema.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restaurar restauração do sistema do método
- Restaurar método restauração do sistema, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644352"
---
# <a name="restore-method-of-the-systemrestore-class"></a>Método Restore da classe SystemRestore

Inicia uma restauração do sistema. O chamador deve forçar a reinicialização do sistema. A restauração real ocorre durante a reinicialização.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SequenceNumber* \[ no\]
</dt> <dd>

O número de sequência do ponto de restauração. Para determinar o número de sequência de um ponto de restauração específico, enumere todos os pontos de restauração no sistema.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, o valor de retorno será S \_ OK. Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.

## <a name="examples"></a>Exemplos


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                         |
| Namespace<br/>                | \\ \\ Padrão raiz<br/>                                                        |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





