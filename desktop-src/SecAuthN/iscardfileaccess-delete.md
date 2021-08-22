---
description: O método Delete exclui um arquivo em um determinado local dentro do sistema de arquivos de cartão inteligente.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Método ISCardFileAccess::D elete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 721830ea3d446585e7f52c699642b1534c78d34826722b5737e191dfce94c817
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008044"
---
# <a name="iscardfileaccessdelete-method"></a>Método ISCardFileAccess::D elete

\[O **método** Delete está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método Delete** exclui um arquivo em um determinado local dentro do sistema de [*arquivos*](../secgloss/s-gly.md) de cartão inteligente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*refType* \[ Em\]
</dt> <dd>

Tipo de referência usado em *bstrPathSpec.*

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

**SC \_ TYPE \_ BY \_ NAME**
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

**SC \_ TYPE \_ BY \_ ID**
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

**SC \_ TYPE \_ BY \_ SHORT**
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

**SC \_ TYPE \_ BY \_ ANY**
</dt> </dl> </dd> <dt>

*bstrPathSpec* \[ Em\]
</dt> <dd>

Identificador do arquivo a ser excluído.

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Especifica se as mensagens seguras devem ser usadas e os dados pré-alocados.

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

**SC \_ FL \_ SECURE \_ MESSAGING**
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

**SC \_ FL \_ PRÉ-ALOCADO**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                  | Descrição                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | A operação foi concluída com êxito.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Parâmetro inválido.<br/>                             |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | A interface não implementou esse método.<br/> |



 

## <a name="remarks"></a>Comentários

Para ver uma lista de todos os métodos definidos por essa interface, consulte [**ISCardFileAccess**](iscardfileaccess.md).

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

[**Criar**](iscardfileaccess-create.md)
</dt> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> </dl>

 

 
