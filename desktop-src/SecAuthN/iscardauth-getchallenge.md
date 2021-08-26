---
description: O método GetChallenge retorna um desafio do cartão inteligente.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: Método ISCardAuth::GetChallenge
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0132ab8b4b3b2f646639c1618a9f2ca7e67fad1ce2c2fcec38590c7608802091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015416"
---
# <a name="iscardauthgetchallenge-method"></a>Método ISCardAuth::GetChallenge

\[O **método GetChallenge** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método GetChallenge** retorna um desafio do [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lAlgoID* \[ in, opcional\]
</dt> <dd>

Algoritmo a ser usado no processo de autenticação.

</dd> <dt>

*lLengthOfChallenge* \[ Em\]
</dt> <dd>

Comprimento máximo da resposta esperada.

</dd> <dt>

*pParam* \[ Em\]
</dt> <dd>

Um [**objeto IByteBuffer**](ibytebuffer.md) que contém parâmetros específicos do fornecedor do processo de autenticação.

</dd> <dt>

*pBuffer* \[ in, out\]
</dt> <dd>

Na entrada, aponta para o buffer.

Na saída, contém os dados de desafio do cartão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para ver uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardAuth**](iscardauth.md).

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

[**ISCardAuth**](iscardauth.md)
</dt> </dl>

 

 
