---
description: Bloqueia um cartão inteligente conectado para uso exclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: Método ISCardManage::SCardLock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardLock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e610b914f1185eb2a1f4f7becdc8ba12c8aea4823630ecf3c5b9abe0f1ea3f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013936"
---
# <a name="iscardmanagescardlock-method"></a>Método ISCardManage::SCardLock

\[O **método SCardLock** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método SCardLock** bloqueia um cartão [*inteligente conectado para*](../secgloss/s-gly.md) uso exclusivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                            | Descrição                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Falha na conclusão da operação.<br/>     |



 

## <a name="remarks"></a>Comentários

Para liberar o uso exclusivo do cartão inteligente conectado, chame [**SCardUnlock.**](iscardmanage-scardunlock.md)

Para ver uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir a solicitação. Para obter mais informações, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardUnlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
