---
description: Bloqueia um cartão inteligente conectado para uso exclusivo.
ms.assetid: c39a7cfe-04b6-4298-927a-4280664cf769
title: 'Método ISCardManage:: SCardLock'
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
ms.openlocfilehash: 2198f512fde90d1c79173f5151fc4f759944500a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165344"
---
# <a name="iscardmanagescardlock-method"></a>Método ISCardManage:: SCardLock

\[O método **SCardLock** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **SCardLock** bloqueia um [*cartão inteligente*](../secgloss/s-gly.md) conectado para uso exclusivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SCardLock();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                            | Descrição                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ falha**</dt> </dl> | Falha ao concluir a operação.<br/>     |



 

## <a name="remarks"></a>Comentários

Para liberar o uso exclusivo do cartão inteligente conectado, chame [**SCardUnlock**](iscardmanage-scardunlock.md).

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**SCardUnlock**](iscardmanage-scardunlock.md)
</dt> </dl>

 

 
