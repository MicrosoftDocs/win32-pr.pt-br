---
description: Cria uma interface ISCardFileAccess.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'Método ISCardManage:: createfileaccess'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8305b656391f509ea6da8a84c5815e5406d19c1d40fbf6c3a59d07660f31039d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014106"
---
# <a name="iscardmanagecreatefileaccess-method"></a>Método ISCardManage:: createfileaccess

\[O método **createfileaccess** está disponível para uso nos sistemas operacionais especificados na seção requisitos. ele não está disponível para uso no Windows server 2003 com Service Pack 1 (SP1) e posterior, Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **createfileaccess** cria uma interface [**ISCardFileAccess**](iscardfileaccess.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppISCardFileAccess* \[ fora\]
</dt> <dd>

Ponteiro retornado para a interface [**ISCardFileAccess**](iscardfileaccess.md) criada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um dos seguintes valores possíveis.



| Código de retorno                                                                                   | Descrição                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *ppISCardFileAccess* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppISCardFileAccess*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                    |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |
| Fim do suporte do cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
