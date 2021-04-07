---
description: O método de autenticação de usuário \_ permite o acesso aos serviços de autenticação de usuário.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'Método ISCardAuth:: User_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827033"
---
# <a name="iscardauthuser_auth-method"></a>Método de autenticação de usuário ISCardAuth:: \_

\[O método de **\_ autenticação de usuário** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método de autenticação de **usuário \_** permite o acesso aos serviços de autenticação de usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lAlgorID* \[ no\]
</dt> <dd>

Algoritmo a ser usado no processo de autenticação.

</dd> <dt>

*pParam* \[ no\]
</dt> <dd>

Um objeto [**IByteBuffer**](ibytebuffer.md) que contém parâmetros específicos do fornecedor do processo de autenticação.

</dd> <dt>

*pBuffer* \[ no\]
</dt> <dd>

Dados a serem usados no processo de autenticação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parâmetro inválido.<br/>                |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardAuth**](iscardauth.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**IByteBuffer**](ibytebuffer.md)
</dt> </dl>

 

 
