---
description: Gera um número aleatório seguro usando o CSP (provedor de serviços de criptografia) padrão.
ms.assetid: 52c49f73-58b8-455f-9368-54f38de55776
title: Método Utilities. getaleatório
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.GetRandom
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b7e02c7df61c1a2d710189fb2e5e0a21cc0b504
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813100"
---
# <a name="utilitiesgetrandom-method"></a>Método Utilities. getaleatório

\[O método **getaleatório** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O método **getaleatório** gera um número aleatório seguro usando o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) padrão.

## <a name="syntax"></a>Sintaxe


```VB
Utilities.GetRandom( _
  [ ByVal Length ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Comprimento* \[ em, opcional\]
</dt> <dd>

O comprimento, em bytes, do número aleatório a ser criado. O valor padrão é 8 bytes.

</dd> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica o tipo de codificação a ser usado para o número aleatório gerado. O valor padrão é capicote de \_ codificação \_ Binary. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um *comprimento* de número gerado aleatoriamente de bytes com a codificação especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Utilitários**](utilities.md)
</dt> </dl>

 

 
