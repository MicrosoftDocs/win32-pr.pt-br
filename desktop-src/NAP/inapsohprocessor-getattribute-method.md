---
title: Método GetAttribute INapSoHProcessor (NapProtocol. h)
description: Recupera o tipo de atributo e o valor, dado o local do atributo.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Método GetAttribute NAP
- Método GetAttribute NAP, interface INapSoHProcessor
- Interface INapSoHProcessor NAP, método GetAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ba1b86ca1eab51fdca382a758a9a65650af2249eb0d605c24274c84d1f95669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939563"
---
# <a name="inapsohprocessorgetattribute-method"></a>Método INapSoHProcessor:: GetAttribute

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

O método **INapSoHProcessor:: GetAttribute** recupera o tipo e o valor do atributo, dado o local do atributo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*attributeLocation* \[ no\]
</dt> <dd>

O local (índice) do atributo cujo tipo e valor devem ser recuperados. O valor de *attributeLocation* é retornado de uma chamada anterior para [**INapSoHProcessor:: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).

</dd> <dt>

*tipo* \[ de fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**SoHAttributeType**](sohattributetype-enum.md) que especifica o tipo do atributo no *valor*.

</dd> <dt>

*valor* \[ do fora\]
</dt> <dd>

Um ponteiro para um ponteiro para uma estrutura [**SoHAttributeValue**](sohattributevalue-union.md) que contém o valor do atributo, conforme definido pelo *tipo*.

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
| Cabeçalho<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INapSoHProcessor**](inapsohprocessor.md)
</dt> </dl>

 

 





