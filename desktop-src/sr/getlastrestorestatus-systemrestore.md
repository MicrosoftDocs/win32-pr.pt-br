---
title: Método GetLastRestoreStatus da classe SystemRestore
description: Recupera o status da última restauração do sistema.
ms.assetid: 03f9fd71-9f20-428e-bdca-4692e838581a
keywords:
- Restauração do sistema do método GetLastRestoreStatus
- GetLastRestoreStatus método de restauração do sistema, classe SystemRestore
- Restauração do sistema de classe SystemRestore, método GetLastRestoreStatus
topic_type:
- apiref
api_name:
- SystemRestore.GetLastRestoreStatus
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd1ef0e62f7874bb92f3c8e9ecec7b62a1b3ff3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763323"
---
# <a name="getlastrestorestatus-method-of-the-systemrestore-class"></a>Método GetLastRestoreStatus da classe SystemRestore

Recupera o status da última restauração do sistema.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetLastRestoreStatus();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O método retorna um dos valores de status a seguir.



| Valor retornado                                                                 | Descrição                                  |
|------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0</dt> </dl> | A última restauração falhou.<br/>          |
| <dl> <dt>1</dt> </dl> | A última restauração foi bem-sucedida.<br/>  |
| <dl> <dt>2</dt> </dl> | A última restauração foi interrompida.<br/> |



 

## <a name="examples"></a>Exemplos


```VB
'GetLastRestoreStatus Method of the SystemRestore Class
'Retrieves the status of the last system restore.
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
stat = obj.GetLastRestoreStatus()
If stat = 0 Then
    wscript.Echo "Failed"
ElseIf stat = 1 Then 
    wscript.Echo "Success"
ElseIf stat = 2 Then
    wscript.Echo "Interrrupted"
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

 

 





