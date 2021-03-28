---
description: Desliga o thread de resolução de nomes de usuário.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Método DiskQuotaControl. ShutdownNameResolution (Dskquota. h)
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
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010442"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>Método DiskQuotaControl. ShutdownNameResolution

Desliga o thread de resolução de nomes de usuário.

## <a name="syntax"></a>Sintaxe


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O resolvedor de nome de SID (identificador de segurança) traduz o SID para nomes de usuário em um thread em segundo plano. Esse thread é desligado automaticamente quando o objeto de controle de cota associado é destruído. No entanto, há alguns casos em que o thread não é mais necessário, mas o objeto ainda não está pronto para ser destruído. Um exemplo típico é quando nenhum processamento adicional está ocorrendo, mas os clientes ainda estão mantendo referências ao objeto. O método **ShutdownNameResolution** permite encerrar o thread do resolvedor e liberar os recursos associados sem destruir o objeto de controle de cota.

> [!Note]  
> Quando você desligar o thread do resolvedor, a resolução de nomes assíncronas será interrompida imediatamente. Se as chamadas forem feitas posteriormente para métodos como [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md), o objeto de cota poderá recriar o thread do resolvedor.

 

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

 

 




