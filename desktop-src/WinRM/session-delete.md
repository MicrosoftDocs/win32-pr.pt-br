---
title: Método Session. Delete (WSManDisp. h)
description: Exclui o recurso especificado no URI de recurso.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método Delete
- Gerenciamento Remoto do Windows do método Delete, objeto Session
- Gerenciamento Remoto do Windows de objeto de sessão, método Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf4b46997a7e3cf50dbf50c2828de78a814a513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918180"
---
# <a name="sessiondelete-method"></a>Método Session. Delete

Exclui o recurso especificado no URI de recurso.

## <a name="syntax"></a>Sintaxe


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceURI* \[ no\]
</dt> <dd>

O URI do recurso a ser excluído. Você também pode usar um objeto [**ResourceLocator**](resourcelocator.md) para especificar o recurso.

</dd> <dt>

*sinalizadores* \[ de em, opcional\]
</dt> <dd>

Reservado para uso futuro. Deve ser definido como 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A sintaxe a seguir é usada para chamar esse método.


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir exclui os ouvintes configurados para transporte HTTP.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Session**](session.md)
</dt> </dl>

 

 





