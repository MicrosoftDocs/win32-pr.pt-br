---
description: A propriedade ComponentCurrentState do objeto Session é uma propriedade somente leitura que retorna o estado instalado atual do componente designado. Para valores de estado, consulte a propriedade ComponentRequestState.
ms.assetid: c8343e90-8867-462d-9844-e547341a590c
title: Propriedade Session.ComponentCurrentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ce060c7eddb76491480f4a1de9f477629da489ae9d8412adc02da25b8d7a0a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039847"
---
# <a name="sessioncomponentcurrentstate-property"></a>Propriedade Session.ComponentCurrentState

A **propriedade ComponentCurrentState** do [**objeto Session**](session-object.md) é uma propriedade somente leitura que retorna o estado instalado atual do componente designado. Para valores de estado, consulte a [**propriedade ComponentRequestState.**](session-componentrequeststate.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.ComponentCurrentState
```



## <a name="property-value"></a>Valor da propriedade

Nome da cadeia de caracteres necessária do componente solicitado, chave primária na tabela Componente.

## <a name="remarks"></a>Comentários

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sessão**](session-object.md)
</dt> <dt>

[**Propriedade ComponentRequestState**](session-componentrequeststate.md)
</dt> </dl>

 

 




