---
description: Faz com que o arquivo especificado (EF ou DF) não seja válido. Um arquivo que não é válido não pode ser acessado por outros métodos antes de usar o rehabilitate.
ms.assetid: 5600fcf0-091c-437e-a45c-4de5b0a47d68
title: 'Método ISCardFileAccess:: Invalidate'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Invalidate
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3e1d74885f97eca64f403155f1dba52e398b9426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752227"
---
# <a name="iscardfileaccessinvalidate-method"></a>Método ISCardFileAccess:: Invalidate

\[O método **Invalidate** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Invalidate** faz com que o arquivo especificado (EF ou DF) não seja válido. Um arquivo que não é válido não pode ser acessado por outros métodos antes de usar o [**rehabilitate**](iscardfileaccess-rehabilitate.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Invalidate(
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrPathSpec* \[ no\]
</dt> <dd>

Grupo.

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Especifica se as mensagens seguras devem ser usadas.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ mensagens seguras do SC FL \_**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um parâmetro não é válido.<br/>         |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                    |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).

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

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**Rehabilitate**](iscardfileaccess-rehabilitate.md)
</dt> </dl>

 

 
