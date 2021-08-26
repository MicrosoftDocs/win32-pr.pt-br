---
description: Permite que um aplicativo se reconecte a um cartão inteligente ou leitor sem a necessidade de emitir uma chamada de desanexação seguida por uma chamada AttachByHandle ou AttachByIFD, respectivamente.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'Método ISCardManage:: Reconnect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9c0359a062f62e49b52b92623714e6d94aff015e53a71afa45d4a433c31f28c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013976"
---
# <a name="iscardmanagereconnect-method"></a>Método ISCardManage:: Reconnect

\[O método **reconnect** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **reconnect** permite que um aplicativo se reconecte a um [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md) sem a necessidade de emitir uma chamada de [**desanexação**](iscardmanage-detach.md) seguida por uma chamada [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivamente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para anexar uma chamada de cartão inteligente [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md).

Para desanexar um cartão inteligente, [**desanexe**](iscardmanage-detach.md)a chamada.

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Detach**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
