---
title: Método INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Recupera o número total de atributos na SoH.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Método GetNumberOfAttributes NAP
- Método GetNumberOfAttributes NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, método GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55805d85cc6a809a915f3998ab1b3dd218bd35a10b3b0044ff7c78130a72d97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621167"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a>Método INapSoHProcessor:: GetNumberOfAttributes

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHProcessor:: GetNumberOfAttributes** recupera o número total de atributos na soh.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*attributeCount* \[ fora\]
</dt> <dd>

Um ponteiro para a contagem de atributos retornados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Outros códigos de erro específicos de COM também podem ser retornados.



| Código de retorno                                                                                     | Descrição                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Êxito na operação.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Erro de permissões, acesso negado.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | O limite de recursos do sistema não pôde executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





