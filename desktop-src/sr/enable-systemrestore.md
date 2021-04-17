---
title: Habilitar o método da classe SystemRestore
description: Habilita o monitoramento em uma unidade específica.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Habilitar restauração do sistema de métodos
- Habilitar a restauração do sistema de método, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método Enable
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790349"
---
# <a name="enable-method-of-the-systemrestore-class"></a>Habilitar o método da classe SystemRestore

Habilita o monitoramento em uma unidade específica.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Unidade* \[ no\]
</dt> <dd>

A unidade a ser habilitada. A cadeia de caracteres da unidade deve estar no formato "C: \\ ". Se esse parâmetro for a unidade do sistema ou uma cadeia de caracteres vazia (""), todas as unidades serão monitoradas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, o valor de retorno será S \_ OK. Caso contrário, o método retorna um dos códigos de erro COM definidos em WinError. h.

## <a name="remarks"></a>Comentários

O método **Enable** não aguarda o monitoramento ser totalmente habilitado antes de ser retornado, pois isso pode levar algum tempo. Em vez disso, ele retorna imediatamente após iniciar o serviço de restauração do sistema e o driver de filtro.

Para habilitar a restauração do sistema em uma unidade que não seja do sistema, você deve primeiro habilitar a restauração do sistema na unidade do sistema.

Esse método falha no modo de segurança.

## <a name="examples"></a>Exemplos


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
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

 

 





