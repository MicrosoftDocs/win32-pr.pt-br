---
description: Desliga o thread de resolução de nome de usuário.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Método DiskQuotaControl.ShutdownNameResolution (Dskquota.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da02f79ea8f7b582056e9c3c7c0c3f1db53fa9e08181559c99dd983924861c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459833"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>Método DiskQuotaControl.ShutdownNameResolution

Desliga o thread de resolução de nome de usuário.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O resolvedor de nome do SID (identificador de segurança) converte o SID em nomes de usuário em um thread em segundo plano. Esse thread é desligado automaticamente quando o objeto de controle de cota associado é destruído. No entanto, há alguns casos em que o thread não é mais necessário, mas o objeto ainda não está pronto para ser destruído. Um exemplo típico é quando nenhum processamento posterior está ocorrendo, mas os clientes ainda estão mantendo referências ao objeto . O **método ShutdownNameResolution** permite que você encerre o thread do resolvedor e livre os recursos associados sem destruir o objeto de controle de cota.

> [!Note]  
> Quando você desliga o thread do resolvedor, a resolução de nome assíncrona é interrompida imediatamente. Se as chamadas são feitas posteriormente para métodos como [**AddUser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md), o objeto de cota pode criar o thread resolvedor.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




