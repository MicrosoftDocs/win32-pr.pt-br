---
title: Método getfriendlyname do INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter o nome amigável de um cliente de integridade.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Método getfriendlyname NAP
- Método getfriendlyname NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método getamigávelname
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3236a9d4959c441816aa476993d95286b4ac1f710ccdb63325aba225bfabb106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799711"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a>Método INapComponentInfo:: getfriendlyname

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método de retorno de chamada **INapComponentInfo:: Getamigávelname** é usado pelo sistema NAP para obter o nome amigável de um cliente de integridade.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyName* \[ fora\]
</dt> <dd>

Um ponteiro para uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso do nome amigável.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne um desses códigos de erro com base no resultado dessa operação.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | A operação teve êxito.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>


</dt> <dt>

[**INapComponentInfo**](inapcomponentinfo.md)
</dt> </dl>

 

 





