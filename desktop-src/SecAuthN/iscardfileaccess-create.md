---
description: O método Create cria um arquivo em um determinado local dentro do sistema de arquivos do cartão inteligente.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'Método ISCardFileAccess:: Create'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090455"
---
# <a name="iscardfileaccesscreate-method"></a>Método ISCardFileAccess:: Create

\[O método **Create** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **Create** cria um arquivo em um determinado local dentro do sistema de arquivos do [*cartão inteligente*](../secgloss/s-gly.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*refType* \[ no\]
</dt> <dd>

Tipo de referência usado em *bstrPathSpec*.

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ tipo \_ por \_ nome**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ tipo \_ por \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ tipo \_ por \_ curto**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ tipo \_ por \_ qualquer**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ no\]
</dt> <dd>

ID do arquivo a ser criado no contexto atual.

</dd> <dt>

*TLV* \[ no\]
</dt> <dd>

Lista de estruturas TLV (marca, comprimento, valor) que os valores precisam ser definidos.

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Especifica se as mensagens seguras devem ser usadas e os dados alocados.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**\_ \_ mensagens seguras do SC FL \_**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ fl \_ prealocado**
</dt> </dl> </dd> <dt>

*pDataBuffer* \[ no\]
</dt> <dd>

Ponteiro para dados alocados previamente.

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

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).

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

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
