---
description: Cria a interface especificada.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Método ISCardManage:: createinterface'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170818"
---
# <a name="iscardmanagecreateinterface-method"></a>Método ISCardManage:: createinterface

\[O método **createinterface** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O método **createinterface** cria a interface especificada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pguidInterface* \[ no\]
</dt> <dd>

O valor de GUID da interface a ser criada.

</dd> <dt>

*bstrname* \[ no\]
</dt> <dd>

O nome da interface a ser criada se o GUID não estiver disponível. Os valores padrão são "CryptoProvider".

</dd> <dt>

*pUserData* \[ no\]
</dt> <dd>

Ponteiro para dados específicos do usuário a serem usados na criação de uma interface.

</dd> <dt>

*ppInterface* \[ fora\]
</dt> <dd>

Ponteiro para a interface retornada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Os possíveis valores de retorno são os seguintes:



| Código de retorno                                                                                   | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um dos parâmetros fornecidos não é válido.<br/>                                         |
| <dl> <dt>**\_ponteiro E**</dt> </dl>     | Um ponteiro inadequado foi passado no parâmetro *pguidInterface* ou *pUserData* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                                                        |



 

## <a name="remarks"></a>Comentários

Para obter uma lista de todos os métodos definidos pela interface [**ISCardManage**](iscardmanage.md) , consulte **ISCardManage**.

Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).

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

 

 
