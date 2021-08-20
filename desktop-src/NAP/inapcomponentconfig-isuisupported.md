---
title: Método INapComponentConfig IsUISupported (NapCommon. h)
description: Especifica se o componente dá suporte a uma interface do usuário personalizada.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Método IsUISupported NAP
- Método IsUISupported NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, método IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e343b037e4f77b4c1e342ffa78278854b11d714e09e9e57188d83fc9f93a180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134484"
---
# <a name="inapcomponentconfigisuisupported-method"></a>Método INapComponentConfig:: IsUISupported

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **IsUISupported** especifica se o componente dá suporte a uma interface de usuário personalizada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsSupported* \[ fora\]
</dt> <dd>

Um ponteiro para um BOOL que é definido como **true** se o componente dá suporte a uma interface do usuário personalizada; caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

A interface do usuário personalizada de um componente deve ser iniciada usando [**INapComponentConfig:: InvokeUI**](inapcomponentconfig-invokeui.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





