---
description: Cria a interface especificada.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: Método ISCardManage::CreateInterface
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
ms.openlocfilehash: 8c9b231ec7930b78c1693e38268638e7a24b26dfa32d8f25acb5a429dbcdedc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922655"
---
# <a name="iscardmanagecreateinterface-method"></a>Método ISCardManage::CreateInterface

\[O **método CreateInterface** está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Os [Módulos de Cartão Inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]

O **método CreateInterface** cria a interface especificada.

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

*pguidInterface* \[ Em\]
</dt> <dd>

O valor guid da interface a ser criado.

</dd> <dt>

*bstrName* \[ Em\]
</dt> <dd>

O nome da interface a ser criado se o GUID não estiver disponível. Os valores padrão são "CryptoProvider".

</dd> <dt>

*pUserData* \[ Em\]
</dt> <dd>

Ponteiro para dados específicos do usuário a ser usado na criação de uma interface.

</dd> <dt>

*ppInterface* \[ out\]
</dt> <dd>

Ponteiro para a interface retornada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Os valores de retorno possíveis são os seguintes:



| Código de retorno                                                                                   | Description                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operação concluída com sucesso.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Um dos parâmetros fornecidos não é válido.<br/>                                         |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>     | Um ponteiro ruim foi passado no *parâmetro pguidInterface* ou *pUserData.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Sem memória.<br/>                                                                        |



 

## <a name="remarks"></a>Comentários

Para ver uma lista de todos os métodos definidos pela interface [**ISCardManage,**](iscardmanage.md) **consulte ISCardManage**.

Além dos códigos de erro COM listados acima, essa interface poderá retornar um código de erro de cartão inteligente se uma função de cartão inteligente tiver sido chamada para concluir [*a*](../secgloss/s-gly.md) solicitação. Para obter informações sobre códigos de erro de cartão inteligente, consulte [Valores de retorno de cartão inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/> |
| Fim do suporte ao cliente<br/>    | Windows XP<br/>                                |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
