---
title: Método Disable da classe SystemRestore
description: Desabilita o monitoramento em uma unidade específica.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Desabilitar a restauração do sistema de métodos
- Desabilitar a restauração do sistema de método, classe SystemRestore
- Método SystemRestore de restauração do sistema de classe, desabilitar
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085683"
---
# <a name="disable-method-of-the-systemrestore-class"></a>Método Disable da classe SystemRestore

Desabilita o monitoramento em uma unidade específica.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Unidade* \[ no\]
</dt> <dd>

A unidade a ser desabilitada. A cadeia de caracteres da unidade deve estar no formato "C: \\ ". Se esse parâmetro for a unidade do sistema ou uma cadeia de caracteres vazia (""), nenhuma unidade será monitorada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, o valor de retorno será S \_ OK. Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.

## <a name="examples"></a>Exemplos


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                         |
| Namespace<br/>                | \\Padrão raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemRestore**](systemrestore.md)
</dt> </dl>

 

 





