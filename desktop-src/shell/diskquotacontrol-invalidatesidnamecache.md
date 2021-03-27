---
description: Invalida o cache de nome de usuário da ID de segurança.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Método DiskQuotaControl. InvalidateSidNameCache (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920750"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a>Método DiskQuotaControl. InvalidateSidNameCache

Invalida o cache de nome de usuário da ID de segurança.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os nomes de usuário e as IDs de segurança associadas são armazenados em um cache. Você pode limpar esse cache chamando **InvalidateSidNameCache**. Se você criar subseqüentemente um novo objeto de usuário, as informações precisarão ser obtidas no controlador de domínio e o cache precisará ser restabelecido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




