---
description: Limpa as informações de usuário em cache do objeto.
title: Método DIDiskQuotaUser. Invalidate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843267"
---
# <a name="didiskquotauserinvalidate-method"></a>Método DIDiskQuotaUser. Invalidate

Limpa as informações de usuário em cache do objeto.

## <a name="syntax"></a>Sintaxe


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método limpa as informações do usuário armazenadas no cache do objeto. Na próxima vez que uma solicitação for feita para informações relacionadas à cota, o objeto recuperará as informações do volume NTFS e atualizará o cache.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




