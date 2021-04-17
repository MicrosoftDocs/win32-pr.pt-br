---
description: Obtém o status atual do cartão inteligente ou leitor.
ms.assetid: ae285e2e-6591-43ab-b92f-1ec755872379
title: 'Método ISCardManage:: status'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Status
api_type:
- COM
api_location: ''
ms.openlocfilehash: 26683823b5b709d86b36f4345b47f306f2000ef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749685"
---
# <a name="iscardmanagestatus-method"></a>Método ISCardManage:: status

\[O método de **status** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método de **status** Obtém o status atual do [*cartão inteligente*](../secgloss/s-gly.md) ou [*leitor*](../secgloss/r-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Status(
  [out] SCARD_STATES    *pStatus,
  [out] SCARD_PROTOCOLS *pProtocols
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStatus* \[ fora\]
</dt> <dd>

Ponteiro para um valor de enumeração de Estados SCARTARs \_ . No retorno, contém o status/estado atual.

</dd> <dt>

*pProtocols* \[ fora\]
</dt> <dd>

Ponteiro para um \_ valor de enumeração de protocolos scartar. No retorno, contém o protocolo atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

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
</dt> </dl>

 

 
