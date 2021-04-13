---
description: Libera o uso exclusivo do cartão inteligente conectado.
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: 'Método ISCardManage:: SCardUnlock'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90c6b10d407992ae8147998d2d420989cc91e970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165342"
---
# <a name="iscardmanagescardunlock-method"></a>Método ISCardManage:: SCardUnlock

\[O método **SCardUnlock** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **SCardUnlock** libera o uso exclusivo do [*cartão inteligente*](../secgloss/s-gly.md)conectado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Disposição* \[ do no\]
</dt> <dd>

O estado para sair do cartão inteligente quando o bloqueio é liberado.

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**Deixe**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**REDEFINIR**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**Desligamento**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**EJEÇÃO**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operação concluída com sucesso.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O parâmetro de *disposição* não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

Para bloquear o cartão inteligente conectado, chame [**SCardLock**](iscardmanage-scardlock.md).

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

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
