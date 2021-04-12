---
description: Cria uma interface ISCardVerify.
ms.assetid: 6338e672-83cd-46fe-8f94-f4ba6e2581ea
title: 'Método ISCardManage:: CreateCHVerification'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCHVerification
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a5909a8782571f9bd01a1c31e5ccd04c3d029df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171249"
---
# <a name="iscardmanagecreatechverification-method"></a>Método ISCardManage:: CreateCHVerification

\[O método **CreateCHVerification** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **CreateCHVerification** cria uma interface [**ISCardVerify**](iscardverify.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateCHVerification(
  [out] ISCardVerify **ppISCardVerify
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppISCardVerify* \[ fora\]
</dt> <dd>

Ponteiro retornado para a interface [**ISCardVerify**](iscardverify.md) criada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um dos seguintes valores possíveis:



| Código de retorno                                                                                   | Descrição                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O parâmetro *ppISCardVerify* não é válido.<br/>  |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado em *ppISCardVerify*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardManage**](iscardmanage.md).

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

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**ISCardVerify**](iscardverify.md)
</dt> </dl>

 

 
